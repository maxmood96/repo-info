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
$ docker pull couchdb@sha256:78dcb93c69a8e9f010352d9010c9d02e77d6ee5af625206abea245f656e73e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:287516a45e781e1c64f99f49d34922dc58f0e000d2a0c19e4e021034bc50f33d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84603996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ac248c32e141a8d57312106c82c3bf5a2233e6ff71228c3db9143e0f53621e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:39 GMT
ADD file:08cfc7bf77cc2291c96890f44a435216cb1168c45cef77f7801430982c43ca58 in / 
# Thu, 11 Jan 2024 02:38:39 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 05:33:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jan 2024 05:33:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 11 Jan 2024 05:33:52 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:33:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 11 Jan 2024 05:33:56 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jan 2024 05:34:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:34:24 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Thu, 11 Jan 2024 05:34:24 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 11 Jan 2024 05:34:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 11 Jan 2024 05:34:43 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 11 Jan 2024 05:34:43 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 11 Jan 2024 05:34:43 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Thu, 11 Jan 2024 05:34:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 11 Jan 2024 05:34:44 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 05:34:44 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jan 2024 05:34:44 GMT
EXPOSE 4369 5984 9100
# Thu, 11 Jan 2024 05:34:44 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4648efdf070b378f12737b5cdacaded7b6294f27d0a0c1fb33849090813e920a`  
		Last Modified: Thu, 11 Jan 2024 02:43:48 GMT  
		Size: 27.2 MB (27188221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d912e6f1dd072f57b379a8acbab328980f4a6fd3cea623363042128d604a562f`  
		Last Modified: Thu, 11 Jan 2024 05:35:35 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2694f6780d7e6611967545e415f73b7a3942d57403be7d85893de295d24438`  
		Last Modified: Thu, 11 Jan 2024 05:35:34 GMT  
		Size: 6.7 MB (6704589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a6cb4f83addc4f4e977b984f0200f0b0d27c3aa9b7970fbd3c6947810ef46a`  
		Last Modified: Thu, 11 Jan 2024 05:35:34 GMT  
		Size: 1.3 MB (1259905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b3402a4569e7dcf8682d485597201cfc631d3c1d03789e27e84467bd7a9e60`  
		Last Modified: Thu, 11 Jan 2024 05:35:33 GMT  
		Size: 294.6 KB (294593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103dbf5055e2042566345f56c7107efabbe48d52d9aa3cead042973ad23df1b4`  
		Last Modified: Thu, 11 Jan 2024 05:35:47 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bb064386a6953d3c2ba54a9755c2b07f47652553441ebce7594e491fcfb8d7`  
		Last Modified: Thu, 11 Jan 2024 05:35:51 GMT  
		Size: 49.1 MB (49149684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b6f049e07b40c71a4226e4de093d0e830cb01eb22acf092803e5b8e4348803`  
		Last Modified: Thu, 11 Jan 2024 05:35:45 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba205a3b86ff8a5da1eaa7532fde104b57dac5736b072cc831d1db7f7def3cb2`  
		Last Modified: Thu, 11 Jan 2024 05:35:45 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea0843840e70d26c9a93d333ebf2ba4d5e1bec1efd3c9db99127511eb5bda4bc`  
		Last Modified: Thu, 11 Jan 2024 05:35:45 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:207b0468e52219037da01f3b03529703e27a2b3671e28afab2c1c14ef1779369`  
		Last Modified: Thu, 11 Jan 2024 05:35:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:7dda1442f1ed61b3177c8d6b48e0b83e999150fb5ea32fd16d72aa0c25b59ed1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73043944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c1d7ee3142789d609835f994069dfaf47fbf5f6a028597a33c4278c1f9c53a0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 11 Jan 2024 02:41:13 GMT
ADD file:0d7c08c3a192fbaded92a14e5eed44f5df7d00cd932ed45984ebb6b6e21446a6 in / 
# Thu, 11 Jan 2024 02:41:13 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:28:30 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jan 2024 06:28:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 11 Jan 2024 06:28:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:28:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 11 Jan 2024 06:28:40 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jan 2024 06:28:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:29:03 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Thu, 11 Jan 2024 06:29:04 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 11 Jan 2024 06:29:15 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 11 Jan 2024 06:29:15 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 11 Jan 2024 06:29:15 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 11 Jan 2024 06:29:15 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Thu, 11 Jan 2024 06:29:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 11 Jan 2024 06:29:16 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:29:16 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jan 2024 06:29:16 GMT
EXPOSE 4369 5984 9100
# Thu, 11 Jan 2024 06:29:16 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0d982983796daa327ca72ca687e0d8417bb909e8256d666725dae5ad846525ae`  
		Last Modified: Thu, 11 Jan 2024 02:45:24 GMT  
		Size: 26.0 MB (25969811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:045ae2b1301e0d4d902919f14ba0c2bdc42e0d49d80bf85546fbd245fe277883`  
		Last Modified: Thu, 11 Jan 2024 06:29:49 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19038a383fdabf47d56e07f75f86e36846e9757af76e450123327dc0d8017f8`  
		Last Modified: Thu, 11 Jan 2024 06:29:48 GMT  
		Size: 6.6 MB (6577588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b5bd25881dbfc612b64ae1b149a3d60568a830051bc583b6aead0e836ba1cec`  
		Last Modified: Thu, 11 Jan 2024 06:29:47 GMT  
		Size: 1.2 MB (1164775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d09863cad54994cd662045e95b2f2adea079ff9bbf8e1f4c89f9d4ef9411a0`  
		Last Modified: Thu, 11 Jan 2024 06:29:47 GMT  
		Size: 294.4 KB (294381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e0200db62e476518237c4760690af942c80421278723116f30fe57259ce7eb`  
		Last Modified: Thu, 11 Jan 2024 06:30:01 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a29954f135404df0c00dcbb980a06db34df78cb6278af1bccee53c811e84c3`  
		Last Modified: Thu, 11 Jan 2024 06:30:03 GMT  
		Size: 39.0 MB (39030351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927785dbf5d2fa144c05c808218f3769520c8f6d475af2e4f74a0076a8edeb5c`  
		Last Modified: Thu, 11 Jan 2024 06:29:59 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:154ab288d2d1bc04b3d15cf7387cd9471bb779ab3f956d8a60ffa04cbca0d1a8`  
		Last Modified: Thu, 11 Jan 2024 06:29:59 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538f6c048ba3d7c279cc7d7b0fde1211567919f76d1887ec0b4e479000123254`  
		Last Modified: Thu, 11 Jan 2024 06:29:59 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6b0ed8b17d8d9626c4c5abb04e5cd02433a43a247bdac473f03377d1589861`  
		Last Modified: Thu, 11 Jan 2024 06:29:59 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:78dcb93c69a8e9f010352d9010c9d02e77d6ee5af625206abea245f656e73e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:287516a45e781e1c64f99f49d34922dc58f0e000d2a0c19e4e021034bc50f33d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84603996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ac248c32e141a8d57312106c82c3bf5a2233e6ff71228c3db9143e0f53621e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:39 GMT
ADD file:08cfc7bf77cc2291c96890f44a435216cb1168c45cef77f7801430982c43ca58 in / 
# Thu, 11 Jan 2024 02:38:39 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 05:33:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jan 2024 05:33:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 11 Jan 2024 05:33:52 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:33:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 11 Jan 2024 05:33:56 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jan 2024 05:34:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:34:24 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Thu, 11 Jan 2024 05:34:24 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 11 Jan 2024 05:34:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 11 Jan 2024 05:34:43 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 11 Jan 2024 05:34:43 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 11 Jan 2024 05:34:43 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Thu, 11 Jan 2024 05:34:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 11 Jan 2024 05:34:44 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 05:34:44 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jan 2024 05:34:44 GMT
EXPOSE 4369 5984 9100
# Thu, 11 Jan 2024 05:34:44 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4648efdf070b378f12737b5cdacaded7b6294f27d0a0c1fb33849090813e920a`  
		Last Modified: Thu, 11 Jan 2024 02:43:48 GMT  
		Size: 27.2 MB (27188221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d912e6f1dd072f57b379a8acbab328980f4a6fd3cea623363042128d604a562f`  
		Last Modified: Thu, 11 Jan 2024 05:35:35 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2694f6780d7e6611967545e415f73b7a3942d57403be7d85893de295d24438`  
		Last Modified: Thu, 11 Jan 2024 05:35:34 GMT  
		Size: 6.7 MB (6704589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a6cb4f83addc4f4e977b984f0200f0b0d27c3aa9b7970fbd3c6947810ef46a`  
		Last Modified: Thu, 11 Jan 2024 05:35:34 GMT  
		Size: 1.3 MB (1259905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b3402a4569e7dcf8682d485597201cfc631d3c1d03789e27e84467bd7a9e60`  
		Last Modified: Thu, 11 Jan 2024 05:35:33 GMT  
		Size: 294.6 KB (294593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103dbf5055e2042566345f56c7107efabbe48d52d9aa3cead042973ad23df1b4`  
		Last Modified: Thu, 11 Jan 2024 05:35:47 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bb064386a6953d3c2ba54a9755c2b07f47652553441ebce7594e491fcfb8d7`  
		Last Modified: Thu, 11 Jan 2024 05:35:51 GMT  
		Size: 49.1 MB (49149684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b6f049e07b40c71a4226e4de093d0e830cb01eb22acf092803e5b8e4348803`  
		Last Modified: Thu, 11 Jan 2024 05:35:45 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba205a3b86ff8a5da1eaa7532fde104b57dac5736b072cc831d1db7f7def3cb2`  
		Last Modified: Thu, 11 Jan 2024 05:35:45 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea0843840e70d26c9a93d333ebf2ba4d5e1bec1efd3c9db99127511eb5bda4bc`  
		Last Modified: Thu, 11 Jan 2024 05:35:45 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:207b0468e52219037da01f3b03529703e27a2b3671e28afab2c1c14ef1779369`  
		Last Modified: Thu, 11 Jan 2024 05:35:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:7dda1442f1ed61b3177c8d6b48e0b83e999150fb5ea32fd16d72aa0c25b59ed1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73043944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c1d7ee3142789d609835f994069dfaf47fbf5f6a028597a33c4278c1f9c53a0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 11 Jan 2024 02:41:13 GMT
ADD file:0d7c08c3a192fbaded92a14e5eed44f5df7d00cd932ed45984ebb6b6e21446a6 in / 
# Thu, 11 Jan 2024 02:41:13 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:28:30 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jan 2024 06:28:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 11 Jan 2024 06:28:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:28:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 11 Jan 2024 06:28:40 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jan 2024 06:28:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:29:03 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Thu, 11 Jan 2024 06:29:04 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 11 Jan 2024 06:29:15 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 11 Jan 2024 06:29:15 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 11 Jan 2024 06:29:15 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 11 Jan 2024 06:29:15 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Thu, 11 Jan 2024 06:29:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 11 Jan 2024 06:29:16 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:29:16 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jan 2024 06:29:16 GMT
EXPOSE 4369 5984 9100
# Thu, 11 Jan 2024 06:29:16 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0d982983796daa327ca72ca687e0d8417bb909e8256d666725dae5ad846525ae`  
		Last Modified: Thu, 11 Jan 2024 02:45:24 GMT  
		Size: 26.0 MB (25969811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:045ae2b1301e0d4d902919f14ba0c2bdc42e0d49d80bf85546fbd245fe277883`  
		Last Modified: Thu, 11 Jan 2024 06:29:49 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19038a383fdabf47d56e07f75f86e36846e9757af76e450123327dc0d8017f8`  
		Last Modified: Thu, 11 Jan 2024 06:29:48 GMT  
		Size: 6.6 MB (6577588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b5bd25881dbfc612b64ae1b149a3d60568a830051bc583b6aead0e836ba1cec`  
		Last Modified: Thu, 11 Jan 2024 06:29:47 GMT  
		Size: 1.2 MB (1164775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d09863cad54994cd662045e95b2f2adea079ff9bbf8e1f4c89f9d4ef9411a0`  
		Last Modified: Thu, 11 Jan 2024 06:29:47 GMT  
		Size: 294.4 KB (294381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e0200db62e476518237c4760690af942c80421278723116f30fe57259ce7eb`  
		Last Modified: Thu, 11 Jan 2024 06:30:01 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a29954f135404df0c00dcbb980a06db34df78cb6278af1bccee53c811e84c3`  
		Last Modified: Thu, 11 Jan 2024 06:30:03 GMT  
		Size: 39.0 MB (39030351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927785dbf5d2fa144c05c808218f3769520c8f6d475af2e4f74a0076a8edeb5c`  
		Last Modified: Thu, 11 Jan 2024 06:29:59 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:154ab288d2d1bc04b3d15cf7387cd9471bb779ab3f956d8a60ffa04cbca0d1a8`  
		Last Modified: Thu, 11 Jan 2024 06:29:59 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538f6c048ba3d7c279cc7d7b0fde1211567919f76d1887ec0b4e479000123254`  
		Last Modified: Thu, 11 Jan 2024 06:29:59 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6b0ed8b17d8d9626c4c5abb04e5cd02433a43a247bdac473f03377d1589861`  
		Last Modified: Thu, 11 Jan 2024 06:29:59 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:78dcb93c69a8e9f010352d9010c9d02e77d6ee5af625206abea245f656e73e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:287516a45e781e1c64f99f49d34922dc58f0e000d2a0c19e4e021034bc50f33d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84603996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ac248c32e141a8d57312106c82c3bf5a2233e6ff71228c3db9143e0f53621e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:39 GMT
ADD file:08cfc7bf77cc2291c96890f44a435216cb1168c45cef77f7801430982c43ca58 in / 
# Thu, 11 Jan 2024 02:38:39 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 05:33:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jan 2024 05:33:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 11 Jan 2024 05:33:52 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:33:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 11 Jan 2024 05:33:56 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jan 2024 05:34:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:34:24 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Thu, 11 Jan 2024 05:34:24 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 11 Jan 2024 05:34:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 11 Jan 2024 05:34:43 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 11 Jan 2024 05:34:43 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 11 Jan 2024 05:34:43 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Thu, 11 Jan 2024 05:34:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 11 Jan 2024 05:34:44 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 05:34:44 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jan 2024 05:34:44 GMT
EXPOSE 4369 5984 9100
# Thu, 11 Jan 2024 05:34:44 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4648efdf070b378f12737b5cdacaded7b6294f27d0a0c1fb33849090813e920a`  
		Last Modified: Thu, 11 Jan 2024 02:43:48 GMT  
		Size: 27.2 MB (27188221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d912e6f1dd072f57b379a8acbab328980f4a6fd3cea623363042128d604a562f`  
		Last Modified: Thu, 11 Jan 2024 05:35:35 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2694f6780d7e6611967545e415f73b7a3942d57403be7d85893de295d24438`  
		Last Modified: Thu, 11 Jan 2024 05:35:34 GMT  
		Size: 6.7 MB (6704589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a6cb4f83addc4f4e977b984f0200f0b0d27c3aa9b7970fbd3c6947810ef46a`  
		Last Modified: Thu, 11 Jan 2024 05:35:34 GMT  
		Size: 1.3 MB (1259905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b3402a4569e7dcf8682d485597201cfc631d3c1d03789e27e84467bd7a9e60`  
		Last Modified: Thu, 11 Jan 2024 05:35:33 GMT  
		Size: 294.6 KB (294593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103dbf5055e2042566345f56c7107efabbe48d52d9aa3cead042973ad23df1b4`  
		Last Modified: Thu, 11 Jan 2024 05:35:47 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bb064386a6953d3c2ba54a9755c2b07f47652553441ebce7594e491fcfb8d7`  
		Last Modified: Thu, 11 Jan 2024 05:35:51 GMT  
		Size: 49.1 MB (49149684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b6f049e07b40c71a4226e4de093d0e830cb01eb22acf092803e5b8e4348803`  
		Last Modified: Thu, 11 Jan 2024 05:35:45 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba205a3b86ff8a5da1eaa7532fde104b57dac5736b072cc831d1db7f7def3cb2`  
		Last Modified: Thu, 11 Jan 2024 05:35:45 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea0843840e70d26c9a93d333ebf2ba4d5e1bec1efd3c9db99127511eb5bda4bc`  
		Last Modified: Thu, 11 Jan 2024 05:35:45 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:207b0468e52219037da01f3b03529703e27a2b3671e28afab2c1c14ef1779369`  
		Last Modified: Thu, 11 Jan 2024 05:35:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:7dda1442f1ed61b3177c8d6b48e0b83e999150fb5ea32fd16d72aa0c25b59ed1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73043944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c1d7ee3142789d609835f994069dfaf47fbf5f6a028597a33c4278c1f9c53a0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 11 Jan 2024 02:41:13 GMT
ADD file:0d7c08c3a192fbaded92a14e5eed44f5df7d00cd932ed45984ebb6b6e21446a6 in / 
# Thu, 11 Jan 2024 02:41:13 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:28:30 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jan 2024 06:28:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 11 Jan 2024 06:28:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:28:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 11 Jan 2024 06:28:40 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jan 2024 06:28:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:29:03 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Thu, 11 Jan 2024 06:29:04 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 11 Jan 2024 06:29:15 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 11 Jan 2024 06:29:15 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 11 Jan 2024 06:29:15 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 11 Jan 2024 06:29:15 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Thu, 11 Jan 2024 06:29:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 11 Jan 2024 06:29:16 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:29:16 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jan 2024 06:29:16 GMT
EXPOSE 4369 5984 9100
# Thu, 11 Jan 2024 06:29:16 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0d982983796daa327ca72ca687e0d8417bb909e8256d666725dae5ad846525ae`  
		Last Modified: Thu, 11 Jan 2024 02:45:24 GMT  
		Size: 26.0 MB (25969811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:045ae2b1301e0d4d902919f14ba0c2bdc42e0d49d80bf85546fbd245fe277883`  
		Last Modified: Thu, 11 Jan 2024 06:29:49 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19038a383fdabf47d56e07f75f86e36846e9757af76e450123327dc0d8017f8`  
		Last Modified: Thu, 11 Jan 2024 06:29:48 GMT  
		Size: 6.6 MB (6577588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b5bd25881dbfc612b64ae1b149a3d60568a830051bc583b6aead0e836ba1cec`  
		Last Modified: Thu, 11 Jan 2024 06:29:47 GMT  
		Size: 1.2 MB (1164775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d09863cad54994cd662045e95b2f2adea079ff9bbf8e1f4c89f9d4ef9411a0`  
		Last Modified: Thu, 11 Jan 2024 06:29:47 GMT  
		Size: 294.4 KB (294381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e0200db62e476518237c4760690af942c80421278723116f30fe57259ce7eb`  
		Last Modified: Thu, 11 Jan 2024 06:30:01 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a29954f135404df0c00dcbb980a06db34df78cb6278af1bccee53c811e84c3`  
		Last Modified: Thu, 11 Jan 2024 06:30:03 GMT  
		Size: 39.0 MB (39030351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927785dbf5d2fa144c05c808218f3769520c8f6d475af2e4f74a0076a8edeb5c`  
		Last Modified: Thu, 11 Jan 2024 06:29:59 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:154ab288d2d1bc04b3d15cf7387cd9471bb779ab3f956d8a60ffa04cbca0d1a8`  
		Last Modified: Thu, 11 Jan 2024 06:29:59 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538f6c048ba3d7c279cc7d7b0fde1211567919f76d1887ec0b4e479000123254`  
		Last Modified: Thu, 11 Jan 2024 06:29:59 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6b0ed8b17d8d9626c4c5abb04e5cd02433a43a247bdac473f03377d1589861`  
		Last Modified: Thu, 11 Jan 2024 06:29:59 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3`

```console
$ docker pull couchdb@sha256:d684daac1e11c90df0f4ae9f5cc9866b198d03d1b636867741992b12f2dfeeb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:94eae1e4891cab1426c43e968258c444a9e4ec711b8d6e80dd19a11e48b56910
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.3 MB (90282155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ba54687bbde594dc5a12c99a6a7228ec9bd8140c9aeaf68d61103a8412dea7`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 05:32:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jan 2024 05:32:52 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 11 Jan 2024 05:32:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:33:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Thu, 11 Jan 2024 05:33:02 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jan 2024 05:33:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:33:08 GMT
ENV COUCHDB_VERSION=3.3.3
# Thu, 11 Jan 2024 05:33:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 11 Jan 2024 05:33:21 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 11 Jan 2024 05:33:21 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 11 Jan 2024 05:33:21 GMT
COPY --chown=couchdb:couchdbfile:e5db3ae8229456931b3901d8737d15bbebc21bae345eb60dc63b3edc7a03cfbc in /opt/couchdb/etc/ 
# Thu, 11 Jan 2024 05:33:21 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Thu, 11 Jan 2024 05:33:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 11 Jan 2024 05:33:22 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 05:33:22 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jan 2024 05:33:22 GMT
EXPOSE 4369 5984 9100
# Thu, 11 Jan 2024 05:33:22 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfeb8d6d7cb9ec479de9e07297a4472878669f03cdc566d5ba2bdf49121cdbd`  
		Last Modified: Thu, 11 Jan 2024 05:35:00 GMT  
		Size: 3.4 KB (3410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7ac1349877a8205b90d6e6d1ef8cfa4d201f84fc189f8655d5e0525c735ee0`  
		Last Modified: Thu, 11 Jan 2024 05:34:59 GMT  
		Size: 5.2 MB (5226552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efbad6a63f2382da1e97c8d1dc6a5cb77899556bbd8fad2aaf8dd66b2ce00604`  
		Last Modified: Thu, 11 Jan 2024 05:34:58 GMT  
		Size: 610.9 KB (610908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227a8bbc783b3bd4eeed204844a79a51702307ae9b08da4ae1a162f142c48334`  
		Last Modified: Thu, 11 Jan 2024 05:34:58 GMT  
		Size: 295.1 KB (295133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3baadb6b9da90e40a0a57037da3b6e96d8599c58eff15ec5a6708bd0df6ab197`  
		Last Modified: Thu, 11 Jan 2024 05:34:58 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b705d298942cad7478031a63b4dc673d7d112dd13144ca0f6b4a85cf1c2318ec`  
		Last Modified: Thu, 11 Jan 2024 05:35:02 GMT  
		Size: 52.7 MB (52723949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a7281945f13c96bd64bdd2151029ecdd55723a1d6b57b9a88cc787f00c3f4f`  
		Last Modified: Thu, 11 Jan 2024 05:34:56 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7595f19c0256c9fbc059ca171d4909f09e648811bf4a86e74eff51cf29319477`  
		Last Modified: Thu, 11 Jan 2024 05:34:56 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8224f3b72b8930d3657822dcad3731868ebeeca1815bba4374e1c06824dc3133`  
		Last Modified: Thu, 11 Jan 2024 05:34:56 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a4cce3951e5070185c31edf9e8b96bc1b2fef875581f66f76059c20cbee6218`  
		Last Modified: Thu, 11 Jan 2024 05:34:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:8186dcf53c5964afdb14024925e7aa13e71e9f22b665cbbe926e80bc1d828503
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88720355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4daaa9a74f3ce7fabf84b8351b56756ad504ca89ed84a6bddf6a42e63d2675bd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:27:45 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jan 2024 06:27:46 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 11 Jan 2024 06:27:52 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:27:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Thu, 11 Jan 2024 06:27:54 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jan 2024 06:27:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:27:59 GMT
ENV COUCHDB_VERSION=3.3.3
# Thu, 11 Jan 2024 06:27:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 11 Jan 2024 06:28:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 11 Jan 2024 06:28:11 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 11 Jan 2024 06:28:11 GMT
COPY --chown=couchdb:couchdbfile:e5db3ae8229456931b3901d8737d15bbebc21bae345eb60dc63b3edc7a03cfbc in /opt/couchdb/etc/ 
# Thu, 11 Jan 2024 06:28:11 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Thu, 11 Jan 2024 06:28:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 11 Jan 2024 06:28:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:28:12 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jan 2024 06:28:12 GMT
EXPOSE 4369 5984 9100
# Thu, 11 Jan 2024 06:28:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ccc2078107ccc438fcb3b557ed215d440cd15f6f1879ad9db9f9b84b6946ac2`  
		Last Modified: Thu, 11 Jan 2024 06:29:31 GMT  
		Size: 3.4 KB (3433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562c17c5f419b97b03f49e7bed7c8cfd4d92ba18af2b014b62eb052a179e63ac`  
		Last Modified: Thu, 11 Jan 2024 06:29:30 GMT  
		Size: 5.2 MB (5210746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0a74a2782d1ffc7d869c33ab658ff80a6d3cfcd8903731d2b6b85bce269f3a`  
		Last Modified: Thu, 11 Jan 2024 06:29:29 GMT  
		Size: 567.1 KB (567052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d92f4c25743b8992888f53be6782574bfbbfd772cc684706e5b48a64335287`  
		Last Modified: Thu, 11 Jan 2024 06:29:29 GMT  
		Size: 295.0 KB (295014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fdc8f03011aa4022b246fe0407ba7262723f0241e4cd3d25a21dff79bfb5a38`  
		Last Modified: Thu, 11 Jan 2024 06:29:29 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526e7e3d442f1428a1319a06b3ab6a7f513801d8685ed4f82c2f3673554ce903`  
		Last Modified: Thu, 11 Jan 2024 06:29:32 GMT  
		Size: 52.6 MB (52575849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484d11cf87354911d23d11cfbe6aeb7d8a796c9920f28bfe718a82f1eb0e08f7`  
		Last Modified: Thu, 11 Jan 2024 06:29:27 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6998cc50abfc5aaa579705f7cd87e6cc14d1d025f7991c7e1dbda78c001ec6a2`  
		Last Modified: Thu, 11 Jan 2024 06:29:27 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eba36c22e1fbb899a6ef140ff740dd457840b73757d76107d94aabf491822e0`  
		Last Modified: Thu, 11 Jan 2024 06:29:27 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9f8cd437ce7c18dd794ba132faf0160dff5278c64bdde4169d1e83b9ac22d0`  
		Last Modified: Thu, 11 Jan 2024 06:29:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:71ecbc9c195a60c66a1c1c5d5e72e1f9f89f326a186c5df487a6d390eb4b634b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (96007614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe505cc2c2df7063d3f23f30f459e2cf4d44971de8421052bb5248ae2b9936bc`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 11 Jan 2024 02:34:59 GMT
ADD file:577ec786dad9a86344b678e69a7f514c3deede7cc45d9b3c9088449060272d55 in / 
# Thu, 11 Jan 2024 02:35:01 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:30:25 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jan 2024 03:30:27 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 11 Jan 2024 03:30:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:30:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Thu, 11 Jan 2024 03:30:51 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jan 2024 03:31:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:31:09 GMT
ENV COUCHDB_VERSION=3.3.3
# Thu, 11 Jan 2024 03:31:10 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 11 Jan 2024 03:31:36 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 11 Jan 2024 03:31:38 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 11 Jan 2024 03:31:38 GMT
COPY --chown=couchdb:couchdbfile:e5db3ae8229456931b3901d8737d15bbebc21bae345eb60dc63b3edc7a03cfbc in /opt/couchdb/etc/ 
# Thu, 11 Jan 2024 03:31:39 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Thu, 11 Jan 2024 03:31:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 11 Jan 2024 03:31:42 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 03:31:42 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jan 2024 03:31:43 GMT
EXPOSE 4369 5984 9100
# Thu, 11 Jan 2024 03:31:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4c9dbec0f2ecfefcce502a32967ad48a18396e58a4950f972d672b4d95c84bcc`  
		Last Modified: Thu, 11 Jan 2024 02:40:16 GMT  
		Size: 35.3 MB (35293800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d36a93a1206cc85ef8791bb5fc9b1a212ec8f13c65cb09c5f1ea7be2950adf1`  
		Last Modified: Thu, 11 Jan 2024 03:32:21 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f81256de3a18967943f59a0b1b9931dbb8001bcf2650eb267dadbfcdae32db`  
		Last Modified: Thu, 11 Jan 2024 03:32:20 GMT  
		Size: 6.0 MB (6046274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5aab839934ae5028748b84f3ce32b535dd2bd1842bdf0a377ffcce46ef7ffb`  
		Last Modified: Thu, 11 Jan 2024 03:32:19 GMT  
		Size: 662.9 KB (662906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1327c67902d35033bb0c721980f80ddc38d539b101d3bee2bebffae63183c5fa`  
		Last Modified: Thu, 11 Jan 2024 03:32:19 GMT  
		Size: 295.1 KB (295142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04f26b416411093b2df143603fb2c349cdece87315d457850693e112f00fae6`  
		Last Modified: Thu, 11 Jan 2024 03:32:19 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31953ad359289cedf760f9e787681a7a3b1728a525ded248dde4de666d2cad6d`  
		Last Modified: Thu, 11 Jan 2024 03:32:23 GMT  
		Size: 53.7 MB (53701827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d92dfe86aea46604d8224976d0693306b512cbd99dce36276433e917520b32`  
		Last Modified: Thu, 11 Jan 2024 03:32:16 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170c73d485a6ff8254a1741017deb5f288e32f242ec08fa6b8f542eea5b62ae6`  
		Last Modified: Thu, 11 Jan 2024 03:32:16 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7008cbdbbe03281a17f4119708fd6bae79449ace30246a523b2e401e6d80263`  
		Last Modified: Thu, 11 Jan 2024 03:32:16 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda45f47c60cc6c457755c7af4e5c15c9d71c6b77f0372180e382f0fdb3ac28f`  
		Last Modified: Thu, 11 Jan 2024 03:32:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; s390x

```console
$ docker pull couchdb@sha256:f1b4699daea1d64f1162a807185d98928134516adac50d1c139832df8fc34318
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (87021065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85c8be32187ef874de0d68df8b5232f566fe85437349ba9f1794400d0ef8e6b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 11 Jan 2024 01:45:46 GMT
ADD file:77a92d4e9397475a6c68f4341baba607a7c875bc6e252de3e096482dd074f8ca in / 
# Thu, 11 Jan 2024 01:45:49 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 05:56:37 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jan 2024 05:56:37 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 11 Jan 2024 05:56:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:56:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Thu, 11 Jan 2024 05:56:48 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jan 2024 05:56:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:56:54 GMT
ENV COUCHDB_VERSION=3.3.3
# Thu, 11 Jan 2024 05:56:54 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 11 Jan 2024 05:57:15 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 11 Jan 2024 05:57:18 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 11 Jan 2024 05:57:19 GMT
COPY --chown=couchdb:couchdbfile:e5db3ae8229456931b3901d8737d15bbebc21bae345eb60dc63b3edc7a03cfbc in /opt/couchdb/etc/ 
# Thu, 11 Jan 2024 05:57:19 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Thu, 11 Jan 2024 05:57:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 11 Jan 2024 05:57:20 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 05:57:20 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jan 2024 05:57:20 GMT
EXPOSE 4369 5984 9100
# Thu, 11 Jan 2024 05:57:20 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a8470cec8ee9510bf45556c756635d84eb3cbc0220b52812522196008c6b0d3e`  
		Last Modified: Thu, 11 Jan 2024 01:51:19 GMT  
		Size: 29.7 MB (29656884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cefad3d1b84d34933e006ba9b58bd33333046f78e415923952dd253fc6c7a05`  
		Last Modified: Thu, 11 Jan 2024 05:57:37 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08027e0ca2920aeb48561a1f84f07f538b03fdc22067b47aa2c28489cbc4bc25`  
		Last Modified: Thu, 11 Jan 2024 05:57:36 GMT  
		Size: 5.1 MB (5111668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a932b8b14973fd451ccf15fd59d9a2e12a2a4c9915504951dc8d0a455b77404b`  
		Last Modified: Thu, 11 Jan 2024 05:57:36 GMT  
		Size: 573.6 KB (573617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f58653b62bd97148f0cb8b5ece2fe9722fe38b1e1c334616ceec1cfe1dc72d`  
		Last Modified: Thu, 11 Jan 2024 05:57:36 GMT  
		Size: 295.1 KB (295051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd0ef1b80fc30354920b31651370b4007602a3bdf34ab931c15f1ceb28439dd`  
		Last Modified: Thu, 11 Jan 2024 05:57:35 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8deff2a22dc3f942be63a01c98515ff9b1edcc1654b94c9cfa3761ddd480225c`  
		Last Modified: Thu, 11 Jan 2024 05:57:39 GMT  
		Size: 51.4 MB (51376162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c79556934fb3341422637bddebb803ee73da632d7aaf66c6106dbb12bf1206`  
		Last Modified: Thu, 11 Jan 2024 05:57:34 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2590f69e566aefdebef97d238779d67e92af05e0c3646cc76bae3ec8f860c69`  
		Last Modified: Thu, 11 Jan 2024 05:57:34 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e81e97d3824a4dbae238e0a27db0851fb30a479ed4a155a168c79bd747458b`  
		Last Modified: Thu, 11 Jan 2024 05:57:34 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22a12fd5122e216fad215f7fb0fc7d0453135dad4b52ae627cbacc93e218c6c`  
		Last Modified: Thu, 11 Jan 2024 05:57:34 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:f66ace47bc386b53b7c75e3e539d511513564388acf4fbd27d7105d2c82b2bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:0163c3afe1917729214444d3bbd805dcb3680a40558d65acefb2a6b3f15954df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80076729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb6cfc6e5dc4c5298e40f72b885ac71a0b57abcbf91056e1224a60d7101938ea`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:39 GMT
ADD file:08cfc7bf77cc2291c96890f44a435216cb1168c45cef77f7801430982c43ca58 in / 
# Thu, 11 Jan 2024 02:38:39 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 05:33:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jan 2024 05:33:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 11 Jan 2024 05:33:52 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:33:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 11 Jan 2024 05:33:56 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jan 2024 05:34:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:34:02 GMT
ENV COUCHDB_VERSION=3.1.2
# Thu, 11 Jan 2024 05:34:03 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 11 Jan 2024 05:34:17 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 11 Jan 2024 05:34:17 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 11 Jan 2024 05:34:17 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 11 Jan 2024 05:34:17 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Thu, 11 Jan 2024 05:34:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 11 Jan 2024 05:34:18 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 05:34:18 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jan 2024 05:34:18 GMT
EXPOSE 4369 5984 9100
# Thu, 11 Jan 2024 05:34:18 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4648efdf070b378f12737b5cdacaded7b6294f27d0a0c1fb33849090813e920a`  
		Last Modified: Thu, 11 Jan 2024 02:43:48 GMT  
		Size: 27.2 MB (27188221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d912e6f1dd072f57b379a8acbab328980f4a6fd3cea623363042128d604a562f`  
		Last Modified: Thu, 11 Jan 2024 05:35:35 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2694f6780d7e6611967545e415f73b7a3942d57403be7d85893de295d24438`  
		Last Modified: Thu, 11 Jan 2024 05:35:34 GMT  
		Size: 6.7 MB (6704589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a6cb4f83addc4f4e977b984f0200f0b0d27c3aa9b7970fbd3c6947810ef46a`  
		Last Modified: Thu, 11 Jan 2024 05:35:34 GMT  
		Size: 1.3 MB (1259905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b3402a4569e7dcf8682d485597201cfc631d3c1d03789e27e84467bd7a9e60`  
		Last Modified: Thu, 11 Jan 2024 05:35:33 GMT  
		Size: 294.6 KB (294593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:742ee1a8e19917c36acd88c52b092721300c0127274ca8748d22ab9227409153`  
		Last Modified: Thu, 11 Jan 2024 05:35:33 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669f1ae3d8ecb861235af1acf7f5e7653688ae7ea5a9b698f64d01024e44b1c`  
		Last Modified: Thu, 11 Jan 2024 05:35:36 GMT  
		Size: 44.6 MB (44622406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c91ed8174e0ce4cb774ee4afae5df84bc8ddad0e30fb274cce13f760ce0975`  
		Last Modified: Thu, 11 Jan 2024 05:35:31 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952cc8aa37388c5c76e3b98f37334e996a56160e9579ce04e85968c7f2771856`  
		Last Modified: Thu, 11 Jan 2024 05:35:31 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f09ccbd5220a2c1bf3d6e43e74975ff002e51b86b7beeca95a90a9ce2b26081`  
		Last Modified: Thu, 11 Jan 2024 05:35:31 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d84f85b861d5eddafeed6a0e9b1562a8634ed83514ecdac12c9f0426ce1591`  
		Last Modified: Thu, 11 Jan 2024 05:35:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:dd4981369483a912a4f0da3e9323e76e9a099aded11308a0cc2d163abf34c10d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75141133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13f258d0cc33f5ae3422da90f23efa4eea346ff2f649888903ca086d75073cd9`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 11 Jan 2024 02:41:13 GMT
ADD file:0d7c08c3a192fbaded92a14e5eed44f5df7d00cd932ed45984ebb6b6e21446a6 in / 
# Thu, 11 Jan 2024 02:41:13 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:28:30 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jan 2024 06:28:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 11 Jan 2024 06:28:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:28:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 11 Jan 2024 06:28:40 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jan 2024 06:28:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:28:45 GMT
ENV COUCHDB_VERSION=3.1.2
# Thu, 11 Jan 2024 06:28:45 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 11 Jan 2024 06:28:56 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 11 Jan 2024 06:28:57 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 11 Jan 2024 06:28:57 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 11 Jan 2024 06:28:57 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Thu, 11 Jan 2024 06:28:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 11 Jan 2024 06:28:57 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:28:57 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jan 2024 06:28:57 GMT
EXPOSE 4369 5984 9100
# Thu, 11 Jan 2024 06:28:58 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0d982983796daa327ca72ca687e0d8417bb909e8256d666725dae5ad846525ae`  
		Last Modified: Thu, 11 Jan 2024 02:45:24 GMT  
		Size: 26.0 MB (25969811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:045ae2b1301e0d4d902919f14ba0c2bdc42e0d49d80bf85546fbd245fe277883`  
		Last Modified: Thu, 11 Jan 2024 06:29:49 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19038a383fdabf47d56e07f75f86e36846e9757af76e450123327dc0d8017f8`  
		Last Modified: Thu, 11 Jan 2024 06:29:48 GMT  
		Size: 6.6 MB (6577588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b5bd25881dbfc612b64ae1b149a3d60568a830051bc583b6aead0e836ba1cec`  
		Last Modified: Thu, 11 Jan 2024 06:29:47 GMT  
		Size: 1.2 MB (1164775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d09863cad54994cd662045e95b2f2adea079ff9bbf8e1f4c89f9d4ef9411a0`  
		Last Modified: Thu, 11 Jan 2024 06:29:47 GMT  
		Size: 294.4 KB (294381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319a92c1d8705eaaae2914483f0843e739ff8fe120d4eb7cf7ba55c971b020ae`  
		Last Modified: Thu, 11 Jan 2024 06:29:46 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd250963835ab6de39671e39af53cc8a8064428b0c0a639c84b56046685c04c`  
		Last Modified: Thu, 11 Jan 2024 06:29:50 GMT  
		Size: 41.1 MB (41127548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc5eb4e021b777c1a5c5b55aaf58a7fe228e8debf3943750639c9c4cc51735b`  
		Last Modified: Thu, 11 Jan 2024 06:29:45 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1eb8622e9cca3579ad19a61031179b3ef541ea4e23005ad3a208e36bba540cb`  
		Last Modified: Thu, 11 Jan 2024 06:29:44 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98aab8d88bede520b2bf2e1824168fe3439011346a2bcdc9f4a2b38c3f12fa2e`  
		Last Modified: Thu, 11 Jan 2024 06:29:44 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c70ae77ec5ac5a6a7b44472d84cf7cf8c3f44700f815485e2488aa14f2ff2d6`  
		Last Modified: Thu, 11 Jan 2024 06:29:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1.2`

```console
$ docker pull couchdb@sha256:f66ace47bc386b53b7c75e3e539d511513564388acf4fbd27d7105d2c82b2bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1.2` - linux; amd64

```console
$ docker pull couchdb@sha256:0163c3afe1917729214444d3bbd805dcb3680a40558d65acefb2a6b3f15954df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80076729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb6cfc6e5dc4c5298e40f72b885ac71a0b57abcbf91056e1224a60d7101938ea`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:39 GMT
ADD file:08cfc7bf77cc2291c96890f44a435216cb1168c45cef77f7801430982c43ca58 in / 
# Thu, 11 Jan 2024 02:38:39 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 05:33:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jan 2024 05:33:43 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 11 Jan 2024 05:33:52 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:33:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 11 Jan 2024 05:33:56 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jan 2024 05:34:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:34:02 GMT
ENV COUCHDB_VERSION=3.1.2
# Thu, 11 Jan 2024 05:34:03 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 11 Jan 2024 05:34:17 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 11 Jan 2024 05:34:17 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 11 Jan 2024 05:34:17 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 11 Jan 2024 05:34:17 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Thu, 11 Jan 2024 05:34:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 11 Jan 2024 05:34:18 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 05:34:18 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jan 2024 05:34:18 GMT
EXPOSE 4369 5984 9100
# Thu, 11 Jan 2024 05:34:18 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4648efdf070b378f12737b5cdacaded7b6294f27d0a0c1fb33849090813e920a`  
		Last Modified: Thu, 11 Jan 2024 02:43:48 GMT  
		Size: 27.2 MB (27188221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d912e6f1dd072f57b379a8acbab328980f4a6fd3cea623363042128d604a562f`  
		Last Modified: Thu, 11 Jan 2024 05:35:35 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2694f6780d7e6611967545e415f73b7a3942d57403be7d85893de295d24438`  
		Last Modified: Thu, 11 Jan 2024 05:35:34 GMT  
		Size: 6.7 MB (6704589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a6cb4f83addc4f4e977b984f0200f0b0d27c3aa9b7970fbd3c6947810ef46a`  
		Last Modified: Thu, 11 Jan 2024 05:35:34 GMT  
		Size: 1.3 MB (1259905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b3402a4569e7dcf8682d485597201cfc631d3c1d03789e27e84467bd7a9e60`  
		Last Modified: Thu, 11 Jan 2024 05:35:33 GMT  
		Size: 294.6 KB (294593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:742ee1a8e19917c36acd88c52b092721300c0127274ca8748d22ab9227409153`  
		Last Modified: Thu, 11 Jan 2024 05:35:33 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b669f1ae3d8ecb861235af1acf7f5e7653688ae7ea5a9b698f64d01024e44b1c`  
		Last Modified: Thu, 11 Jan 2024 05:35:36 GMT  
		Size: 44.6 MB (44622406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c91ed8174e0ce4cb774ee4afae5df84bc8ddad0e30fb274cce13f760ce0975`  
		Last Modified: Thu, 11 Jan 2024 05:35:31 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952cc8aa37388c5c76e3b98f37334e996a56160e9579ce04e85968c7f2771856`  
		Last Modified: Thu, 11 Jan 2024 05:35:31 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f09ccbd5220a2c1bf3d6e43e74975ff002e51b86b7beeca95a90a9ce2b26081`  
		Last Modified: Thu, 11 Jan 2024 05:35:31 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d84f85b861d5eddafeed6a0e9b1562a8634ed83514ecdac12c9f0426ce1591`  
		Last Modified: Thu, 11 Jan 2024 05:35:31 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:dd4981369483a912a4f0da3e9323e76e9a099aded11308a0cc2d163abf34c10d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75141133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13f258d0cc33f5ae3422da90f23efa4eea346ff2f649888903ca086d75073cd9`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 11 Jan 2024 02:41:13 GMT
ADD file:0d7c08c3a192fbaded92a14e5eed44f5df7d00cd932ed45984ebb6b6e21446a6 in / 
# Thu, 11 Jan 2024 02:41:13 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:28:30 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jan 2024 06:28:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 11 Jan 2024 06:28:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:28:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 11 Jan 2024 06:28:40 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jan 2024 06:28:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:28:45 GMT
ENV COUCHDB_VERSION=3.1.2
# Thu, 11 Jan 2024 06:28:45 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 11 Jan 2024 06:28:56 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 11 Jan 2024 06:28:57 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 11 Jan 2024 06:28:57 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 11 Jan 2024 06:28:57 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Thu, 11 Jan 2024 06:28:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 11 Jan 2024 06:28:57 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:28:57 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jan 2024 06:28:57 GMT
EXPOSE 4369 5984 9100
# Thu, 11 Jan 2024 06:28:58 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0d982983796daa327ca72ca687e0d8417bb909e8256d666725dae5ad846525ae`  
		Last Modified: Thu, 11 Jan 2024 02:45:24 GMT  
		Size: 26.0 MB (25969811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:045ae2b1301e0d4d902919f14ba0c2bdc42e0d49d80bf85546fbd245fe277883`  
		Last Modified: Thu, 11 Jan 2024 06:29:49 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19038a383fdabf47d56e07f75f86e36846e9757af76e450123327dc0d8017f8`  
		Last Modified: Thu, 11 Jan 2024 06:29:48 GMT  
		Size: 6.6 MB (6577588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b5bd25881dbfc612b64ae1b149a3d60568a830051bc583b6aead0e836ba1cec`  
		Last Modified: Thu, 11 Jan 2024 06:29:47 GMT  
		Size: 1.2 MB (1164775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d09863cad54994cd662045e95b2f2adea079ff9bbf8e1f4c89f9d4ef9411a0`  
		Last Modified: Thu, 11 Jan 2024 06:29:47 GMT  
		Size: 294.4 KB (294381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319a92c1d8705eaaae2914483f0843e739ff8fe120d4eb7cf7ba55c971b020ae`  
		Last Modified: Thu, 11 Jan 2024 06:29:46 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd250963835ab6de39671e39af53cc8a8064428b0c0a639c84b56046685c04c`  
		Last Modified: Thu, 11 Jan 2024 06:29:50 GMT  
		Size: 41.1 MB (41127548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc5eb4e021b777c1a5c5b55aaf58a7fe228e8debf3943750639c9c4cc51735b`  
		Last Modified: Thu, 11 Jan 2024 06:29:45 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1eb8622e9cca3579ad19a61031179b3ef541ea4e23005ad3a208e36bba540cb`  
		Last Modified: Thu, 11 Jan 2024 06:29:44 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98aab8d88bede520b2bf2e1824168fe3439011346a2bcdc9f4a2b38c3f12fa2e`  
		Last Modified: Thu, 11 Jan 2024 06:29:44 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c70ae77ec5ac5a6a7b44472d84cf7cf8c3f44700f815485e2488aa14f2ff2d6`  
		Last Modified: Thu, 11 Jan 2024 06:29:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2`

```console
$ docker pull couchdb@sha256:aad569a8fbcc50e172ca067978c561a72c7cee3d5118b92c7c07762d14a3f536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:68dacc08e4745d45a3d2e45b85432d077b79e628e05a70bdc73858a72c3b86c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89747520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4df4d85a8e0a1fc56eb609aa0dba891c46dd6ee448a63774c98a096060abb73`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 05:32:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jan 2024 05:32:52 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 11 Jan 2024 05:32:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:33:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Thu, 11 Jan 2024 05:33:02 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jan 2024 05:33:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:33:26 GMT
ENV COUCHDB_VERSION=3.2.3
# Thu, 11 Jan 2024 05:33:26 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 11 Jan 2024 05:33:39 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 11 Jan 2024 05:33:39 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 11 Jan 2024 05:33:39 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Thu, 11 Jan 2024 05:33:39 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Thu, 11 Jan 2024 05:33:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 11 Jan 2024 05:33:40 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 05:33:40 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jan 2024 05:33:40 GMT
EXPOSE 4369 5984 9100
# Thu, 11 Jan 2024 05:33:40 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfeb8d6d7cb9ec479de9e07297a4472878669f03cdc566d5ba2bdf49121cdbd`  
		Last Modified: Thu, 11 Jan 2024 05:35:00 GMT  
		Size: 3.4 KB (3410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7ac1349877a8205b90d6e6d1ef8cfa4d201f84fc189f8655d5e0525c735ee0`  
		Last Modified: Thu, 11 Jan 2024 05:34:59 GMT  
		Size: 5.2 MB (5226552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efbad6a63f2382da1e97c8d1dc6a5cb77899556bbd8fad2aaf8dd66b2ce00604`  
		Last Modified: Thu, 11 Jan 2024 05:34:58 GMT  
		Size: 610.9 KB (610908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227a8bbc783b3bd4eeed204844a79a51702307ae9b08da4ae1a162f142c48334`  
		Last Modified: Thu, 11 Jan 2024 05:34:58 GMT  
		Size: 295.1 KB (295133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a69f1f53b5a86bcdc181cbd98ef0b37b7c89d0de44d28e04a2f7fd32c0a7487`  
		Last Modified: Thu, 11 Jan 2024 05:35:19 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82920941dbef8197136d527195743b1b5be50e0be79acb1fe72ef0eb46de538a`  
		Last Modified: Thu, 11 Jan 2024 05:35:23 GMT  
		Size: 52.2 MB (52189559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df11f57a3a1031921d4703ae53ce478a4abb0b1f9d680684b05068fee497b2bd`  
		Last Modified: Thu, 11 Jan 2024 05:35:17 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c17550da1fa703daf2bfd723604390b6446ae1045b36e08c6d93ebd05281d4`  
		Last Modified: Thu, 11 Jan 2024 05:35:17 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2afac0974f51ebd15ca344bd69a4a8c51a31b013d9848076014d2e211de74a93`  
		Last Modified: Thu, 11 Jan 2024 05:35:17 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e23ec2aa70aeee0ee1d4134f7b011ef7f3efa07567c50e91bba892771d850f`  
		Last Modified: Thu, 11 Jan 2024 05:35:17 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:960305e9b35826163f173e8b89eab4112410bee3725c3f0773140932dd9f7877
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.2 MB (85205205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352add31bc606968e9b4695dc003a06de6c7ca3682ea0d3145b972feb8dabfee`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:49 GMT
ADD file:7b3c55926db26568f849247e80abdec3cfd6642929a40f0bbee95e4cb176051e in / 
# Wed, 12 Apr 2023 00:39:49 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:33:39 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 12 Apr 2023 01:33:39 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 12 Apr 2023 01:33:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:33:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 12 Apr 2023 01:33:48 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 12 Apr 2023 01:33:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:34:12 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Wed, 12 Apr 2023 01:34:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 12 Apr 2023 01:34:24 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 12 Apr 2023 01:34:24 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 12 Apr 2023 01:34:24 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 12 Apr 2023 01:34:24 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 12 Apr 2023 01:34:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 12 Apr 2023 01:34:25 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 12 Apr 2023 01:34:25 GMT
VOLUME [/opt/couchdb/data]
# Wed, 12 Apr 2023 01:34:25 GMT
EXPOSE 4369 5984 9100
# Wed, 12 Apr 2023 01:34:25 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ebc3dc5a2d72427c585c8cda7574a75d96e04b9a37572bd3af0bff905abefbb9`  
		Last Modified: Wed, 12 Apr 2023 00:42:35 GMT  
		Size: 30.1 MB (30063826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f522824805b9b3818de882a514dd5454399e3c21b512a09e64274bf12d18ab4`  
		Last Modified: Wed, 12 Apr 2023 01:35:29 GMT  
		Size: 3.4 KB (3434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fdfaf598c101b0427a73a7b5a1edb3b6229985b64794e6d215eb049125bbd25`  
		Last Modified: Wed, 12 Apr 2023 01:35:27 GMT  
		Size: 5.2 MB (5209561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc33796685833f0fdacecb6c4f2078915729822d8fb7a21aada1b767c48b377`  
		Last Modified: Wed, 12 Apr 2023 01:35:27 GMT  
		Size: 566.3 KB (566295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356323e70f7127294f4bee19c211582a4af79acc6d1f696d70fc94229c84aa52`  
		Last Modified: Wed, 12 Apr 2023 01:35:27 GMT  
		Size: 294.3 KB (294328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9652526d42f149093060de62ac3b39905fb0bfb8457d6148e4314ef71058a153`  
		Last Modified: Wed, 12 Apr 2023 01:35:44 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d95be693dac094ea4fe70ff2bd1f44b66a9ede007474a31cafcb829c361429`  
		Last Modified: Wed, 12 Apr 2023 01:35:47 GMT  
		Size: 49.1 MB (49063995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61eb7f6826c8440901fb275f2b3c5f6be3e97d95482db6770215d5bd31899ed1`  
		Last Modified: Wed, 12 Apr 2023 01:35:42 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d81fa00cdd93053287b1afda2f3cfda4475c6ac6307dc22125a76f843f21415`  
		Last Modified: Wed, 12 Apr 2023 01:35:43 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e726b19dd008ea8df7bf3ce90fa1947f685d2f6fdd3caa36e1f3b6e40526d0`  
		Last Modified: Wed, 12 Apr 2023 01:35:43 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c78146fce98da16e884fde6d22f444849c69c3da90555e336827ceb2b6a039`  
		Last Modified: Wed, 12 Apr 2023 01:35:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2` - linux; ppc64le

```console
$ docker pull couchdb@sha256:90a95123b16f3f08c9e3b862a7e628ead429c8602d5dc110db1b038b5b47db9f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.4 MB (92383985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c0714b286e5789d8b829c846536d1f8a5308d8cf419fa60995af8b91ab3b55`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 12 Apr 2023 00:08:20 GMT
ADD file:63eb52aaff02c15bceabb87a78eb1b36389066ff4774cf8a754160ca7d509816 in / 
# Wed, 12 Apr 2023 00:08:23 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:23:31 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 12 Apr 2023 01:23:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 12 Apr 2023 01:23:57 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:24:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 12 Apr 2023 01:24:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 12 Apr 2023 01:24:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:25:25 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Wed, 12 Apr 2023 01:25:27 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 12 Apr 2023 01:25:58 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 12 Apr 2023 01:26:02 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 12 Apr 2023 01:26:02 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 12 Apr 2023 01:26:03 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 12 Apr 2023 01:26:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 12 Apr 2023 01:26:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 12 Apr 2023 01:26:06 GMT
VOLUME [/opt/couchdb/data]
# Wed, 12 Apr 2023 01:26:06 GMT
EXPOSE 4369 5984 9100
# Wed, 12 Apr 2023 01:26:07 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5b41d5ec640939cf684959234ad3b80909268a32bfd520a31c6720a91521c2fa`  
		Last Modified: Wed, 12 Apr 2023 00:13:13 GMT  
		Size: 35.3 MB (35291995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7569dcea363c11bb071b416ea27193dbe62d8a210fa1f829efabb35b46600dae`  
		Last Modified: Wed, 12 Apr 2023 01:26:25 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a685c575c0e899abc0410edf84715dd5cf4184fcbd447fdbbcac069795eadd05`  
		Last Modified: Wed, 12 Apr 2023 01:26:26 GMT  
		Size: 6.0 MB (6044117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0283a2882808914c7a35f392d4ad2d2921ccf8b8855ab399e2998c22d061f16e`  
		Last Modified: Wed, 12 Apr 2023 01:26:24 GMT  
		Size: 662.1 KB (662116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17deb4c48f5c43beee592bed99d27502afe8c8f60cde1cb4bebb7dce00e877c`  
		Last Modified: Wed, 12 Apr 2023 01:26:24 GMT  
		Size: 294.3 KB (294319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7661a9384c6767a073bc8e86df2ec2c60bef8bad55fac7ab22d7ecffcdb1f1`  
		Last Modified: Wed, 12 Apr 2023 01:26:48 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74733b44093de42db86284861068e909838a6bca4f3ecf0bfd04eb99d5bf8c79`  
		Last Modified: Wed, 12 Apr 2023 01:26:56 GMT  
		Size: 50.1 MB (50084252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c567dbfb6ac3167b1cd2d6532940fd6fb66d9b5b6a1dedf22d61b92a7b4095eb`  
		Last Modified: Wed, 12 Apr 2023 01:26:46 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf08299e06354b4674e5fabd7e99da65832d26bc98826c051d261e7a03195099`  
		Last Modified: Wed, 12 Apr 2023 01:26:46 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5861e0f3152c23eda58111aaac02f82ed4973711f9a55c51cb55ebb9af6220`  
		Last Modified: Wed, 12 Apr 2023 01:26:46 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54774512e47b4b9a6dee9f79bf7ec483b3c7c234e949bc4f6c96fb22a3e8237`  
		Last Modified: Wed, 12 Apr 2023 01:26:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2.3`

```console
$ docker pull couchdb@sha256:ce6d4adabdeeafea2302cf84d2998107b18ea3c17846b8996f1c7f984a906ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchdb:3.2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:68dacc08e4745d45a3d2e45b85432d077b79e628e05a70bdc73858a72c3b86c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89747520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4df4d85a8e0a1fc56eb609aa0dba891c46dd6ee448a63774c98a096060abb73`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 05:32:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jan 2024 05:32:52 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 11 Jan 2024 05:32:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:33:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Thu, 11 Jan 2024 05:33:02 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jan 2024 05:33:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:33:26 GMT
ENV COUCHDB_VERSION=3.2.3
# Thu, 11 Jan 2024 05:33:26 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 11 Jan 2024 05:33:39 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 11 Jan 2024 05:33:39 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 11 Jan 2024 05:33:39 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Thu, 11 Jan 2024 05:33:39 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Thu, 11 Jan 2024 05:33:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 11 Jan 2024 05:33:40 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 05:33:40 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jan 2024 05:33:40 GMT
EXPOSE 4369 5984 9100
# Thu, 11 Jan 2024 05:33:40 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfeb8d6d7cb9ec479de9e07297a4472878669f03cdc566d5ba2bdf49121cdbd`  
		Last Modified: Thu, 11 Jan 2024 05:35:00 GMT  
		Size: 3.4 KB (3410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7ac1349877a8205b90d6e6d1ef8cfa4d201f84fc189f8655d5e0525c735ee0`  
		Last Modified: Thu, 11 Jan 2024 05:34:59 GMT  
		Size: 5.2 MB (5226552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efbad6a63f2382da1e97c8d1dc6a5cb77899556bbd8fad2aaf8dd66b2ce00604`  
		Last Modified: Thu, 11 Jan 2024 05:34:58 GMT  
		Size: 610.9 KB (610908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227a8bbc783b3bd4eeed204844a79a51702307ae9b08da4ae1a162f142c48334`  
		Last Modified: Thu, 11 Jan 2024 05:34:58 GMT  
		Size: 295.1 KB (295133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a69f1f53b5a86bcdc181cbd98ef0b37b7c89d0de44d28e04a2f7fd32c0a7487`  
		Last Modified: Thu, 11 Jan 2024 05:35:19 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82920941dbef8197136d527195743b1b5be50e0be79acb1fe72ef0eb46de538a`  
		Last Modified: Thu, 11 Jan 2024 05:35:23 GMT  
		Size: 52.2 MB (52189559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df11f57a3a1031921d4703ae53ce478a4abb0b1f9d680684b05068fee497b2bd`  
		Last Modified: Thu, 11 Jan 2024 05:35:17 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c17550da1fa703daf2bfd723604390b6446ae1045b36e08c6d93ebd05281d4`  
		Last Modified: Thu, 11 Jan 2024 05:35:17 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2afac0974f51ebd15ca344bd69a4a8c51a31b013d9848076014d2e211de74a93`  
		Last Modified: Thu, 11 Jan 2024 05:35:17 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e23ec2aa70aeee0ee1d4134f7b011ef7f3efa07567c50e91bba892771d850f`  
		Last Modified: Thu, 11 Jan 2024 05:35:17 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.3`

```console
$ docker pull couchdb@sha256:d684daac1e11c90df0f4ae9f5cc9866b198d03d1b636867741992b12f2dfeeb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `couchdb:3.3` - linux; amd64

```console
$ docker pull couchdb@sha256:94eae1e4891cab1426c43e968258c444a9e4ec711b8d6e80dd19a11e48b56910
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.3 MB (90282155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ba54687bbde594dc5a12c99a6a7228ec9bd8140c9aeaf68d61103a8412dea7`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 05:32:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jan 2024 05:32:52 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 11 Jan 2024 05:32:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:33:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Thu, 11 Jan 2024 05:33:02 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jan 2024 05:33:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:33:08 GMT
ENV COUCHDB_VERSION=3.3.3
# Thu, 11 Jan 2024 05:33:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 11 Jan 2024 05:33:21 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 11 Jan 2024 05:33:21 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 11 Jan 2024 05:33:21 GMT
COPY --chown=couchdb:couchdbfile:e5db3ae8229456931b3901d8737d15bbebc21bae345eb60dc63b3edc7a03cfbc in /opt/couchdb/etc/ 
# Thu, 11 Jan 2024 05:33:21 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Thu, 11 Jan 2024 05:33:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 11 Jan 2024 05:33:22 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 05:33:22 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jan 2024 05:33:22 GMT
EXPOSE 4369 5984 9100
# Thu, 11 Jan 2024 05:33:22 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfeb8d6d7cb9ec479de9e07297a4472878669f03cdc566d5ba2bdf49121cdbd`  
		Last Modified: Thu, 11 Jan 2024 05:35:00 GMT  
		Size: 3.4 KB (3410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7ac1349877a8205b90d6e6d1ef8cfa4d201f84fc189f8655d5e0525c735ee0`  
		Last Modified: Thu, 11 Jan 2024 05:34:59 GMT  
		Size: 5.2 MB (5226552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efbad6a63f2382da1e97c8d1dc6a5cb77899556bbd8fad2aaf8dd66b2ce00604`  
		Last Modified: Thu, 11 Jan 2024 05:34:58 GMT  
		Size: 610.9 KB (610908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227a8bbc783b3bd4eeed204844a79a51702307ae9b08da4ae1a162f142c48334`  
		Last Modified: Thu, 11 Jan 2024 05:34:58 GMT  
		Size: 295.1 KB (295133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3baadb6b9da90e40a0a57037da3b6e96d8599c58eff15ec5a6708bd0df6ab197`  
		Last Modified: Thu, 11 Jan 2024 05:34:58 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b705d298942cad7478031a63b4dc673d7d112dd13144ca0f6b4a85cf1c2318ec`  
		Last Modified: Thu, 11 Jan 2024 05:35:02 GMT  
		Size: 52.7 MB (52723949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a7281945f13c96bd64bdd2151029ecdd55723a1d6b57b9a88cc787f00c3f4f`  
		Last Modified: Thu, 11 Jan 2024 05:34:56 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7595f19c0256c9fbc059ca171d4909f09e648811bf4a86e74eff51cf29319477`  
		Last Modified: Thu, 11 Jan 2024 05:34:56 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8224f3b72b8930d3657822dcad3731868ebeeca1815bba4374e1c06824dc3133`  
		Last Modified: Thu, 11 Jan 2024 05:34:56 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a4cce3951e5070185c31edf9e8b96bc1b2fef875581f66f76059c20cbee6218`  
		Last Modified: Thu, 11 Jan 2024 05:34:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:8186dcf53c5964afdb14024925e7aa13e71e9f22b665cbbe926e80bc1d828503
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88720355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4daaa9a74f3ce7fabf84b8351b56756ad504ca89ed84a6bddf6a42e63d2675bd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:27:45 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jan 2024 06:27:46 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 11 Jan 2024 06:27:52 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:27:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Thu, 11 Jan 2024 06:27:54 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jan 2024 06:27:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:27:59 GMT
ENV COUCHDB_VERSION=3.3.3
# Thu, 11 Jan 2024 06:27:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 11 Jan 2024 06:28:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 11 Jan 2024 06:28:11 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 11 Jan 2024 06:28:11 GMT
COPY --chown=couchdb:couchdbfile:e5db3ae8229456931b3901d8737d15bbebc21bae345eb60dc63b3edc7a03cfbc in /opt/couchdb/etc/ 
# Thu, 11 Jan 2024 06:28:11 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Thu, 11 Jan 2024 06:28:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 11 Jan 2024 06:28:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:28:12 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jan 2024 06:28:12 GMT
EXPOSE 4369 5984 9100
# Thu, 11 Jan 2024 06:28:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ccc2078107ccc438fcb3b557ed215d440cd15f6f1879ad9db9f9b84b6946ac2`  
		Last Modified: Thu, 11 Jan 2024 06:29:31 GMT  
		Size: 3.4 KB (3433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562c17c5f419b97b03f49e7bed7c8cfd4d92ba18af2b014b62eb052a179e63ac`  
		Last Modified: Thu, 11 Jan 2024 06:29:30 GMT  
		Size: 5.2 MB (5210746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0a74a2782d1ffc7d869c33ab658ff80a6d3cfcd8903731d2b6b85bce269f3a`  
		Last Modified: Thu, 11 Jan 2024 06:29:29 GMT  
		Size: 567.1 KB (567052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d92f4c25743b8992888f53be6782574bfbbfd772cc684706e5b48a64335287`  
		Last Modified: Thu, 11 Jan 2024 06:29:29 GMT  
		Size: 295.0 KB (295014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fdc8f03011aa4022b246fe0407ba7262723f0241e4cd3d25a21dff79bfb5a38`  
		Last Modified: Thu, 11 Jan 2024 06:29:29 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526e7e3d442f1428a1319a06b3ab6a7f513801d8685ed4f82c2f3673554ce903`  
		Last Modified: Thu, 11 Jan 2024 06:29:32 GMT  
		Size: 52.6 MB (52575849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484d11cf87354911d23d11cfbe6aeb7d8a796c9920f28bfe718a82f1eb0e08f7`  
		Last Modified: Thu, 11 Jan 2024 06:29:27 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6998cc50abfc5aaa579705f7cd87e6cc14d1d025f7991c7e1dbda78c001ec6a2`  
		Last Modified: Thu, 11 Jan 2024 06:29:27 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eba36c22e1fbb899a6ef140ff740dd457840b73757d76107d94aabf491822e0`  
		Last Modified: Thu, 11 Jan 2024 06:29:27 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9f8cd437ce7c18dd794ba132faf0160dff5278c64bdde4169d1e83b9ac22d0`  
		Last Modified: Thu, 11 Jan 2024 06:29:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:71ecbc9c195a60c66a1c1c5d5e72e1f9f89f326a186c5df487a6d390eb4b634b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (96007614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe505cc2c2df7063d3f23f30f459e2cf4d44971de8421052bb5248ae2b9936bc`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 11 Jan 2024 02:34:59 GMT
ADD file:577ec786dad9a86344b678e69a7f514c3deede7cc45d9b3c9088449060272d55 in / 
# Thu, 11 Jan 2024 02:35:01 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:30:25 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jan 2024 03:30:27 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 11 Jan 2024 03:30:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:30:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Thu, 11 Jan 2024 03:30:51 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jan 2024 03:31:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:31:09 GMT
ENV COUCHDB_VERSION=3.3.3
# Thu, 11 Jan 2024 03:31:10 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 11 Jan 2024 03:31:36 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 11 Jan 2024 03:31:38 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 11 Jan 2024 03:31:38 GMT
COPY --chown=couchdb:couchdbfile:e5db3ae8229456931b3901d8737d15bbebc21bae345eb60dc63b3edc7a03cfbc in /opt/couchdb/etc/ 
# Thu, 11 Jan 2024 03:31:39 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Thu, 11 Jan 2024 03:31:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 11 Jan 2024 03:31:42 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 03:31:42 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jan 2024 03:31:43 GMT
EXPOSE 4369 5984 9100
# Thu, 11 Jan 2024 03:31:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4c9dbec0f2ecfefcce502a32967ad48a18396e58a4950f972d672b4d95c84bcc`  
		Last Modified: Thu, 11 Jan 2024 02:40:16 GMT  
		Size: 35.3 MB (35293800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d36a93a1206cc85ef8791bb5fc9b1a212ec8f13c65cb09c5f1ea7be2950adf1`  
		Last Modified: Thu, 11 Jan 2024 03:32:21 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f81256de3a18967943f59a0b1b9931dbb8001bcf2650eb267dadbfcdae32db`  
		Last Modified: Thu, 11 Jan 2024 03:32:20 GMT  
		Size: 6.0 MB (6046274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5aab839934ae5028748b84f3ce32b535dd2bd1842bdf0a377ffcce46ef7ffb`  
		Last Modified: Thu, 11 Jan 2024 03:32:19 GMT  
		Size: 662.9 KB (662906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1327c67902d35033bb0c721980f80ddc38d539b101d3bee2bebffae63183c5fa`  
		Last Modified: Thu, 11 Jan 2024 03:32:19 GMT  
		Size: 295.1 KB (295142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04f26b416411093b2df143603fb2c349cdece87315d457850693e112f00fae6`  
		Last Modified: Thu, 11 Jan 2024 03:32:19 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31953ad359289cedf760f9e787681a7a3b1728a525ded248dde4de666d2cad6d`  
		Last Modified: Thu, 11 Jan 2024 03:32:23 GMT  
		Size: 53.7 MB (53701827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d92dfe86aea46604d8224976d0693306b512cbd99dce36276433e917520b32`  
		Last Modified: Thu, 11 Jan 2024 03:32:16 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170c73d485a6ff8254a1741017deb5f288e32f242ec08fa6b8f542eea5b62ae6`  
		Last Modified: Thu, 11 Jan 2024 03:32:16 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7008cbdbbe03281a17f4119708fd6bae79449ace30246a523b2e401e6d80263`  
		Last Modified: Thu, 11 Jan 2024 03:32:16 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda45f47c60cc6c457755c7af4e5c15c9d71c6b77f0372180e382f0fdb3ac28f`  
		Last Modified: Thu, 11 Jan 2024 03:32:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3` - linux; s390x

```console
$ docker pull couchdb@sha256:f1b4699daea1d64f1162a807185d98928134516adac50d1c139832df8fc34318
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (87021065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85c8be32187ef874de0d68df8b5232f566fe85437349ba9f1794400d0ef8e6b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 11 Jan 2024 01:45:46 GMT
ADD file:77a92d4e9397475a6c68f4341baba607a7c875bc6e252de3e096482dd074f8ca in / 
# Thu, 11 Jan 2024 01:45:49 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 05:56:37 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jan 2024 05:56:37 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 11 Jan 2024 05:56:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:56:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Thu, 11 Jan 2024 05:56:48 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jan 2024 05:56:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:56:54 GMT
ENV COUCHDB_VERSION=3.3.3
# Thu, 11 Jan 2024 05:56:54 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 11 Jan 2024 05:57:15 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 11 Jan 2024 05:57:18 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 11 Jan 2024 05:57:19 GMT
COPY --chown=couchdb:couchdbfile:e5db3ae8229456931b3901d8737d15bbebc21bae345eb60dc63b3edc7a03cfbc in /opt/couchdb/etc/ 
# Thu, 11 Jan 2024 05:57:19 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Thu, 11 Jan 2024 05:57:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 11 Jan 2024 05:57:20 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 05:57:20 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jan 2024 05:57:20 GMT
EXPOSE 4369 5984 9100
# Thu, 11 Jan 2024 05:57:20 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a8470cec8ee9510bf45556c756635d84eb3cbc0220b52812522196008c6b0d3e`  
		Last Modified: Thu, 11 Jan 2024 01:51:19 GMT  
		Size: 29.7 MB (29656884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cefad3d1b84d34933e006ba9b58bd33333046f78e415923952dd253fc6c7a05`  
		Last Modified: Thu, 11 Jan 2024 05:57:37 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08027e0ca2920aeb48561a1f84f07f538b03fdc22067b47aa2c28489cbc4bc25`  
		Last Modified: Thu, 11 Jan 2024 05:57:36 GMT  
		Size: 5.1 MB (5111668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a932b8b14973fd451ccf15fd59d9a2e12a2a4c9915504951dc8d0a455b77404b`  
		Last Modified: Thu, 11 Jan 2024 05:57:36 GMT  
		Size: 573.6 KB (573617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f58653b62bd97148f0cb8b5ece2fe9722fe38b1e1c334616ceec1cfe1dc72d`  
		Last Modified: Thu, 11 Jan 2024 05:57:36 GMT  
		Size: 295.1 KB (295051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd0ef1b80fc30354920b31651370b4007602a3bdf34ab931c15f1ceb28439dd`  
		Last Modified: Thu, 11 Jan 2024 05:57:35 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8deff2a22dc3f942be63a01c98515ff9b1edcc1654b94c9cfa3761ddd480225c`  
		Last Modified: Thu, 11 Jan 2024 05:57:39 GMT  
		Size: 51.4 MB (51376162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c79556934fb3341422637bddebb803ee73da632d7aaf66c6106dbb12bf1206`  
		Last Modified: Thu, 11 Jan 2024 05:57:34 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2590f69e566aefdebef97d238779d67e92af05e0c3646cc76bae3ec8f860c69`  
		Last Modified: Thu, 11 Jan 2024 05:57:34 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e81e97d3824a4dbae238e0a27db0851fb30a479ed4a155a168c79bd747458b`  
		Last Modified: Thu, 11 Jan 2024 05:57:34 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22a12fd5122e216fad215f7fb0fc7d0453135dad4b52ae627cbacc93e218c6c`  
		Last Modified: Thu, 11 Jan 2024 05:57:34 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.3.3`

```console
$ docker pull couchdb@sha256:d684daac1e11c90df0f4ae9f5cc9866b198d03d1b636867741992b12f2dfeeb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `couchdb:3.3.3` - linux; amd64

```console
$ docker pull couchdb@sha256:94eae1e4891cab1426c43e968258c444a9e4ec711b8d6e80dd19a11e48b56910
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.3 MB (90282155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ba54687bbde594dc5a12c99a6a7228ec9bd8140c9aeaf68d61103a8412dea7`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 05:32:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jan 2024 05:32:52 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 11 Jan 2024 05:32:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:33:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Thu, 11 Jan 2024 05:33:02 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jan 2024 05:33:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:33:08 GMT
ENV COUCHDB_VERSION=3.3.3
# Thu, 11 Jan 2024 05:33:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 11 Jan 2024 05:33:21 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 11 Jan 2024 05:33:21 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 11 Jan 2024 05:33:21 GMT
COPY --chown=couchdb:couchdbfile:e5db3ae8229456931b3901d8737d15bbebc21bae345eb60dc63b3edc7a03cfbc in /opt/couchdb/etc/ 
# Thu, 11 Jan 2024 05:33:21 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Thu, 11 Jan 2024 05:33:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 11 Jan 2024 05:33:22 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 05:33:22 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jan 2024 05:33:22 GMT
EXPOSE 4369 5984 9100
# Thu, 11 Jan 2024 05:33:22 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfeb8d6d7cb9ec479de9e07297a4472878669f03cdc566d5ba2bdf49121cdbd`  
		Last Modified: Thu, 11 Jan 2024 05:35:00 GMT  
		Size: 3.4 KB (3410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7ac1349877a8205b90d6e6d1ef8cfa4d201f84fc189f8655d5e0525c735ee0`  
		Last Modified: Thu, 11 Jan 2024 05:34:59 GMT  
		Size: 5.2 MB (5226552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efbad6a63f2382da1e97c8d1dc6a5cb77899556bbd8fad2aaf8dd66b2ce00604`  
		Last Modified: Thu, 11 Jan 2024 05:34:58 GMT  
		Size: 610.9 KB (610908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227a8bbc783b3bd4eeed204844a79a51702307ae9b08da4ae1a162f142c48334`  
		Last Modified: Thu, 11 Jan 2024 05:34:58 GMT  
		Size: 295.1 KB (295133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3baadb6b9da90e40a0a57037da3b6e96d8599c58eff15ec5a6708bd0df6ab197`  
		Last Modified: Thu, 11 Jan 2024 05:34:58 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b705d298942cad7478031a63b4dc673d7d112dd13144ca0f6b4a85cf1c2318ec`  
		Last Modified: Thu, 11 Jan 2024 05:35:02 GMT  
		Size: 52.7 MB (52723949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a7281945f13c96bd64bdd2151029ecdd55723a1d6b57b9a88cc787f00c3f4f`  
		Last Modified: Thu, 11 Jan 2024 05:34:56 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7595f19c0256c9fbc059ca171d4909f09e648811bf4a86e74eff51cf29319477`  
		Last Modified: Thu, 11 Jan 2024 05:34:56 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8224f3b72b8930d3657822dcad3731868ebeeca1815bba4374e1c06824dc3133`  
		Last Modified: Thu, 11 Jan 2024 05:34:56 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a4cce3951e5070185c31edf9e8b96bc1b2fef875581f66f76059c20cbee6218`  
		Last Modified: Thu, 11 Jan 2024 05:34:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:8186dcf53c5964afdb14024925e7aa13e71e9f22b665cbbe926e80bc1d828503
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88720355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4daaa9a74f3ce7fabf84b8351b56756ad504ca89ed84a6bddf6a42e63d2675bd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:27:45 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jan 2024 06:27:46 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 11 Jan 2024 06:27:52 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:27:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Thu, 11 Jan 2024 06:27:54 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jan 2024 06:27:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:27:59 GMT
ENV COUCHDB_VERSION=3.3.3
# Thu, 11 Jan 2024 06:27:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 11 Jan 2024 06:28:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 11 Jan 2024 06:28:11 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 11 Jan 2024 06:28:11 GMT
COPY --chown=couchdb:couchdbfile:e5db3ae8229456931b3901d8737d15bbebc21bae345eb60dc63b3edc7a03cfbc in /opt/couchdb/etc/ 
# Thu, 11 Jan 2024 06:28:11 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Thu, 11 Jan 2024 06:28:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 11 Jan 2024 06:28:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:28:12 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jan 2024 06:28:12 GMT
EXPOSE 4369 5984 9100
# Thu, 11 Jan 2024 06:28:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ccc2078107ccc438fcb3b557ed215d440cd15f6f1879ad9db9f9b84b6946ac2`  
		Last Modified: Thu, 11 Jan 2024 06:29:31 GMT  
		Size: 3.4 KB (3433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562c17c5f419b97b03f49e7bed7c8cfd4d92ba18af2b014b62eb052a179e63ac`  
		Last Modified: Thu, 11 Jan 2024 06:29:30 GMT  
		Size: 5.2 MB (5210746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0a74a2782d1ffc7d869c33ab658ff80a6d3cfcd8903731d2b6b85bce269f3a`  
		Last Modified: Thu, 11 Jan 2024 06:29:29 GMT  
		Size: 567.1 KB (567052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d92f4c25743b8992888f53be6782574bfbbfd772cc684706e5b48a64335287`  
		Last Modified: Thu, 11 Jan 2024 06:29:29 GMT  
		Size: 295.0 KB (295014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fdc8f03011aa4022b246fe0407ba7262723f0241e4cd3d25a21dff79bfb5a38`  
		Last Modified: Thu, 11 Jan 2024 06:29:29 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526e7e3d442f1428a1319a06b3ab6a7f513801d8685ed4f82c2f3673554ce903`  
		Last Modified: Thu, 11 Jan 2024 06:29:32 GMT  
		Size: 52.6 MB (52575849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484d11cf87354911d23d11cfbe6aeb7d8a796c9920f28bfe718a82f1eb0e08f7`  
		Last Modified: Thu, 11 Jan 2024 06:29:27 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6998cc50abfc5aaa579705f7cd87e6cc14d1d025f7991c7e1dbda78c001ec6a2`  
		Last Modified: Thu, 11 Jan 2024 06:29:27 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eba36c22e1fbb899a6ef140ff740dd457840b73757d76107d94aabf491822e0`  
		Last Modified: Thu, 11 Jan 2024 06:29:27 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9f8cd437ce7c18dd794ba132faf0160dff5278c64bdde4169d1e83b9ac22d0`  
		Last Modified: Thu, 11 Jan 2024 06:29:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:71ecbc9c195a60c66a1c1c5d5e72e1f9f89f326a186c5df487a6d390eb4b634b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (96007614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe505cc2c2df7063d3f23f30f459e2cf4d44971de8421052bb5248ae2b9936bc`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 11 Jan 2024 02:34:59 GMT
ADD file:577ec786dad9a86344b678e69a7f514c3deede7cc45d9b3c9088449060272d55 in / 
# Thu, 11 Jan 2024 02:35:01 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:30:25 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jan 2024 03:30:27 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 11 Jan 2024 03:30:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:30:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Thu, 11 Jan 2024 03:30:51 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jan 2024 03:31:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:31:09 GMT
ENV COUCHDB_VERSION=3.3.3
# Thu, 11 Jan 2024 03:31:10 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 11 Jan 2024 03:31:36 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 11 Jan 2024 03:31:38 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 11 Jan 2024 03:31:38 GMT
COPY --chown=couchdb:couchdbfile:e5db3ae8229456931b3901d8737d15bbebc21bae345eb60dc63b3edc7a03cfbc in /opt/couchdb/etc/ 
# Thu, 11 Jan 2024 03:31:39 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Thu, 11 Jan 2024 03:31:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 11 Jan 2024 03:31:42 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 03:31:42 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jan 2024 03:31:43 GMT
EXPOSE 4369 5984 9100
# Thu, 11 Jan 2024 03:31:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4c9dbec0f2ecfefcce502a32967ad48a18396e58a4950f972d672b4d95c84bcc`  
		Last Modified: Thu, 11 Jan 2024 02:40:16 GMT  
		Size: 35.3 MB (35293800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d36a93a1206cc85ef8791bb5fc9b1a212ec8f13c65cb09c5f1ea7be2950adf1`  
		Last Modified: Thu, 11 Jan 2024 03:32:21 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f81256de3a18967943f59a0b1b9931dbb8001bcf2650eb267dadbfcdae32db`  
		Last Modified: Thu, 11 Jan 2024 03:32:20 GMT  
		Size: 6.0 MB (6046274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5aab839934ae5028748b84f3ce32b535dd2bd1842bdf0a377ffcce46ef7ffb`  
		Last Modified: Thu, 11 Jan 2024 03:32:19 GMT  
		Size: 662.9 KB (662906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1327c67902d35033bb0c721980f80ddc38d539b101d3bee2bebffae63183c5fa`  
		Last Modified: Thu, 11 Jan 2024 03:32:19 GMT  
		Size: 295.1 KB (295142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04f26b416411093b2df143603fb2c349cdece87315d457850693e112f00fae6`  
		Last Modified: Thu, 11 Jan 2024 03:32:19 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31953ad359289cedf760f9e787681a7a3b1728a525ded248dde4de666d2cad6d`  
		Last Modified: Thu, 11 Jan 2024 03:32:23 GMT  
		Size: 53.7 MB (53701827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d92dfe86aea46604d8224976d0693306b512cbd99dce36276433e917520b32`  
		Last Modified: Thu, 11 Jan 2024 03:32:16 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170c73d485a6ff8254a1741017deb5f288e32f242ec08fa6b8f542eea5b62ae6`  
		Last Modified: Thu, 11 Jan 2024 03:32:16 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7008cbdbbe03281a17f4119708fd6bae79449ace30246a523b2e401e6d80263`  
		Last Modified: Thu, 11 Jan 2024 03:32:16 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda45f47c60cc6c457755c7af4e5c15c9d71c6b77f0372180e382f0fdb3ac28f`  
		Last Modified: Thu, 11 Jan 2024 03:32:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3.3` - linux; s390x

```console
$ docker pull couchdb@sha256:f1b4699daea1d64f1162a807185d98928134516adac50d1c139832df8fc34318
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (87021065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85c8be32187ef874de0d68df8b5232f566fe85437349ba9f1794400d0ef8e6b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 11 Jan 2024 01:45:46 GMT
ADD file:77a92d4e9397475a6c68f4341baba607a7c875bc6e252de3e096482dd074f8ca in / 
# Thu, 11 Jan 2024 01:45:49 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 05:56:37 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jan 2024 05:56:37 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 11 Jan 2024 05:56:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:56:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Thu, 11 Jan 2024 05:56:48 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jan 2024 05:56:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:56:54 GMT
ENV COUCHDB_VERSION=3.3.3
# Thu, 11 Jan 2024 05:56:54 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 11 Jan 2024 05:57:15 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 11 Jan 2024 05:57:18 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 11 Jan 2024 05:57:19 GMT
COPY --chown=couchdb:couchdbfile:e5db3ae8229456931b3901d8737d15bbebc21bae345eb60dc63b3edc7a03cfbc in /opt/couchdb/etc/ 
# Thu, 11 Jan 2024 05:57:19 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Thu, 11 Jan 2024 05:57:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 11 Jan 2024 05:57:20 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 05:57:20 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jan 2024 05:57:20 GMT
EXPOSE 4369 5984 9100
# Thu, 11 Jan 2024 05:57:20 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a8470cec8ee9510bf45556c756635d84eb3cbc0220b52812522196008c6b0d3e`  
		Last Modified: Thu, 11 Jan 2024 01:51:19 GMT  
		Size: 29.7 MB (29656884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cefad3d1b84d34933e006ba9b58bd33333046f78e415923952dd253fc6c7a05`  
		Last Modified: Thu, 11 Jan 2024 05:57:37 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08027e0ca2920aeb48561a1f84f07f538b03fdc22067b47aa2c28489cbc4bc25`  
		Last Modified: Thu, 11 Jan 2024 05:57:36 GMT  
		Size: 5.1 MB (5111668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a932b8b14973fd451ccf15fd59d9a2e12a2a4c9915504951dc8d0a455b77404b`  
		Last Modified: Thu, 11 Jan 2024 05:57:36 GMT  
		Size: 573.6 KB (573617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f58653b62bd97148f0cb8b5ece2fe9722fe38b1e1c334616ceec1cfe1dc72d`  
		Last Modified: Thu, 11 Jan 2024 05:57:36 GMT  
		Size: 295.1 KB (295051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd0ef1b80fc30354920b31651370b4007602a3bdf34ab931c15f1ceb28439dd`  
		Last Modified: Thu, 11 Jan 2024 05:57:35 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8deff2a22dc3f942be63a01c98515ff9b1edcc1654b94c9cfa3761ddd480225c`  
		Last Modified: Thu, 11 Jan 2024 05:57:39 GMT  
		Size: 51.4 MB (51376162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c79556934fb3341422637bddebb803ee73da632d7aaf66c6106dbb12bf1206`  
		Last Modified: Thu, 11 Jan 2024 05:57:34 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2590f69e566aefdebef97d238779d67e92af05e0c3646cc76bae3ec8f860c69`  
		Last Modified: Thu, 11 Jan 2024 05:57:34 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e81e97d3824a4dbae238e0a27db0851fb30a479ed4a155a168c79bd747458b`  
		Last Modified: Thu, 11 Jan 2024 05:57:34 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22a12fd5122e216fad215f7fb0fc7d0453135dad4b52ae627cbacc93e218c6c`  
		Last Modified: Thu, 11 Jan 2024 05:57:34 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:d684daac1e11c90df0f4ae9f5cc9866b198d03d1b636867741992b12f2dfeeb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:94eae1e4891cab1426c43e968258c444a9e4ec711b8d6e80dd19a11e48b56910
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.3 MB (90282155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ba54687bbde594dc5a12c99a6a7228ec9bd8140c9aeaf68d61103a8412dea7`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 05:32:51 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jan 2024 05:32:52 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 11 Jan 2024 05:32:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:33:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Thu, 11 Jan 2024 05:33:02 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jan 2024 05:33:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:33:08 GMT
ENV COUCHDB_VERSION=3.3.3
# Thu, 11 Jan 2024 05:33:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 11 Jan 2024 05:33:21 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 11 Jan 2024 05:33:21 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 11 Jan 2024 05:33:21 GMT
COPY --chown=couchdb:couchdbfile:e5db3ae8229456931b3901d8737d15bbebc21bae345eb60dc63b3edc7a03cfbc in /opt/couchdb/etc/ 
# Thu, 11 Jan 2024 05:33:21 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Thu, 11 Jan 2024 05:33:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 11 Jan 2024 05:33:22 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 05:33:22 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jan 2024 05:33:22 GMT
EXPOSE 4369 5984 9100
# Thu, 11 Jan 2024 05:33:22 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfeb8d6d7cb9ec479de9e07297a4472878669f03cdc566d5ba2bdf49121cdbd`  
		Last Modified: Thu, 11 Jan 2024 05:35:00 GMT  
		Size: 3.4 KB (3410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7ac1349877a8205b90d6e6d1ef8cfa4d201f84fc189f8655d5e0525c735ee0`  
		Last Modified: Thu, 11 Jan 2024 05:34:59 GMT  
		Size: 5.2 MB (5226552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efbad6a63f2382da1e97c8d1dc6a5cb77899556bbd8fad2aaf8dd66b2ce00604`  
		Last Modified: Thu, 11 Jan 2024 05:34:58 GMT  
		Size: 610.9 KB (610908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227a8bbc783b3bd4eeed204844a79a51702307ae9b08da4ae1a162f142c48334`  
		Last Modified: Thu, 11 Jan 2024 05:34:58 GMT  
		Size: 295.1 KB (295133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3baadb6b9da90e40a0a57037da3b6e96d8599c58eff15ec5a6708bd0df6ab197`  
		Last Modified: Thu, 11 Jan 2024 05:34:58 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b705d298942cad7478031a63b4dc673d7d112dd13144ca0f6b4a85cf1c2318ec`  
		Last Modified: Thu, 11 Jan 2024 05:35:02 GMT  
		Size: 52.7 MB (52723949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a7281945f13c96bd64bdd2151029ecdd55723a1d6b57b9a88cc787f00c3f4f`  
		Last Modified: Thu, 11 Jan 2024 05:34:56 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7595f19c0256c9fbc059ca171d4909f09e648811bf4a86e74eff51cf29319477`  
		Last Modified: Thu, 11 Jan 2024 05:34:56 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8224f3b72b8930d3657822dcad3731868ebeeca1815bba4374e1c06824dc3133`  
		Last Modified: Thu, 11 Jan 2024 05:34:56 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a4cce3951e5070185c31edf9e8b96bc1b2fef875581f66f76059c20cbee6218`  
		Last Modified: Thu, 11 Jan 2024 05:34:56 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:8186dcf53c5964afdb14024925e7aa13e71e9f22b665cbbe926e80bc1d828503
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88720355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4daaa9a74f3ce7fabf84b8351b56756ad504ca89ed84a6bddf6a42e63d2675bd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:27:45 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jan 2024 06:27:46 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 11 Jan 2024 06:27:52 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:27:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Thu, 11 Jan 2024 06:27:54 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jan 2024 06:27:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:27:59 GMT
ENV COUCHDB_VERSION=3.3.3
# Thu, 11 Jan 2024 06:27:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 11 Jan 2024 06:28:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 11 Jan 2024 06:28:11 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 11 Jan 2024 06:28:11 GMT
COPY --chown=couchdb:couchdbfile:e5db3ae8229456931b3901d8737d15bbebc21bae345eb60dc63b3edc7a03cfbc in /opt/couchdb/etc/ 
# Thu, 11 Jan 2024 06:28:11 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Thu, 11 Jan 2024 06:28:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 11 Jan 2024 06:28:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:28:12 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jan 2024 06:28:12 GMT
EXPOSE 4369 5984 9100
# Thu, 11 Jan 2024 06:28:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ccc2078107ccc438fcb3b557ed215d440cd15f6f1879ad9db9f9b84b6946ac2`  
		Last Modified: Thu, 11 Jan 2024 06:29:31 GMT  
		Size: 3.4 KB (3433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562c17c5f419b97b03f49e7bed7c8cfd4d92ba18af2b014b62eb052a179e63ac`  
		Last Modified: Thu, 11 Jan 2024 06:29:30 GMT  
		Size: 5.2 MB (5210746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0a74a2782d1ffc7d869c33ab658ff80a6d3cfcd8903731d2b6b85bce269f3a`  
		Last Modified: Thu, 11 Jan 2024 06:29:29 GMT  
		Size: 567.1 KB (567052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d92f4c25743b8992888f53be6782574bfbbfd772cc684706e5b48a64335287`  
		Last Modified: Thu, 11 Jan 2024 06:29:29 GMT  
		Size: 295.0 KB (295014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fdc8f03011aa4022b246fe0407ba7262723f0241e4cd3d25a21dff79bfb5a38`  
		Last Modified: Thu, 11 Jan 2024 06:29:29 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526e7e3d442f1428a1319a06b3ab6a7f513801d8685ed4f82c2f3673554ce903`  
		Last Modified: Thu, 11 Jan 2024 06:29:32 GMT  
		Size: 52.6 MB (52575849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484d11cf87354911d23d11cfbe6aeb7d8a796c9920f28bfe718a82f1eb0e08f7`  
		Last Modified: Thu, 11 Jan 2024 06:29:27 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6998cc50abfc5aaa579705f7cd87e6cc14d1d025f7991c7e1dbda78c001ec6a2`  
		Last Modified: Thu, 11 Jan 2024 06:29:27 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eba36c22e1fbb899a6ef140ff740dd457840b73757d76107d94aabf491822e0`  
		Last Modified: Thu, 11 Jan 2024 06:29:27 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9f8cd437ce7c18dd794ba132faf0160dff5278c64bdde4169d1e83b9ac22d0`  
		Last Modified: Thu, 11 Jan 2024 06:29:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:71ecbc9c195a60c66a1c1c5d5e72e1f9f89f326a186c5df487a6d390eb4b634b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (96007614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe505cc2c2df7063d3f23f30f459e2cf4d44971de8421052bb5248ae2b9936bc`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 11 Jan 2024 02:34:59 GMT
ADD file:577ec786dad9a86344b678e69a7f514c3deede7cc45d9b3c9088449060272d55 in / 
# Thu, 11 Jan 2024 02:35:01 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:30:25 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jan 2024 03:30:27 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 11 Jan 2024 03:30:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:30:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Thu, 11 Jan 2024 03:30:51 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jan 2024 03:31:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:31:09 GMT
ENV COUCHDB_VERSION=3.3.3
# Thu, 11 Jan 2024 03:31:10 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 11 Jan 2024 03:31:36 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 11 Jan 2024 03:31:38 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 11 Jan 2024 03:31:38 GMT
COPY --chown=couchdb:couchdbfile:e5db3ae8229456931b3901d8737d15bbebc21bae345eb60dc63b3edc7a03cfbc in /opt/couchdb/etc/ 
# Thu, 11 Jan 2024 03:31:39 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Thu, 11 Jan 2024 03:31:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 11 Jan 2024 03:31:42 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 03:31:42 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jan 2024 03:31:43 GMT
EXPOSE 4369 5984 9100
# Thu, 11 Jan 2024 03:31:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4c9dbec0f2ecfefcce502a32967ad48a18396e58a4950f972d672b4d95c84bcc`  
		Last Modified: Thu, 11 Jan 2024 02:40:16 GMT  
		Size: 35.3 MB (35293800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d36a93a1206cc85ef8791bb5fc9b1a212ec8f13c65cb09c5f1ea7be2950adf1`  
		Last Modified: Thu, 11 Jan 2024 03:32:21 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f81256de3a18967943f59a0b1b9931dbb8001bcf2650eb267dadbfcdae32db`  
		Last Modified: Thu, 11 Jan 2024 03:32:20 GMT  
		Size: 6.0 MB (6046274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5aab839934ae5028748b84f3ce32b535dd2bd1842bdf0a377ffcce46ef7ffb`  
		Last Modified: Thu, 11 Jan 2024 03:32:19 GMT  
		Size: 662.9 KB (662906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1327c67902d35033bb0c721980f80ddc38d539b101d3bee2bebffae63183c5fa`  
		Last Modified: Thu, 11 Jan 2024 03:32:19 GMT  
		Size: 295.1 KB (295142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04f26b416411093b2df143603fb2c349cdece87315d457850693e112f00fae6`  
		Last Modified: Thu, 11 Jan 2024 03:32:19 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31953ad359289cedf760f9e787681a7a3b1728a525ded248dde4de666d2cad6d`  
		Last Modified: Thu, 11 Jan 2024 03:32:23 GMT  
		Size: 53.7 MB (53701827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d92dfe86aea46604d8224976d0693306b512cbd99dce36276433e917520b32`  
		Last Modified: Thu, 11 Jan 2024 03:32:16 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170c73d485a6ff8254a1741017deb5f288e32f242ec08fa6b8f542eea5b62ae6`  
		Last Modified: Thu, 11 Jan 2024 03:32:16 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7008cbdbbe03281a17f4119708fd6bae79449ace30246a523b2e401e6d80263`  
		Last Modified: Thu, 11 Jan 2024 03:32:16 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda45f47c60cc6c457755c7af4e5c15c9d71c6b77f0372180e382f0fdb3ac28f`  
		Last Modified: Thu, 11 Jan 2024 03:32:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:f1b4699daea1d64f1162a807185d98928134516adac50d1c139832df8fc34318
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (87021065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85c8be32187ef874de0d68df8b5232f566fe85437349ba9f1794400d0ef8e6b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 11 Jan 2024 01:45:46 GMT
ADD file:77a92d4e9397475a6c68f4341baba607a7c875bc6e252de3e096482dd074f8ca in / 
# Thu, 11 Jan 2024 01:45:49 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 05:56:37 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 11 Jan 2024 05:56:37 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 11 Jan 2024 05:56:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:56:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Thu, 11 Jan 2024 05:56:48 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 11 Jan 2024 05:56:54 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:56:54 GMT
ENV COUCHDB_VERSION=3.3.3
# Thu, 11 Jan 2024 05:56:54 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 11 Jan 2024 05:57:15 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 11 Jan 2024 05:57:18 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 11 Jan 2024 05:57:19 GMT
COPY --chown=couchdb:couchdbfile:e5db3ae8229456931b3901d8737d15bbebc21bae345eb60dc63b3edc7a03cfbc in /opt/couchdb/etc/ 
# Thu, 11 Jan 2024 05:57:19 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Thu, 11 Jan 2024 05:57:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 11 Jan 2024 05:57:20 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 05:57:20 GMT
VOLUME [/opt/couchdb/data]
# Thu, 11 Jan 2024 05:57:20 GMT
EXPOSE 4369 5984 9100
# Thu, 11 Jan 2024 05:57:20 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a8470cec8ee9510bf45556c756635d84eb3cbc0220b52812522196008c6b0d3e`  
		Last Modified: Thu, 11 Jan 2024 01:51:19 GMT  
		Size: 29.7 MB (29656884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cefad3d1b84d34933e006ba9b58bd33333046f78e415923952dd253fc6c7a05`  
		Last Modified: Thu, 11 Jan 2024 05:57:37 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08027e0ca2920aeb48561a1f84f07f538b03fdc22067b47aa2c28489cbc4bc25`  
		Last Modified: Thu, 11 Jan 2024 05:57:36 GMT  
		Size: 5.1 MB (5111668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a932b8b14973fd451ccf15fd59d9a2e12a2a4c9915504951dc8d0a455b77404b`  
		Last Modified: Thu, 11 Jan 2024 05:57:36 GMT  
		Size: 573.6 KB (573617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f58653b62bd97148f0cb8b5ece2fe9722fe38b1e1c334616ceec1cfe1dc72d`  
		Last Modified: Thu, 11 Jan 2024 05:57:36 GMT  
		Size: 295.1 KB (295051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd0ef1b80fc30354920b31651370b4007602a3bdf34ab931c15f1ceb28439dd`  
		Last Modified: Thu, 11 Jan 2024 05:57:35 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8deff2a22dc3f942be63a01c98515ff9b1edcc1654b94c9cfa3761ddd480225c`  
		Last Modified: Thu, 11 Jan 2024 05:57:39 GMT  
		Size: 51.4 MB (51376162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c79556934fb3341422637bddebb803ee73da632d7aaf66c6106dbb12bf1206`  
		Last Modified: Thu, 11 Jan 2024 05:57:34 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2590f69e566aefdebef97d238779d67e92af05e0c3646cc76bae3ec8f860c69`  
		Last Modified: Thu, 11 Jan 2024 05:57:34 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e81e97d3824a4dbae238e0a27db0851fb30a479ed4a155a168c79bd747458b`  
		Last Modified: Thu, 11 Jan 2024 05:57:34 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22a12fd5122e216fad215f7fb0fc7d0453135dad4b52ae627cbacc93e218c6c`  
		Last Modified: Thu, 11 Jan 2024 05:57:34 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
