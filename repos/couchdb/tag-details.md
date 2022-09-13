<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchdb`

-	[`couchdb:2`](#couchdb2)
-	[`couchdb:2.3`](#couchdb23)
-	[`couchdb:2.3.1`](#couchdb231)
-	[`couchdb:3`](#couchdb3)
-	[`couchdb:3.1`](#couchdb31)
-	[`couchdb:3.1.2`](#couchdb312)
-	[`couchdb:3.2`](#couchdb32)
-	[`couchdb:3.2.2`](#couchdb322)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:2`

```console
$ docker pull couchdb@sha256:8b546b52534a3e81a7ac3c37f848a3ac194d8b5628a4aa01c65d87b237949c72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:fdd360c2699c5ccce0e926e64e111ac1ddbeea91ae06bd8c8342deab8bbece81
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84521637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea24299b2688202b1f16bf104a8edd9d9d3620e72226b286c744b41527dd3c1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:48 GMT
ADD file:782d864aa72c2d5fb599311ebae56db4067d2e91ff532c1aaf1a291c3dbce5bb in / 
# Tue, 13 Sep 2022 00:56:49 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 03:54:33 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Sep 2022 03:54:34 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 13 Sep 2022 03:54:41 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 03:54:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 13 Sep 2022 03:54:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Sep 2022 03:54:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 03:55:14 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 13 Sep 2022 03:55:14 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 13 Sep 2022 03:55:32 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 13 Sep 2022 03:55:32 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 13 Sep 2022 03:55:32 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 13 Sep 2022 03:55:32 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 13 Sep 2022 03:55:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 13 Sep 2022 03:55:33 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 03:55:33 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Sep 2022 03:55:33 GMT
EXPOSE 4369 5984 9100
# Tue, 13 Sep 2022 03:55:33 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4b7b4a8876e2f677668e51b8473f97a237d3d4df201b9df4031bcaa8068370b1`  
		Last Modified: Tue, 13 Sep 2022 01:01:16 GMT  
		Size: 27.1 MB (27130552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c088c3a03bf60b8f0b3b24363efbc28aef3c87451537b97521bfbf1f2aa13199`  
		Last Modified: Tue, 13 Sep 2022 03:56:21 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e6c9d6ee4b135545b364dd8b30be2b91e27e6b1e62addf07801a90a90ac96f`  
		Last Modified: Tue, 13 Sep 2022 03:56:20 GMT  
		Size: 6.7 MB (6698707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e1633127944965c144a64754b6a92bf6622c1de73c33716a59ca7f9ef1baca`  
		Last Modified: Tue, 13 Sep 2022 03:56:19 GMT  
		Size: 1.3 MB (1258362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61a40f9af1917164479b4fc40fc1f8fa2db40005957a46bb7b167f3a6f2724c`  
		Last Modified: Tue, 13 Sep 2022 03:56:18 GMT  
		Size: 293.1 KB (293062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d24fe37ce953bdb8931392614becce928b2547796764bddd9f88e56c6ed97d8`  
		Last Modified: Tue, 13 Sep 2022 03:56:34 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283af9663b67d645492bd442d5e7cbc4a46b247238ff7aed93a0483c77310649`  
		Last Modified: Tue, 13 Sep 2022 03:56:38 GMT  
		Size: 49.1 MB (49133940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4788d07645893982eb35d79013264bcb958817cb4c1c0e52f0254f8de7e34c33`  
		Last Modified: Tue, 13 Sep 2022 03:56:32 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e97b88ff5fd41abb9abad7b6ce9c27f883f8df6819b6074f7e6732f3e396ce`  
		Last Modified: Tue, 13 Sep 2022 03:56:32 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6073742d94dc8629793832fe392891511bc2c7fa5be1aa13b87b50d0d956c430`  
		Last Modified: Tue, 13 Sep 2022 03:56:32 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3d38689c87981ca7f5c0ace468c72ed5ff7a897ed74b8d86386db94be8d949`  
		Last Modified: Tue, 13 Sep 2022 03:56:32 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:f46aa3a2a4b42b8d05949d938b3a867c6e20dfb88bda4b6d9752c43ed77faaf1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72531356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f33c6f656db8dbbaf57ddcbcd8159a30eb978619cf0842740873acb06858afc7`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:58 GMT
ADD file:4c5bca2d158b11314fb47a6d4b34239575621c2f00f92e77870f23aa02913fac in / 
# Tue, 23 Aug 2022 01:52:59 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:42:10 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Aug 2022 02:42:11 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 23 Aug 2022 02:42:19 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:42:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 23 Aug 2022 02:42:24 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Aug 2022 02:42:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:43:01 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 23 Aug 2022 02:43:02 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 23 Aug 2022 02:43:16 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 23 Aug 2022 02:43:17 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 23 Aug 2022 02:43:18 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 23 Aug 2022 02:43:19 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 23 Aug 2022 02:43:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 02:43:20 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 23 Aug 2022 02:43:21 GMT
VOLUME [/opt/couchdb/data]
# Tue, 23 Aug 2022 02:43:22 GMT
EXPOSE 4369 5984 9100
# Tue, 23 Aug 2022 02:43:23 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a84b81edbdb892b3702892bbb01c240695b0b9d619fda43a9b951c9d2df1443c`  
		Last Modified: Tue, 23 Aug 2022 01:58:50 GMT  
		Size: 25.9 MB (25912515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0f4e940c5871c8fab3c016b817ff8d6306da1ba35e200a5b45893fa56340a9`  
		Last Modified: Tue, 23 Aug 2022 02:44:20 GMT  
		Size: 3.3 KB (3319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd1d4c0f7d1b0bb90aa98f52f1bac0c37707c2d190cd73ea9c79dab071dda83f`  
		Last Modified: Tue, 23 Aug 2022 02:44:19 GMT  
		Size: 6.6 MB (6557176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90567554c16513f656919984d64a7cb938885d7229581719d411c0887c3f2987`  
		Last Modified: Tue, 23 Aug 2022 02:44:18 GMT  
		Size: 951.2 KB (951189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd12be703c9cae124252cac51aa545e6dd67c898c1258761b7e389f252eb8abc`  
		Last Modified: Tue, 23 Aug 2022 02:44:17 GMT  
		Size: 80.0 KB (79956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bef26cd846ae05de27d4329ccae7d30c97dc70d985398a5899f6d0ad218a9c`  
		Last Modified: Tue, 23 Aug 2022 02:44:35 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70df8e83e60da2a02a8beb18e99298dae9fa37fbd3f2299a0a1e2f0feccc8068`  
		Last Modified: Tue, 23 Aug 2022 02:44:38 GMT  
		Size: 39.0 MB (39023592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ee0650183b67f624d71a3487e85310478691d06821878dde9a0a7014072110`  
		Last Modified: Tue, 23 Aug 2022 02:44:33 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8610bf98153f8517ba647b35e6c36942d405459618c8213d32c559811a2094`  
		Last Modified: Tue, 23 Aug 2022 02:44:33 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa52ef42ef91f1ba21b813644e1c3c5f4e0e51620b182ba9bbe2f5ef17264736`  
		Last Modified: Tue, 23 Aug 2022 02:44:33 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573acb96d62e72e1a12917a107542024c283b257fe589258c766e653ba77f853`  
		Last Modified: Tue, 23 Aug 2022 02:44:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:8b546b52534a3e81a7ac3c37f848a3ac194d8b5628a4aa01c65d87b237949c72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:fdd360c2699c5ccce0e926e64e111ac1ddbeea91ae06bd8c8342deab8bbece81
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84521637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea24299b2688202b1f16bf104a8edd9d9d3620e72226b286c744b41527dd3c1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:48 GMT
ADD file:782d864aa72c2d5fb599311ebae56db4067d2e91ff532c1aaf1a291c3dbce5bb in / 
# Tue, 13 Sep 2022 00:56:49 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 03:54:33 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Sep 2022 03:54:34 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 13 Sep 2022 03:54:41 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 03:54:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 13 Sep 2022 03:54:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Sep 2022 03:54:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 03:55:14 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 13 Sep 2022 03:55:14 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 13 Sep 2022 03:55:32 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 13 Sep 2022 03:55:32 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 13 Sep 2022 03:55:32 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 13 Sep 2022 03:55:32 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 13 Sep 2022 03:55:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 13 Sep 2022 03:55:33 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 03:55:33 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Sep 2022 03:55:33 GMT
EXPOSE 4369 5984 9100
# Tue, 13 Sep 2022 03:55:33 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4b7b4a8876e2f677668e51b8473f97a237d3d4df201b9df4031bcaa8068370b1`  
		Last Modified: Tue, 13 Sep 2022 01:01:16 GMT  
		Size: 27.1 MB (27130552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c088c3a03bf60b8f0b3b24363efbc28aef3c87451537b97521bfbf1f2aa13199`  
		Last Modified: Tue, 13 Sep 2022 03:56:21 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e6c9d6ee4b135545b364dd8b30be2b91e27e6b1e62addf07801a90a90ac96f`  
		Last Modified: Tue, 13 Sep 2022 03:56:20 GMT  
		Size: 6.7 MB (6698707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e1633127944965c144a64754b6a92bf6622c1de73c33716a59ca7f9ef1baca`  
		Last Modified: Tue, 13 Sep 2022 03:56:19 GMT  
		Size: 1.3 MB (1258362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61a40f9af1917164479b4fc40fc1f8fa2db40005957a46bb7b167f3a6f2724c`  
		Last Modified: Tue, 13 Sep 2022 03:56:18 GMT  
		Size: 293.1 KB (293062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d24fe37ce953bdb8931392614becce928b2547796764bddd9f88e56c6ed97d8`  
		Last Modified: Tue, 13 Sep 2022 03:56:34 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283af9663b67d645492bd442d5e7cbc4a46b247238ff7aed93a0483c77310649`  
		Last Modified: Tue, 13 Sep 2022 03:56:38 GMT  
		Size: 49.1 MB (49133940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4788d07645893982eb35d79013264bcb958817cb4c1c0e52f0254f8de7e34c33`  
		Last Modified: Tue, 13 Sep 2022 03:56:32 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e97b88ff5fd41abb9abad7b6ce9c27f883f8df6819b6074f7e6732f3e396ce`  
		Last Modified: Tue, 13 Sep 2022 03:56:32 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6073742d94dc8629793832fe392891511bc2c7fa5be1aa13b87b50d0d956c430`  
		Last Modified: Tue, 13 Sep 2022 03:56:32 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3d38689c87981ca7f5c0ace468c72ed5ff7a897ed74b8d86386db94be8d949`  
		Last Modified: Tue, 13 Sep 2022 03:56:32 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:f46aa3a2a4b42b8d05949d938b3a867c6e20dfb88bda4b6d9752c43ed77faaf1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72531356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f33c6f656db8dbbaf57ddcbcd8159a30eb978619cf0842740873acb06858afc7`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:58 GMT
ADD file:4c5bca2d158b11314fb47a6d4b34239575621c2f00f92e77870f23aa02913fac in / 
# Tue, 23 Aug 2022 01:52:59 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:42:10 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Aug 2022 02:42:11 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 23 Aug 2022 02:42:19 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:42:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 23 Aug 2022 02:42:24 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Aug 2022 02:42:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:43:01 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 23 Aug 2022 02:43:02 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 23 Aug 2022 02:43:16 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 23 Aug 2022 02:43:17 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 23 Aug 2022 02:43:18 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 23 Aug 2022 02:43:19 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 23 Aug 2022 02:43:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 02:43:20 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 23 Aug 2022 02:43:21 GMT
VOLUME [/opt/couchdb/data]
# Tue, 23 Aug 2022 02:43:22 GMT
EXPOSE 4369 5984 9100
# Tue, 23 Aug 2022 02:43:23 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a84b81edbdb892b3702892bbb01c240695b0b9d619fda43a9b951c9d2df1443c`  
		Last Modified: Tue, 23 Aug 2022 01:58:50 GMT  
		Size: 25.9 MB (25912515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0f4e940c5871c8fab3c016b817ff8d6306da1ba35e200a5b45893fa56340a9`  
		Last Modified: Tue, 23 Aug 2022 02:44:20 GMT  
		Size: 3.3 KB (3319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd1d4c0f7d1b0bb90aa98f52f1bac0c37707c2d190cd73ea9c79dab071dda83f`  
		Last Modified: Tue, 23 Aug 2022 02:44:19 GMT  
		Size: 6.6 MB (6557176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90567554c16513f656919984d64a7cb938885d7229581719d411c0887c3f2987`  
		Last Modified: Tue, 23 Aug 2022 02:44:18 GMT  
		Size: 951.2 KB (951189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd12be703c9cae124252cac51aa545e6dd67c898c1258761b7e389f252eb8abc`  
		Last Modified: Tue, 23 Aug 2022 02:44:17 GMT  
		Size: 80.0 KB (79956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bef26cd846ae05de27d4329ccae7d30c97dc70d985398a5899f6d0ad218a9c`  
		Last Modified: Tue, 23 Aug 2022 02:44:35 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70df8e83e60da2a02a8beb18e99298dae9fa37fbd3f2299a0a1e2f0feccc8068`  
		Last Modified: Tue, 23 Aug 2022 02:44:38 GMT  
		Size: 39.0 MB (39023592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ee0650183b67f624d71a3487e85310478691d06821878dde9a0a7014072110`  
		Last Modified: Tue, 23 Aug 2022 02:44:33 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8610bf98153f8517ba647b35e6c36942d405459618c8213d32c559811a2094`  
		Last Modified: Tue, 23 Aug 2022 02:44:33 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa52ef42ef91f1ba21b813644e1c3c5f4e0e51620b182ba9bbe2f5ef17264736`  
		Last Modified: Tue, 23 Aug 2022 02:44:33 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573acb96d62e72e1a12917a107542024c283b257fe589258c766e653ba77f853`  
		Last Modified: Tue, 23 Aug 2022 02:44:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:8b546b52534a3e81a7ac3c37f848a3ac194d8b5628a4aa01c65d87b237949c72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:fdd360c2699c5ccce0e926e64e111ac1ddbeea91ae06bd8c8342deab8bbece81
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84521637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea24299b2688202b1f16bf104a8edd9d9d3620e72226b286c744b41527dd3c1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:48 GMT
ADD file:782d864aa72c2d5fb599311ebae56db4067d2e91ff532c1aaf1a291c3dbce5bb in / 
# Tue, 13 Sep 2022 00:56:49 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 03:54:33 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Sep 2022 03:54:34 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 13 Sep 2022 03:54:41 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 03:54:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 13 Sep 2022 03:54:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Sep 2022 03:54:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 03:55:14 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 13 Sep 2022 03:55:14 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 13 Sep 2022 03:55:32 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 13 Sep 2022 03:55:32 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 13 Sep 2022 03:55:32 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 13 Sep 2022 03:55:32 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 13 Sep 2022 03:55:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 13 Sep 2022 03:55:33 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 03:55:33 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Sep 2022 03:55:33 GMT
EXPOSE 4369 5984 9100
# Tue, 13 Sep 2022 03:55:33 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4b7b4a8876e2f677668e51b8473f97a237d3d4df201b9df4031bcaa8068370b1`  
		Last Modified: Tue, 13 Sep 2022 01:01:16 GMT  
		Size: 27.1 MB (27130552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c088c3a03bf60b8f0b3b24363efbc28aef3c87451537b97521bfbf1f2aa13199`  
		Last Modified: Tue, 13 Sep 2022 03:56:21 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e6c9d6ee4b135545b364dd8b30be2b91e27e6b1e62addf07801a90a90ac96f`  
		Last Modified: Tue, 13 Sep 2022 03:56:20 GMT  
		Size: 6.7 MB (6698707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e1633127944965c144a64754b6a92bf6622c1de73c33716a59ca7f9ef1baca`  
		Last Modified: Tue, 13 Sep 2022 03:56:19 GMT  
		Size: 1.3 MB (1258362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61a40f9af1917164479b4fc40fc1f8fa2db40005957a46bb7b167f3a6f2724c`  
		Last Modified: Tue, 13 Sep 2022 03:56:18 GMT  
		Size: 293.1 KB (293062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d24fe37ce953bdb8931392614becce928b2547796764bddd9f88e56c6ed97d8`  
		Last Modified: Tue, 13 Sep 2022 03:56:34 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283af9663b67d645492bd442d5e7cbc4a46b247238ff7aed93a0483c77310649`  
		Last Modified: Tue, 13 Sep 2022 03:56:38 GMT  
		Size: 49.1 MB (49133940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4788d07645893982eb35d79013264bcb958817cb4c1c0e52f0254f8de7e34c33`  
		Last Modified: Tue, 13 Sep 2022 03:56:32 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e97b88ff5fd41abb9abad7b6ce9c27f883f8df6819b6074f7e6732f3e396ce`  
		Last Modified: Tue, 13 Sep 2022 03:56:32 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6073742d94dc8629793832fe392891511bc2c7fa5be1aa13b87b50d0d956c430`  
		Last Modified: Tue, 13 Sep 2022 03:56:32 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3d38689c87981ca7f5c0ace468c72ed5ff7a897ed74b8d86386db94be8d949`  
		Last Modified: Tue, 13 Sep 2022 03:56:32 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:f46aa3a2a4b42b8d05949d938b3a867c6e20dfb88bda4b6d9752c43ed77faaf1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72531356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f33c6f656db8dbbaf57ddcbcd8159a30eb978619cf0842740873acb06858afc7`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:58 GMT
ADD file:4c5bca2d158b11314fb47a6d4b34239575621c2f00f92e77870f23aa02913fac in / 
# Tue, 23 Aug 2022 01:52:59 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:42:10 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Aug 2022 02:42:11 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 23 Aug 2022 02:42:19 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:42:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 23 Aug 2022 02:42:24 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Aug 2022 02:42:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:43:01 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 23 Aug 2022 02:43:02 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 23 Aug 2022 02:43:16 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 23 Aug 2022 02:43:17 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 23 Aug 2022 02:43:18 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 23 Aug 2022 02:43:19 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 23 Aug 2022 02:43:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 02:43:20 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 23 Aug 2022 02:43:21 GMT
VOLUME [/opt/couchdb/data]
# Tue, 23 Aug 2022 02:43:22 GMT
EXPOSE 4369 5984 9100
# Tue, 23 Aug 2022 02:43:23 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a84b81edbdb892b3702892bbb01c240695b0b9d619fda43a9b951c9d2df1443c`  
		Last Modified: Tue, 23 Aug 2022 01:58:50 GMT  
		Size: 25.9 MB (25912515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0f4e940c5871c8fab3c016b817ff8d6306da1ba35e200a5b45893fa56340a9`  
		Last Modified: Tue, 23 Aug 2022 02:44:20 GMT  
		Size: 3.3 KB (3319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd1d4c0f7d1b0bb90aa98f52f1bac0c37707c2d190cd73ea9c79dab071dda83f`  
		Last Modified: Tue, 23 Aug 2022 02:44:19 GMT  
		Size: 6.6 MB (6557176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90567554c16513f656919984d64a7cb938885d7229581719d411c0887c3f2987`  
		Last Modified: Tue, 23 Aug 2022 02:44:18 GMT  
		Size: 951.2 KB (951189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd12be703c9cae124252cac51aa545e6dd67c898c1258761b7e389f252eb8abc`  
		Last Modified: Tue, 23 Aug 2022 02:44:17 GMT  
		Size: 80.0 KB (79956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bef26cd846ae05de27d4329ccae7d30c97dc70d985398a5899f6d0ad218a9c`  
		Last Modified: Tue, 23 Aug 2022 02:44:35 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70df8e83e60da2a02a8beb18e99298dae9fa37fbd3f2299a0a1e2f0feccc8068`  
		Last Modified: Tue, 23 Aug 2022 02:44:38 GMT  
		Size: 39.0 MB (39023592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ee0650183b67f624d71a3487e85310478691d06821878dde9a0a7014072110`  
		Last Modified: Tue, 23 Aug 2022 02:44:33 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8610bf98153f8517ba647b35e6c36942d405459618c8213d32c559811a2094`  
		Last Modified: Tue, 23 Aug 2022 02:44:33 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa52ef42ef91f1ba21b813644e1c3c5f4e0e51620b182ba9bbe2f5ef17264736`  
		Last Modified: Tue, 23 Aug 2022 02:44:33 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573acb96d62e72e1a12917a107542024c283b257fe589258c766e653ba77f853`  
		Last Modified: Tue, 23 Aug 2022 02:44:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3`

```console
$ docker pull couchdb@sha256:b8f1266f877d094bf16126713c8e7e8a91688bb5311826fa779cad3972387a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:ac5c57c4df9f9d0129390f652b62dfa348a1b383c458841010ad52abbb6c8f0b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87530196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9292db79eb5d3107963496f664c9764d4974a423cff1612702d8ca782a888f5`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 03:53:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Sep 2022 03:54:00 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 13 Sep 2022 03:54:07 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 03:54:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 13 Sep 2022 03:54:10 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Sep 2022 03:54:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 03:54:16 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 13 Sep 2022 03:54:16 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 13 Sep 2022 03:54:29 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 13 Sep 2022 03:54:30 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 13 Sep 2022 03:54:30 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 13 Sep 2022 03:54:30 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 13 Sep 2022 03:54:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 13 Sep 2022 03:54:30 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 03:54:31 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Sep 2022 03:54:31 GMT
EXPOSE 4369 5984 9100
# Tue, 13 Sep 2022 03:54:31 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9775a4fbb4b5564bbc1ec8e077d317b8745a7598e059365241ddc1a9766c129c`  
		Last Modified: Tue, 13 Sep 2022 03:55:55 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d707a0a4de816f6a35046bed27c3bd025081394b651fd4b339188a4e19967c4`  
		Last Modified: Tue, 13 Sep 2022 03:55:54 GMT  
		Size: 5.2 MB (5224215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15634eb84187cbacfe864298c664c5eb740aa1a455a39e64f4f6a94c0f07a14`  
		Last Modified: Tue, 13 Sep 2022 03:55:53 GMT  
		Size: 1.6 MB (1553277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59f0fe4ba863352dbd7372301d2eae5be8cd69838e66876a65c5c0b1666de8c`  
		Last Modified: Tue, 13 Sep 2022 03:55:53 GMT  
		Size: 295.6 KB (295573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f507b233637bff8bdab3e80909e9dcdcc02a11efcca3f242c4ae8bf410296bbe`  
		Last Modified: Tue, 13 Sep 2022 03:55:53 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a76624d812c6c764f46d961f80510fa92e7512419c528ba6ab86e250d365d8`  
		Last Modified: Tue, 13 Sep 2022 03:55:56 GMT  
		Size: 49.0 MB (49045868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6166f23a925f2a6a18aa9efa186271f01020d8fd5d40d7a307cb02d6172974`  
		Last Modified: Tue, 13 Sep 2022 03:55:50 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc867e39bf60d67febf095d33500f8b30b51f6edbef26bd9d37b7a38a9bfaebc`  
		Last Modified: Tue, 13 Sep 2022 03:55:50 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5bc74ba5f149b1005fb23f07d5b84e4946fc31381d124892f99322b8c9a202`  
		Last Modified: Tue, 13 Sep 2022 03:55:50 GMT  
		Size: 2.2 KB (2187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ff75922f5a116b20c00eabe11b5280455fc7c77595f4ae03ed74a4e45ffb41`  
		Last Modified: Tue, 13 Sep 2022 03:55:50 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:6d7e5cb02dcd01b68f68dfd7b1572a8b2951615b4a359edb3aaebac20fc5d332
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85427934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e92099630042247528b18325ac126f4af5e138e14f74de8f499e49ef0e8b5e79`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:32 GMT
ADD file:90344130400909b0ad12bb54d439b0e4868fc5863f538f676e6fdfeaeb4dad51 in / 
# Tue, 23 Aug 2022 01:52:33 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:41:18 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Aug 2022 02:41:19 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 23 Aug 2022 02:41:27 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:41:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 23 Aug 2022 02:41:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Aug 2022 02:41:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:41:39 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 23 Aug 2022 02:41:40 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 23 Aug 2022 02:41:54 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 23 Aug 2022 02:41:55 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 23 Aug 2022 02:41:56 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 23 Aug 2022 02:41:57 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 23 Aug 2022 02:41:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 02:41:58 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 23 Aug 2022 02:41:59 GMT
VOLUME [/opt/couchdb/data]
# Tue, 23 Aug 2022 02:42:00 GMT
EXPOSE 4369 5984 9100
# Tue, 23 Aug 2022 02:42:01 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5b142346550416c75ea412d21741de5eaf3e76857affc12fab789277f81f53b3`  
		Last Modified: Tue, 23 Aug 2022 01:58:00 GMT  
		Size: 30.1 MB (30063788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccbd79e228edbe69f8a44334e50d429a18061f0239429d19a33333976b06b697`  
		Last Modified: Tue, 23 Aug 2022 02:43:55 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5faf2f8f02c86decd5a299b67198f7001620cdbe7409ee397941bc3280ea47b6`  
		Last Modified: Tue, 23 Aug 2022 02:43:53 GMT  
		Size: 5.0 MB (5003118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a100aefaee87a675ab1fcd77b424bbe4d314cd35b7ff1359aa20357f193f3bb`  
		Last Modified: Tue, 23 Aug 2022 02:43:53 GMT  
		Size: 1.2 MB (1221129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2a7049f73cfc2c74e858838e3a2476a8b02f624ef7bcf53500fa9921b639e6`  
		Last Modified: Tue, 23 Aug 2022 02:43:52 GMT  
		Size: 79.2 KB (79238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6abed586ad7658064e2b6c7e5ccb73d97836f1f9a9c2c520d89ff0b6cd42a86`  
		Last Modified: Tue, 23 Aug 2022 02:43:52 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702725e61d0a899ca0e4cc0f6264bcfbf981d746cd11b14cd9adb4d55311cdd3`  
		Last Modified: Tue, 23 Aug 2022 02:43:56 GMT  
		Size: 49.1 MB (49053612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577dc8a06cb9dd6a2b71c42b254ea430b73a89d9673eec153724c4035461b972`  
		Last Modified: Tue, 23 Aug 2022 02:43:50 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdfb633a0e999a120e07ab13dd4a271c89abc50ba0b1cc05f69ebc9807dc595c`  
		Last Modified: Tue, 23 Aug 2022 02:43:50 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733afa24355b799fab783ce0b9d05020b614c41fd2c8df9e9b80c2c122d78040`  
		Last Modified: Tue, 23 Aug 2022 02:43:50 GMT  
		Size: 2.2 KB (2184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89826adedb524d807efacca054272109deaadb4c4d49e3b01178bc77cc22c8e9`  
		Last Modified: Tue, 23 Aug 2022 02:43:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:c4593b957d4d6b0673ce80333e06dbe8c9df8c0a2b50642f6476a4858300bbbd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93220963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:506dd60f062d9201502e2c98c3d35ade4544ae5cbe15f325dbe7972922d9cb9c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 23 Aug 2022 01:24:52 GMT
ADD file:d35213360d726a18e220276d33f245115c3e94a321addaa4c9127488368b0203 in / 
# Tue, 23 Aug 2022 01:24:54 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:49:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Aug 2022 01:49:44 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 23 Aug 2022 01:49:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 01:50:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 23 Aug 2022 01:50:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Aug 2022 01:50:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 01:50:19 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 23 Aug 2022 01:50:20 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 23 Aug 2022 01:50:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 23 Aug 2022 01:50:44 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 23 Aug 2022 01:50:44 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 23 Aug 2022 01:50:45 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 23 Aug 2022 01:50:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 01:50:46 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 23 Aug 2022 01:50:46 GMT
VOLUME [/opt/couchdb/data]
# Tue, 23 Aug 2022 01:50:47 GMT
EXPOSE 4369 5984 9100
# Tue, 23 Aug 2022 01:50:47 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:698954eda09d38dd1ccc9ce777b1f6bc7f7473fc6c4c3eb634acc8d035a42eae`  
		Last Modified: Tue, 23 Aug 2022 01:30:36 GMT  
		Size: 35.3 MB (35284280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d3c6587d3e9e92bc112e6a45e7e2d23f0ba9b33296f897a5e3b742401c969c`  
		Last Modified: Tue, 23 Aug 2022 01:51:11 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d780cea1662edc02a54c96fbf73b475ba3e9d57bd3b0570ea910b10cdea373`  
		Last Modified: Tue, 23 Aug 2022 01:51:11 GMT  
		Size: 6.0 MB (6043740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16a08759b9582b5c4a2fc94291d78b0948e6a2c7ff31aea12ba846a4d4aeec4`  
		Last Modified: Tue, 23 Aug 2022 01:51:09 GMT  
		Size: 1.5 MB (1509146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ef44af8ab46bf8c9289fce53bb3a6767ac9629aeb0abb598002eff42db6209`  
		Last Modified: Tue, 23 Aug 2022 01:51:09 GMT  
		Size: 295.5 KB (295491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d42deef8dfffdeae7ce4d406952d8609194892ed34c53b72938c3eacd987b03`  
		Last Modified: Tue, 23 Aug 2022 01:51:08 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97398d4a6ae8504282205e3e95ace3d23991b43691fb7c504cadfb2b13c605aa`  
		Last Modified: Tue, 23 Aug 2022 01:51:15 GMT  
		Size: 50.1 MB (50081169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06dd8436859b528b48825799e3e9e283dbac690eda924186f9eb95eeb9833256`  
		Last Modified: Tue, 23 Aug 2022 01:51:06 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2452eb5653f4e46ce95453a458883d6038c787d15685cc2e731257709186dd1`  
		Last Modified: Tue, 23 Aug 2022 01:51:06 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:043e2bed131252232d4707dc336f0ce88ca531ea0b434c0233c5558f18702dbd`  
		Last Modified: Tue, 23 Aug 2022 01:51:06 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b55c10d8dce9821c6500c4e880e9001cabaee0835f3a3547eb8bcfb47f7d54`  
		Last Modified: Tue, 23 Aug 2022 01:51:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:2edaf1d979c8e78884067dfdaa349036c25170895935ebdf4bf4666f17979130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:56f710e313037efd3c25fa4b49915b84d702a31381fc38a43762e6bac60c74a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80004867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48f1d73bb2abbf3e60211207f5d416c139ea8d36c4bf9360874811baabfbca6`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:48 GMT
ADD file:782d864aa72c2d5fb599311ebae56db4067d2e91ff532c1aaf1a291c3dbce5bb in / 
# Tue, 13 Sep 2022 00:56:49 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 03:54:33 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Sep 2022 03:54:34 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 13 Sep 2022 03:54:41 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 03:54:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 13 Sep 2022 03:54:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Sep 2022 03:54:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 03:54:51 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 13 Sep 2022 03:54:52 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 13 Sep 2022 03:55:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 13 Sep 2022 03:55:06 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 13 Sep 2022 03:55:06 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 13 Sep 2022 03:55:06 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 13 Sep 2022 03:55:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 13 Sep 2022 03:55:07 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 03:55:07 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Sep 2022 03:55:07 GMT
EXPOSE 4369 5984 9100
# Tue, 13 Sep 2022 03:55:07 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4b7b4a8876e2f677668e51b8473f97a237d3d4df201b9df4031bcaa8068370b1`  
		Last Modified: Tue, 13 Sep 2022 01:01:16 GMT  
		Size: 27.1 MB (27130552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c088c3a03bf60b8f0b3b24363efbc28aef3c87451537b97521bfbf1f2aa13199`  
		Last Modified: Tue, 13 Sep 2022 03:56:21 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e6c9d6ee4b135545b364dd8b30be2b91e27e6b1e62addf07801a90a90ac96f`  
		Last Modified: Tue, 13 Sep 2022 03:56:20 GMT  
		Size: 6.7 MB (6698707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e1633127944965c144a64754b6a92bf6622c1de73c33716a59ca7f9ef1baca`  
		Last Modified: Tue, 13 Sep 2022 03:56:19 GMT  
		Size: 1.3 MB (1258362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61a40f9af1917164479b4fc40fc1f8fa2db40005957a46bb7b167f3a6f2724c`  
		Last Modified: Tue, 13 Sep 2022 03:56:18 GMT  
		Size: 293.1 KB (293062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7eae00d81a619c1b8d71dc8e8b6a2318e06ce5afeafd58b6b0d9552f09261d2`  
		Last Modified: Tue, 13 Sep 2022 03:56:18 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75278761418a6e65c5ef254f72d0a496d0637be7e24631aa0fc31e7e365c080d`  
		Last Modified: Tue, 13 Sep 2022 03:56:21 GMT  
		Size: 44.6 MB (44617172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a5b505f864f3542ade296e07b2aeddd0672c1c1e23b3274b9a3a4f9db90256a`  
		Last Modified: Tue, 13 Sep 2022 03:56:17 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5311452d93f303af98096fadb36f8010feea220fb6988b8ccb03e4de55fde725`  
		Last Modified: Tue, 13 Sep 2022 03:56:16 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27cc94873d6f1ffc6ef99804d2418b5444f939646feac9f991cf58c41442b91e`  
		Last Modified: Tue, 13 Sep 2022 03:56:16 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81cfa86b5c94ad137436fdbbbe1db947123cedb91147470f17111fc67173907`  
		Last Modified: Tue, 13 Sep 2022 03:56:16 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:46b8d5fb7b83c77a1c73b5152e652819d498e40bf7f809935d8e429a7fd5950e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74620747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01eb781740cc94a0c8f7226d222690682c8b10fa63a75c944e39bd3dd1717687`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:58 GMT
ADD file:4c5bca2d158b11314fb47a6d4b34239575621c2f00f92e77870f23aa02913fac in / 
# Tue, 23 Aug 2022 01:52:59 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:42:10 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Aug 2022 02:42:11 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 23 Aug 2022 02:42:19 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:42:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 23 Aug 2022 02:42:24 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Aug 2022 02:42:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:42:32 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 23 Aug 2022 02:42:33 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 23 Aug 2022 02:42:47 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 23 Aug 2022 02:42:48 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 23 Aug 2022 02:42:49 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 23 Aug 2022 02:42:50 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 23 Aug 2022 02:42:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 02:42:51 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 23 Aug 2022 02:42:52 GMT
VOLUME [/opt/couchdb/data]
# Tue, 23 Aug 2022 02:42:53 GMT
EXPOSE 4369 5984 9100
# Tue, 23 Aug 2022 02:42:54 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a84b81edbdb892b3702892bbb01c240695b0b9d619fda43a9b951c9d2df1443c`  
		Last Modified: Tue, 23 Aug 2022 01:58:50 GMT  
		Size: 25.9 MB (25912515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0f4e940c5871c8fab3c016b817ff8d6306da1ba35e200a5b45893fa56340a9`  
		Last Modified: Tue, 23 Aug 2022 02:44:20 GMT  
		Size: 3.3 KB (3319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd1d4c0f7d1b0bb90aa98f52f1bac0c37707c2d190cd73ea9c79dab071dda83f`  
		Last Modified: Tue, 23 Aug 2022 02:44:19 GMT  
		Size: 6.6 MB (6557176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90567554c16513f656919984d64a7cb938885d7229581719d411c0887c3f2987`  
		Last Modified: Tue, 23 Aug 2022 02:44:18 GMT  
		Size: 951.2 KB (951189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd12be703c9cae124252cac51aa545e6dd67c898c1258761b7e389f252eb8abc`  
		Last Modified: Tue, 23 Aug 2022 02:44:17 GMT  
		Size: 80.0 KB (79956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83bf954f555f8aa929f99d3f184f092d3883b1d7ebce40502c08656122bad4a1`  
		Last Modified: Tue, 23 Aug 2022 02:44:17 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff1d869c4ee5dd1f5e9faa4cfea4cc0aa882fa0882905583de2c2f90477a659`  
		Last Modified: Tue, 23 Aug 2022 02:44:20 GMT  
		Size: 41.1 MB (41112997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf38547a15a3116a082636938cd6e5c4d570cf60189c862dbd3f81f5d8fb947e`  
		Last Modified: Tue, 23 Aug 2022 02:44:15 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485c08eb4d6f9603dfb2e1c028858fd04e7f545a63ecc3683d69e02126d2d5ae`  
		Last Modified: Tue, 23 Aug 2022 02:44:15 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd0f87221915f7eec5878ce611d0f3012e08e4fd9f9fd4ca062a0a2a9212b6d`  
		Last Modified: Tue, 23 Aug 2022 02:44:15 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674454ba2adcb31bfeff9fc2a1e3f9a40fde7c17a7e90ed3b6ab8e82d8e2e7ea`  
		Last Modified: Tue, 23 Aug 2022 02:44:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1.2`

```console
$ docker pull couchdb@sha256:2edaf1d979c8e78884067dfdaa349036c25170895935ebdf4bf4666f17979130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1.2` - linux; amd64

```console
$ docker pull couchdb@sha256:56f710e313037efd3c25fa4b49915b84d702a31381fc38a43762e6bac60c74a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80004867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48f1d73bb2abbf3e60211207f5d416c139ea8d36c4bf9360874811baabfbca6`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:48 GMT
ADD file:782d864aa72c2d5fb599311ebae56db4067d2e91ff532c1aaf1a291c3dbce5bb in / 
# Tue, 13 Sep 2022 00:56:49 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 03:54:33 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Sep 2022 03:54:34 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 13 Sep 2022 03:54:41 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 03:54:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 13 Sep 2022 03:54:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Sep 2022 03:54:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 03:54:51 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 13 Sep 2022 03:54:52 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 13 Sep 2022 03:55:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 13 Sep 2022 03:55:06 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 13 Sep 2022 03:55:06 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 13 Sep 2022 03:55:06 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 13 Sep 2022 03:55:07 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 13 Sep 2022 03:55:07 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 03:55:07 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Sep 2022 03:55:07 GMT
EXPOSE 4369 5984 9100
# Tue, 13 Sep 2022 03:55:07 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:4b7b4a8876e2f677668e51b8473f97a237d3d4df201b9df4031bcaa8068370b1`  
		Last Modified: Tue, 13 Sep 2022 01:01:16 GMT  
		Size: 27.1 MB (27130552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c088c3a03bf60b8f0b3b24363efbc28aef3c87451537b97521bfbf1f2aa13199`  
		Last Modified: Tue, 13 Sep 2022 03:56:21 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e6c9d6ee4b135545b364dd8b30be2b91e27e6b1e62addf07801a90a90ac96f`  
		Last Modified: Tue, 13 Sep 2022 03:56:20 GMT  
		Size: 6.7 MB (6698707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e1633127944965c144a64754b6a92bf6622c1de73c33716a59ca7f9ef1baca`  
		Last Modified: Tue, 13 Sep 2022 03:56:19 GMT  
		Size: 1.3 MB (1258362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61a40f9af1917164479b4fc40fc1f8fa2db40005957a46bb7b167f3a6f2724c`  
		Last Modified: Tue, 13 Sep 2022 03:56:18 GMT  
		Size: 293.1 KB (293062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7eae00d81a619c1b8d71dc8e8b6a2318e06ce5afeafd58b6b0d9552f09261d2`  
		Last Modified: Tue, 13 Sep 2022 03:56:18 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75278761418a6e65c5ef254f72d0a496d0637be7e24631aa0fc31e7e365c080d`  
		Last Modified: Tue, 13 Sep 2022 03:56:21 GMT  
		Size: 44.6 MB (44617172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a5b505f864f3542ade296e07b2aeddd0672c1c1e23b3274b9a3a4f9db90256a`  
		Last Modified: Tue, 13 Sep 2022 03:56:17 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5311452d93f303af98096fadb36f8010feea220fb6988b8ccb03e4de55fde725`  
		Last Modified: Tue, 13 Sep 2022 03:56:16 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27cc94873d6f1ffc6ef99804d2418b5444f939646feac9f991cf58c41442b91e`  
		Last Modified: Tue, 13 Sep 2022 03:56:16 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81cfa86b5c94ad137436fdbbbe1db947123cedb91147470f17111fc67173907`  
		Last Modified: Tue, 13 Sep 2022 03:56:16 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:46b8d5fb7b83c77a1c73b5152e652819d498e40bf7f809935d8e429a7fd5950e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74620747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01eb781740cc94a0c8f7226d222690682c8b10fa63a75c944e39bd3dd1717687`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:58 GMT
ADD file:4c5bca2d158b11314fb47a6d4b34239575621c2f00f92e77870f23aa02913fac in / 
# Tue, 23 Aug 2022 01:52:59 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:42:10 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Aug 2022 02:42:11 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 23 Aug 2022 02:42:19 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:42:23 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 23 Aug 2022 02:42:24 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Aug 2022 02:42:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:42:32 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 23 Aug 2022 02:42:33 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 23 Aug 2022 02:42:47 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 23 Aug 2022 02:42:48 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 23 Aug 2022 02:42:49 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 23 Aug 2022 02:42:50 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 23 Aug 2022 02:42:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 02:42:51 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 23 Aug 2022 02:42:52 GMT
VOLUME [/opt/couchdb/data]
# Tue, 23 Aug 2022 02:42:53 GMT
EXPOSE 4369 5984 9100
# Tue, 23 Aug 2022 02:42:54 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:a84b81edbdb892b3702892bbb01c240695b0b9d619fda43a9b951c9d2df1443c`  
		Last Modified: Tue, 23 Aug 2022 01:58:50 GMT  
		Size: 25.9 MB (25912515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0f4e940c5871c8fab3c016b817ff8d6306da1ba35e200a5b45893fa56340a9`  
		Last Modified: Tue, 23 Aug 2022 02:44:20 GMT  
		Size: 3.3 KB (3319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd1d4c0f7d1b0bb90aa98f52f1bac0c37707c2d190cd73ea9c79dab071dda83f`  
		Last Modified: Tue, 23 Aug 2022 02:44:19 GMT  
		Size: 6.6 MB (6557176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90567554c16513f656919984d64a7cb938885d7229581719d411c0887c3f2987`  
		Last Modified: Tue, 23 Aug 2022 02:44:18 GMT  
		Size: 951.2 KB (951189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd12be703c9cae124252cac51aa545e6dd67c898c1258761b7e389f252eb8abc`  
		Last Modified: Tue, 23 Aug 2022 02:44:17 GMT  
		Size: 80.0 KB (79956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83bf954f555f8aa929f99d3f184f092d3883b1d7ebce40502c08656122bad4a1`  
		Last Modified: Tue, 23 Aug 2022 02:44:17 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff1d869c4ee5dd1f5e9faa4cfea4cc0aa882fa0882905583de2c2f90477a659`  
		Last Modified: Tue, 23 Aug 2022 02:44:20 GMT  
		Size: 41.1 MB (41112997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf38547a15a3116a082636938cd6e5c4d570cf60189c862dbd3f81f5d8fb947e`  
		Last Modified: Tue, 23 Aug 2022 02:44:15 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485c08eb4d6f9603dfb2e1c028858fd04e7f545a63ecc3683d69e02126d2d5ae`  
		Last Modified: Tue, 23 Aug 2022 02:44:15 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd0f87221915f7eec5878ce611d0f3012e08e4fd9f9fd4ca062a0a2a9212b6d`  
		Last Modified: Tue, 23 Aug 2022 02:44:15 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674454ba2adcb31bfeff9fc2a1e3f9a40fde7c17a7e90ed3b6ab8e82d8e2e7ea`  
		Last Modified: Tue, 23 Aug 2022 02:44:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2`

```console
$ docker pull couchdb@sha256:b8f1266f877d094bf16126713c8e7e8a91688bb5311826fa779cad3972387a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:ac5c57c4df9f9d0129390f652b62dfa348a1b383c458841010ad52abbb6c8f0b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87530196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9292db79eb5d3107963496f664c9764d4974a423cff1612702d8ca782a888f5`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 03:53:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Sep 2022 03:54:00 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 13 Sep 2022 03:54:07 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 03:54:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 13 Sep 2022 03:54:10 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Sep 2022 03:54:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 03:54:16 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 13 Sep 2022 03:54:16 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 13 Sep 2022 03:54:29 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 13 Sep 2022 03:54:30 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 13 Sep 2022 03:54:30 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 13 Sep 2022 03:54:30 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 13 Sep 2022 03:54:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 13 Sep 2022 03:54:30 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 03:54:31 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Sep 2022 03:54:31 GMT
EXPOSE 4369 5984 9100
# Tue, 13 Sep 2022 03:54:31 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9775a4fbb4b5564bbc1ec8e077d317b8745a7598e059365241ddc1a9766c129c`  
		Last Modified: Tue, 13 Sep 2022 03:55:55 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d707a0a4de816f6a35046bed27c3bd025081394b651fd4b339188a4e19967c4`  
		Last Modified: Tue, 13 Sep 2022 03:55:54 GMT  
		Size: 5.2 MB (5224215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15634eb84187cbacfe864298c664c5eb740aa1a455a39e64f4f6a94c0f07a14`  
		Last Modified: Tue, 13 Sep 2022 03:55:53 GMT  
		Size: 1.6 MB (1553277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59f0fe4ba863352dbd7372301d2eae5be8cd69838e66876a65c5c0b1666de8c`  
		Last Modified: Tue, 13 Sep 2022 03:55:53 GMT  
		Size: 295.6 KB (295573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f507b233637bff8bdab3e80909e9dcdcc02a11efcca3f242c4ae8bf410296bbe`  
		Last Modified: Tue, 13 Sep 2022 03:55:53 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a76624d812c6c764f46d961f80510fa92e7512419c528ba6ab86e250d365d8`  
		Last Modified: Tue, 13 Sep 2022 03:55:56 GMT  
		Size: 49.0 MB (49045868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6166f23a925f2a6a18aa9efa186271f01020d8fd5d40d7a307cb02d6172974`  
		Last Modified: Tue, 13 Sep 2022 03:55:50 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc867e39bf60d67febf095d33500f8b30b51f6edbef26bd9d37b7a38a9bfaebc`  
		Last Modified: Tue, 13 Sep 2022 03:55:50 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5bc74ba5f149b1005fb23f07d5b84e4946fc31381d124892f99322b8c9a202`  
		Last Modified: Tue, 13 Sep 2022 03:55:50 GMT  
		Size: 2.2 KB (2187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ff75922f5a116b20c00eabe11b5280455fc7c77595f4ae03ed74a4e45ffb41`  
		Last Modified: Tue, 13 Sep 2022 03:55:50 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:6d7e5cb02dcd01b68f68dfd7b1572a8b2951615b4a359edb3aaebac20fc5d332
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85427934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e92099630042247528b18325ac126f4af5e138e14f74de8f499e49ef0e8b5e79`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:32 GMT
ADD file:90344130400909b0ad12bb54d439b0e4868fc5863f538f676e6fdfeaeb4dad51 in / 
# Tue, 23 Aug 2022 01:52:33 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:41:18 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Aug 2022 02:41:19 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 23 Aug 2022 02:41:27 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:41:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 23 Aug 2022 02:41:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Aug 2022 02:41:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:41:39 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 23 Aug 2022 02:41:40 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 23 Aug 2022 02:41:54 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 23 Aug 2022 02:41:55 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 23 Aug 2022 02:41:56 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 23 Aug 2022 02:41:57 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 23 Aug 2022 02:41:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 02:41:58 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 23 Aug 2022 02:41:59 GMT
VOLUME [/opt/couchdb/data]
# Tue, 23 Aug 2022 02:42:00 GMT
EXPOSE 4369 5984 9100
# Tue, 23 Aug 2022 02:42:01 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5b142346550416c75ea412d21741de5eaf3e76857affc12fab789277f81f53b3`  
		Last Modified: Tue, 23 Aug 2022 01:58:00 GMT  
		Size: 30.1 MB (30063788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccbd79e228edbe69f8a44334e50d429a18061f0239429d19a33333976b06b697`  
		Last Modified: Tue, 23 Aug 2022 02:43:55 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5faf2f8f02c86decd5a299b67198f7001620cdbe7409ee397941bc3280ea47b6`  
		Last Modified: Tue, 23 Aug 2022 02:43:53 GMT  
		Size: 5.0 MB (5003118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a100aefaee87a675ab1fcd77b424bbe4d314cd35b7ff1359aa20357f193f3bb`  
		Last Modified: Tue, 23 Aug 2022 02:43:53 GMT  
		Size: 1.2 MB (1221129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2a7049f73cfc2c74e858838e3a2476a8b02f624ef7bcf53500fa9921b639e6`  
		Last Modified: Tue, 23 Aug 2022 02:43:52 GMT  
		Size: 79.2 KB (79238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6abed586ad7658064e2b6c7e5ccb73d97836f1f9a9c2c520d89ff0b6cd42a86`  
		Last Modified: Tue, 23 Aug 2022 02:43:52 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702725e61d0a899ca0e4cc0f6264bcfbf981d746cd11b14cd9adb4d55311cdd3`  
		Last Modified: Tue, 23 Aug 2022 02:43:56 GMT  
		Size: 49.1 MB (49053612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577dc8a06cb9dd6a2b71c42b254ea430b73a89d9673eec153724c4035461b972`  
		Last Modified: Tue, 23 Aug 2022 02:43:50 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdfb633a0e999a120e07ab13dd4a271c89abc50ba0b1cc05f69ebc9807dc595c`  
		Last Modified: Tue, 23 Aug 2022 02:43:50 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733afa24355b799fab783ce0b9d05020b614c41fd2c8df9e9b80c2c122d78040`  
		Last Modified: Tue, 23 Aug 2022 02:43:50 GMT  
		Size: 2.2 KB (2184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89826adedb524d807efacca054272109deaadb4c4d49e3b01178bc77cc22c8e9`  
		Last Modified: Tue, 23 Aug 2022 02:43:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2` - linux; ppc64le

```console
$ docker pull couchdb@sha256:c4593b957d4d6b0673ce80333e06dbe8c9df8c0a2b50642f6476a4858300bbbd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93220963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:506dd60f062d9201502e2c98c3d35ade4544ae5cbe15f325dbe7972922d9cb9c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 23 Aug 2022 01:24:52 GMT
ADD file:d35213360d726a18e220276d33f245115c3e94a321addaa4c9127488368b0203 in / 
# Tue, 23 Aug 2022 01:24:54 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:49:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Aug 2022 01:49:44 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 23 Aug 2022 01:49:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 01:50:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 23 Aug 2022 01:50:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Aug 2022 01:50:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 01:50:19 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 23 Aug 2022 01:50:20 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 23 Aug 2022 01:50:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 23 Aug 2022 01:50:44 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 23 Aug 2022 01:50:44 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 23 Aug 2022 01:50:45 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 23 Aug 2022 01:50:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 01:50:46 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 23 Aug 2022 01:50:46 GMT
VOLUME [/opt/couchdb/data]
# Tue, 23 Aug 2022 01:50:47 GMT
EXPOSE 4369 5984 9100
# Tue, 23 Aug 2022 01:50:47 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:698954eda09d38dd1ccc9ce777b1f6bc7f7473fc6c4c3eb634acc8d035a42eae`  
		Last Modified: Tue, 23 Aug 2022 01:30:36 GMT  
		Size: 35.3 MB (35284280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d3c6587d3e9e92bc112e6a45e7e2d23f0ba9b33296f897a5e3b742401c969c`  
		Last Modified: Tue, 23 Aug 2022 01:51:11 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d780cea1662edc02a54c96fbf73b475ba3e9d57bd3b0570ea910b10cdea373`  
		Last Modified: Tue, 23 Aug 2022 01:51:11 GMT  
		Size: 6.0 MB (6043740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16a08759b9582b5c4a2fc94291d78b0948e6a2c7ff31aea12ba846a4d4aeec4`  
		Last Modified: Tue, 23 Aug 2022 01:51:09 GMT  
		Size: 1.5 MB (1509146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ef44af8ab46bf8c9289fce53bb3a6767ac9629aeb0abb598002eff42db6209`  
		Last Modified: Tue, 23 Aug 2022 01:51:09 GMT  
		Size: 295.5 KB (295491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d42deef8dfffdeae7ce4d406952d8609194892ed34c53b72938c3eacd987b03`  
		Last Modified: Tue, 23 Aug 2022 01:51:08 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97398d4a6ae8504282205e3e95ace3d23991b43691fb7c504cadfb2b13c605aa`  
		Last Modified: Tue, 23 Aug 2022 01:51:15 GMT  
		Size: 50.1 MB (50081169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06dd8436859b528b48825799e3e9e283dbac690eda924186f9eb95eeb9833256`  
		Last Modified: Tue, 23 Aug 2022 01:51:06 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2452eb5653f4e46ce95453a458883d6038c787d15685cc2e731257709186dd1`  
		Last Modified: Tue, 23 Aug 2022 01:51:06 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:043e2bed131252232d4707dc336f0ce88ca531ea0b434c0233c5558f18702dbd`  
		Last Modified: Tue, 23 Aug 2022 01:51:06 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b55c10d8dce9821c6500c4e880e9001cabaee0835f3a3547eb8bcfb47f7d54`  
		Last Modified: Tue, 23 Aug 2022 01:51:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2.2`

```console
$ docker pull couchdb@sha256:b8f1266f877d094bf16126713c8e7e8a91688bb5311826fa779cad3972387a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.2.2` - linux; amd64

```console
$ docker pull couchdb@sha256:ac5c57c4df9f9d0129390f652b62dfa348a1b383c458841010ad52abbb6c8f0b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87530196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9292db79eb5d3107963496f664c9764d4974a423cff1612702d8ca782a888f5`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 03:53:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Sep 2022 03:54:00 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 13 Sep 2022 03:54:07 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 03:54:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 13 Sep 2022 03:54:10 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Sep 2022 03:54:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 03:54:16 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 13 Sep 2022 03:54:16 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 13 Sep 2022 03:54:29 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 13 Sep 2022 03:54:30 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 13 Sep 2022 03:54:30 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 13 Sep 2022 03:54:30 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 13 Sep 2022 03:54:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 13 Sep 2022 03:54:30 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 03:54:31 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Sep 2022 03:54:31 GMT
EXPOSE 4369 5984 9100
# Tue, 13 Sep 2022 03:54:31 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9775a4fbb4b5564bbc1ec8e077d317b8745a7598e059365241ddc1a9766c129c`  
		Last Modified: Tue, 13 Sep 2022 03:55:55 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d707a0a4de816f6a35046bed27c3bd025081394b651fd4b339188a4e19967c4`  
		Last Modified: Tue, 13 Sep 2022 03:55:54 GMT  
		Size: 5.2 MB (5224215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15634eb84187cbacfe864298c664c5eb740aa1a455a39e64f4f6a94c0f07a14`  
		Last Modified: Tue, 13 Sep 2022 03:55:53 GMT  
		Size: 1.6 MB (1553277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59f0fe4ba863352dbd7372301d2eae5be8cd69838e66876a65c5c0b1666de8c`  
		Last Modified: Tue, 13 Sep 2022 03:55:53 GMT  
		Size: 295.6 KB (295573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f507b233637bff8bdab3e80909e9dcdcc02a11efcca3f242c4ae8bf410296bbe`  
		Last Modified: Tue, 13 Sep 2022 03:55:53 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a76624d812c6c764f46d961f80510fa92e7512419c528ba6ab86e250d365d8`  
		Last Modified: Tue, 13 Sep 2022 03:55:56 GMT  
		Size: 49.0 MB (49045868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6166f23a925f2a6a18aa9efa186271f01020d8fd5d40d7a307cb02d6172974`  
		Last Modified: Tue, 13 Sep 2022 03:55:50 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc867e39bf60d67febf095d33500f8b30b51f6edbef26bd9d37b7a38a9bfaebc`  
		Last Modified: Tue, 13 Sep 2022 03:55:50 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5bc74ba5f149b1005fb23f07d5b84e4946fc31381d124892f99322b8c9a202`  
		Last Modified: Tue, 13 Sep 2022 03:55:50 GMT  
		Size: 2.2 KB (2187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ff75922f5a116b20c00eabe11b5280455fc7c77595f4ae03ed74a4e45ffb41`  
		Last Modified: Tue, 13 Sep 2022 03:55:50 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:6d7e5cb02dcd01b68f68dfd7b1572a8b2951615b4a359edb3aaebac20fc5d332
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85427934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e92099630042247528b18325ac126f4af5e138e14f74de8f499e49ef0e8b5e79`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:32 GMT
ADD file:90344130400909b0ad12bb54d439b0e4868fc5863f538f676e6fdfeaeb4dad51 in / 
# Tue, 23 Aug 2022 01:52:33 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:41:18 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Aug 2022 02:41:19 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 23 Aug 2022 02:41:27 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:41:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 23 Aug 2022 02:41:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Aug 2022 02:41:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:41:39 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 23 Aug 2022 02:41:40 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 23 Aug 2022 02:41:54 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 23 Aug 2022 02:41:55 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 23 Aug 2022 02:41:56 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 23 Aug 2022 02:41:57 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 23 Aug 2022 02:41:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 02:41:58 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 23 Aug 2022 02:41:59 GMT
VOLUME [/opt/couchdb/data]
# Tue, 23 Aug 2022 02:42:00 GMT
EXPOSE 4369 5984 9100
# Tue, 23 Aug 2022 02:42:01 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5b142346550416c75ea412d21741de5eaf3e76857affc12fab789277f81f53b3`  
		Last Modified: Tue, 23 Aug 2022 01:58:00 GMT  
		Size: 30.1 MB (30063788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccbd79e228edbe69f8a44334e50d429a18061f0239429d19a33333976b06b697`  
		Last Modified: Tue, 23 Aug 2022 02:43:55 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5faf2f8f02c86decd5a299b67198f7001620cdbe7409ee397941bc3280ea47b6`  
		Last Modified: Tue, 23 Aug 2022 02:43:53 GMT  
		Size: 5.0 MB (5003118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a100aefaee87a675ab1fcd77b424bbe4d314cd35b7ff1359aa20357f193f3bb`  
		Last Modified: Tue, 23 Aug 2022 02:43:53 GMT  
		Size: 1.2 MB (1221129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2a7049f73cfc2c74e858838e3a2476a8b02f624ef7bcf53500fa9921b639e6`  
		Last Modified: Tue, 23 Aug 2022 02:43:52 GMT  
		Size: 79.2 KB (79238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6abed586ad7658064e2b6c7e5ccb73d97836f1f9a9c2c520d89ff0b6cd42a86`  
		Last Modified: Tue, 23 Aug 2022 02:43:52 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702725e61d0a899ca0e4cc0f6264bcfbf981d746cd11b14cd9adb4d55311cdd3`  
		Last Modified: Tue, 23 Aug 2022 02:43:56 GMT  
		Size: 49.1 MB (49053612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577dc8a06cb9dd6a2b71c42b254ea430b73a89d9673eec153724c4035461b972`  
		Last Modified: Tue, 23 Aug 2022 02:43:50 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdfb633a0e999a120e07ab13dd4a271c89abc50ba0b1cc05f69ebc9807dc595c`  
		Last Modified: Tue, 23 Aug 2022 02:43:50 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733afa24355b799fab783ce0b9d05020b614c41fd2c8df9e9b80c2c122d78040`  
		Last Modified: Tue, 23 Aug 2022 02:43:50 GMT  
		Size: 2.2 KB (2184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89826adedb524d807efacca054272109deaadb4c4d49e3b01178bc77cc22c8e9`  
		Last Modified: Tue, 23 Aug 2022 02:43:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2.2` - linux; ppc64le

```console
$ docker pull couchdb@sha256:c4593b957d4d6b0673ce80333e06dbe8c9df8c0a2b50642f6476a4858300bbbd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93220963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:506dd60f062d9201502e2c98c3d35ade4544ae5cbe15f325dbe7972922d9cb9c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 23 Aug 2022 01:24:52 GMT
ADD file:d35213360d726a18e220276d33f245115c3e94a321addaa4c9127488368b0203 in / 
# Tue, 23 Aug 2022 01:24:54 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:49:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Aug 2022 01:49:44 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 23 Aug 2022 01:49:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 01:50:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 23 Aug 2022 01:50:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Aug 2022 01:50:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 01:50:19 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 23 Aug 2022 01:50:20 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 23 Aug 2022 01:50:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 23 Aug 2022 01:50:44 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 23 Aug 2022 01:50:44 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 23 Aug 2022 01:50:45 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 23 Aug 2022 01:50:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 01:50:46 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 23 Aug 2022 01:50:46 GMT
VOLUME [/opt/couchdb/data]
# Tue, 23 Aug 2022 01:50:47 GMT
EXPOSE 4369 5984 9100
# Tue, 23 Aug 2022 01:50:47 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:698954eda09d38dd1ccc9ce777b1f6bc7f7473fc6c4c3eb634acc8d035a42eae`  
		Last Modified: Tue, 23 Aug 2022 01:30:36 GMT  
		Size: 35.3 MB (35284280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d3c6587d3e9e92bc112e6a45e7e2d23f0ba9b33296f897a5e3b742401c969c`  
		Last Modified: Tue, 23 Aug 2022 01:51:11 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d780cea1662edc02a54c96fbf73b475ba3e9d57bd3b0570ea910b10cdea373`  
		Last Modified: Tue, 23 Aug 2022 01:51:11 GMT  
		Size: 6.0 MB (6043740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16a08759b9582b5c4a2fc94291d78b0948e6a2c7ff31aea12ba846a4d4aeec4`  
		Last Modified: Tue, 23 Aug 2022 01:51:09 GMT  
		Size: 1.5 MB (1509146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ef44af8ab46bf8c9289fce53bb3a6767ac9629aeb0abb598002eff42db6209`  
		Last Modified: Tue, 23 Aug 2022 01:51:09 GMT  
		Size: 295.5 KB (295491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d42deef8dfffdeae7ce4d406952d8609194892ed34c53b72938c3eacd987b03`  
		Last Modified: Tue, 23 Aug 2022 01:51:08 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97398d4a6ae8504282205e3e95ace3d23991b43691fb7c504cadfb2b13c605aa`  
		Last Modified: Tue, 23 Aug 2022 01:51:15 GMT  
		Size: 50.1 MB (50081169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06dd8436859b528b48825799e3e9e283dbac690eda924186f9eb95eeb9833256`  
		Last Modified: Tue, 23 Aug 2022 01:51:06 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2452eb5653f4e46ce95453a458883d6038c787d15685cc2e731257709186dd1`  
		Last Modified: Tue, 23 Aug 2022 01:51:06 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:043e2bed131252232d4707dc336f0ce88ca531ea0b434c0233c5558f18702dbd`  
		Last Modified: Tue, 23 Aug 2022 01:51:06 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b55c10d8dce9821c6500c4e880e9001cabaee0835f3a3547eb8bcfb47f7d54`  
		Last Modified: Tue, 23 Aug 2022 01:51:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:b8f1266f877d094bf16126713c8e7e8a91688bb5311826fa779cad3972387a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:ac5c57c4df9f9d0129390f652b62dfa348a1b383c458841010ad52abbb6c8f0b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87530196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9292db79eb5d3107963496f664c9764d4974a423cff1612702d8ca782a888f5`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 03:53:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 13 Sep 2022 03:54:00 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 13 Sep 2022 03:54:07 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 03:54:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 13 Sep 2022 03:54:10 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 13 Sep 2022 03:54:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 03:54:16 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 13 Sep 2022 03:54:16 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 13 Sep 2022 03:54:29 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 13 Sep 2022 03:54:30 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 13 Sep 2022 03:54:30 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 13 Sep 2022 03:54:30 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 13 Sep 2022 03:54:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 13 Sep 2022 03:54:30 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 03:54:31 GMT
VOLUME [/opt/couchdb/data]
# Tue, 13 Sep 2022 03:54:31 GMT
EXPOSE 4369 5984 9100
# Tue, 13 Sep 2022 03:54:31 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9775a4fbb4b5564bbc1ec8e077d317b8745a7598e059365241ddc1a9766c129c`  
		Last Modified: Tue, 13 Sep 2022 03:55:55 GMT  
		Size: 3.4 KB (3413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d707a0a4de816f6a35046bed27c3bd025081394b651fd4b339188a4e19967c4`  
		Last Modified: Tue, 13 Sep 2022 03:55:54 GMT  
		Size: 5.2 MB (5224215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15634eb84187cbacfe864298c664c5eb740aa1a455a39e64f4f6a94c0f07a14`  
		Last Modified: Tue, 13 Sep 2022 03:55:53 GMT  
		Size: 1.6 MB (1553277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59f0fe4ba863352dbd7372301d2eae5be8cd69838e66876a65c5c0b1666de8c`  
		Last Modified: Tue, 13 Sep 2022 03:55:53 GMT  
		Size: 295.6 KB (295573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f507b233637bff8bdab3e80909e9dcdcc02a11efcca3f242c4ae8bf410296bbe`  
		Last Modified: Tue, 13 Sep 2022 03:55:53 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a76624d812c6c764f46d961f80510fa92e7512419c528ba6ab86e250d365d8`  
		Last Modified: Tue, 13 Sep 2022 03:55:56 GMT  
		Size: 49.0 MB (49045868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6166f23a925f2a6a18aa9efa186271f01020d8fd5d40d7a307cb02d6172974`  
		Last Modified: Tue, 13 Sep 2022 03:55:50 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc867e39bf60d67febf095d33500f8b30b51f6edbef26bd9d37b7a38a9bfaebc`  
		Last Modified: Tue, 13 Sep 2022 03:55:50 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5bc74ba5f149b1005fb23f07d5b84e4946fc31381d124892f99322b8c9a202`  
		Last Modified: Tue, 13 Sep 2022 03:55:50 GMT  
		Size: 2.2 KB (2187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ff75922f5a116b20c00eabe11b5280455fc7c77595f4ae03ed74a4e45ffb41`  
		Last Modified: Tue, 13 Sep 2022 03:55:50 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:6d7e5cb02dcd01b68f68dfd7b1572a8b2951615b4a359edb3aaebac20fc5d332
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85427934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e92099630042247528b18325ac126f4af5e138e14f74de8f499e49ef0e8b5e79`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:32 GMT
ADD file:90344130400909b0ad12bb54d439b0e4868fc5863f538f676e6fdfeaeb4dad51 in / 
# Tue, 23 Aug 2022 01:52:33 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:41:18 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Aug 2022 02:41:19 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 23 Aug 2022 02:41:27 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:41:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 23 Aug 2022 02:41:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Aug 2022 02:41:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:41:39 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 23 Aug 2022 02:41:40 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 23 Aug 2022 02:41:54 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 23 Aug 2022 02:41:55 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 23 Aug 2022 02:41:56 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 23 Aug 2022 02:41:57 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 23 Aug 2022 02:41:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 02:41:58 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 23 Aug 2022 02:41:59 GMT
VOLUME [/opt/couchdb/data]
# Tue, 23 Aug 2022 02:42:00 GMT
EXPOSE 4369 5984 9100
# Tue, 23 Aug 2022 02:42:01 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5b142346550416c75ea412d21741de5eaf3e76857affc12fab789277f81f53b3`  
		Last Modified: Tue, 23 Aug 2022 01:58:00 GMT  
		Size: 30.1 MB (30063788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccbd79e228edbe69f8a44334e50d429a18061f0239429d19a33333976b06b697`  
		Last Modified: Tue, 23 Aug 2022 02:43:55 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5faf2f8f02c86decd5a299b67198f7001620cdbe7409ee397941bc3280ea47b6`  
		Last Modified: Tue, 23 Aug 2022 02:43:53 GMT  
		Size: 5.0 MB (5003118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a100aefaee87a675ab1fcd77b424bbe4d314cd35b7ff1359aa20357f193f3bb`  
		Last Modified: Tue, 23 Aug 2022 02:43:53 GMT  
		Size: 1.2 MB (1221129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2a7049f73cfc2c74e858838e3a2476a8b02f624ef7bcf53500fa9921b639e6`  
		Last Modified: Tue, 23 Aug 2022 02:43:52 GMT  
		Size: 79.2 KB (79238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6abed586ad7658064e2b6c7e5ccb73d97836f1f9a9c2c520d89ff0b6cd42a86`  
		Last Modified: Tue, 23 Aug 2022 02:43:52 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702725e61d0a899ca0e4cc0f6264bcfbf981d746cd11b14cd9adb4d55311cdd3`  
		Last Modified: Tue, 23 Aug 2022 02:43:56 GMT  
		Size: 49.1 MB (49053612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577dc8a06cb9dd6a2b71c42b254ea430b73a89d9673eec153724c4035461b972`  
		Last Modified: Tue, 23 Aug 2022 02:43:50 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdfb633a0e999a120e07ab13dd4a271c89abc50ba0b1cc05f69ebc9807dc595c`  
		Last Modified: Tue, 23 Aug 2022 02:43:50 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733afa24355b799fab783ce0b9d05020b614c41fd2c8df9e9b80c2c122d78040`  
		Last Modified: Tue, 23 Aug 2022 02:43:50 GMT  
		Size: 2.2 KB (2184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89826adedb524d807efacca054272109deaadb4c4d49e3b01178bc77cc22c8e9`  
		Last Modified: Tue, 23 Aug 2022 02:43:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:c4593b957d4d6b0673ce80333e06dbe8c9df8c0a2b50642f6476a4858300bbbd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93220963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:506dd60f062d9201502e2c98c3d35ade4544ae5cbe15f325dbe7972922d9cb9c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 23 Aug 2022 01:24:52 GMT
ADD file:d35213360d726a18e220276d33f245115c3e94a321addaa4c9127488368b0203 in / 
# Tue, 23 Aug 2022 01:24:54 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 01:49:43 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Aug 2022 01:49:44 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 23 Aug 2022 01:49:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 01:50:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 23 Aug 2022 01:50:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Aug 2022 01:50:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 01:50:19 GMT
ENV COUCHDB_VERSION=3.2.2
# Tue, 23 Aug 2022 01:50:20 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 23 Aug 2022 01:50:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 23 Aug 2022 01:50:44 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 23 Aug 2022 01:50:44 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 23 Aug 2022 01:50:45 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 23 Aug 2022 01:50:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 23 Aug 2022 01:50:46 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 23 Aug 2022 01:50:46 GMT
VOLUME [/opt/couchdb/data]
# Tue, 23 Aug 2022 01:50:47 GMT
EXPOSE 4369 5984 9100
# Tue, 23 Aug 2022 01:50:47 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:698954eda09d38dd1ccc9ce777b1f6bc7f7473fc6c4c3eb634acc8d035a42eae`  
		Last Modified: Tue, 23 Aug 2022 01:30:36 GMT  
		Size: 35.3 MB (35284280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d3c6587d3e9e92bc112e6a45e7e2d23f0ba9b33296f897a5e3b742401c969c`  
		Last Modified: Tue, 23 Aug 2022 01:51:11 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d780cea1662edc02a54c96fbf73b475ba3e9d57bd3b0570ea910b10cdea373`  
		Last Modified: Tue, 23 Aug 2022 01:51:11 GMT  
		Size: 6.0 MB (6043740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16a08759b9582b5c4a2fc94291d78b0948e6a2c7ff31aea12ba846a4d4aeec4`  
		Last Modified: Tue, 23 Aug 2022 01:51:09 GMT  
		Size: 1.5 MB (1509146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ef44af8ab46bf8c9289fce53bb3a6767ac9629aeb0abb598002eff42db6209`  
		Last Modified: Tue, 23 Aug 2022 01:51:09 GMT  
		Size: 295.5 KB (295491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d42deef8dfffdeae7ce4d406952d8609194892ed34c53b72938c3eacd987b03`  
		Last Modified: Tue, 23 Aug 2022 01:51:08 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97398d4a6ae8504282205e3e95ace3d23991b43691fb7c504cadfb2b13c605aa`  
		Last Modified: Tue, 23 Aug 2022 01:51:15 GMT  
		Size: 50.1 MB (50081169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06dd8436859b528b48825799e3e9e283dbac690eda924186f9eb95eeb9833256`  
		Last Modified: Tue, 23 Aug 2022 01:51:06 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2452eb5653f4e46ce95453a458883d6038c787d15685cc2e731257709186dd1`  
		Last Modified: Tue, 23 Aug 2022 01:51:06 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:043e2bed131252232d4707dc336f0ce88ca531ea0b434c0233c5558f18702dbd`  
		Last Modified: Tue, 23 Aug 2022 01:51:06 GMT  
		Size: 2.2 KB (2185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b55c10d8dce9821c6500c4e880e9001cabaee0835f3a3547eb8bcfb47f7d54`  
		Last Modified: Tue, 23 Aug 2022 01:51:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
