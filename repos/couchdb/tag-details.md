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
-	[`couchdb:3.3.2`](#couchdb332)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:2`

```console
$ docker pull couchdb@sha256:35ac8511e5a6846aa8866a0c8d4c1850e324d3050e3e90fd6429797b93ffcc62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:84f72d8c5f4cf534af9a95af8c4a733abdecf8aee32b9f0e577bc0c312fd6b4e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84590398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:971f716e6c1521bc5751c7b351dc76c495f6f1c8731edc3a1d3ad90825e178ef`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:35 GMT
ADD file:9c8b7c79fbbb19d308d151785d178e19bfa7b83257f38d03fa7f30cd41d58530 in / 
# Thu, 07 Sep 2023 00:21:35 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 03:13:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 07 Sep 2023 03:13:06 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 07 Sep 2023 03:13:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 03:13:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 07 Sep 2023 03:13:18 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 07 Sep 2023 03:13:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 03:13:46 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Thu, 07 Sep 2023 03:13:47 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 07 Sep 2023 03:14:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 07 Sep 2023 03:14:05 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 07 Sep 2023 03:14:05 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 07 Sep 2023 03:14:05 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Thu, 07 Sep 2023 03:14:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 07 Sep 2023 03:14:06 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 03:14:06 GMT
VOLUME [/opt/couchdb/data]
# Thu, 07 Sep 2023 03:14:06 GMT
EXPOSE 4369 5984 9100
# Thu, 07 Sep 2023 03:14:06 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:91f01557fe0da558070d4f24631c94e91a80877a24621b52b8b13009b62d8d96`  
		Last Modified: Thu, 07 Sep 2023 00:26:44 GMT  
		Size: 27.2 MB (27187385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc1092381bc12e92f881459a06f8fcde5d883b0563fcf7b65e5e511ce3ffc67`  
		Last Modified: Thu, 07 Sep 2023 03:14:59 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d052afed59bd5876190b7d48e486489a8ba3905254ad4a3e826ef374cefc7df2`  
		Last Modified: Thu, 07 Sep 2023 03:14:58 GMT  
		Size: 6.7 MB (6704555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac30d8a043cb827441c89e5b8830f41291e66d2623cbcb0224b82bcbc865f97`  
		Last Modified: Thu, 07 Sep 2023 03:14:58 GMT  
		Size: 1.3 MB (1259873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced242d5e213b169f1b56b4a6d2ab6910a7091ab511204f6f01ee54edcb81018`  
		Last Modified: Thu, 07 Sep 2023 03:14:57 GMT  
		Size: 294.5 KB (294532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00913b017a468f43fcad144f4e4135d62c9781023142d56629c5d0198fc888de`  
		Last Modified: Thu, 07 Sep 2023 03:15:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb40c3e61db6aa33d343bc8bfaae92f3a3e2f782c7aaacbe303e289f2bf4a0fb`  
		Last Modified: Thu, 07 Sep 2023 03:15:15 GMT  
		Size: 49.1 MB (49137036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e538a885a1a107e2bcb13c5b6a2b582fb7a5198f883e321b4ab0572113c8a568`  
		Last Modified: Thu, 07 Sep 2023 03:15:09 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a11a82bafe89c03ffb91106452e02ab48993695627a04f0bd411f31c5f9d7077`  
		Last Modified: Thu, 07 Sep 2023 03:15:09 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e7ccd73b96f921a094707744b4494c21bede298460a27bcc0e4bc8217a10ce`  
		Last Modified: Thu, 07 Sep 2023 03:15:09 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55017fac998c43da4a403b7ef300f59ea39af4d257e00ded20cfdb88b5a3d05c`  
		Last Modified: Thu, 07 Sep 2023 03:15:09 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:7401f2f09ce6743c95f71659c5f8a9d38d2016f3753917e56f6ac6ce6e09669e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73041292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5940c12b2617e827fec2c1e99e8b9df6be85ab0592d2b6afbcb0b34e8f009a22`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 07 Sep 2023 00:40:08 GMT
ADD file:3521159cdea23e107a3e194ebc9b8f9a6a37ea8188236a267b6ec26e87cf498a in / 
# Thu, 07 Sep 2023 00:40:08 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 06:28:52 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 07 Sep 2023 06:28:52 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 07 Sep 2023 06:28:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 06:29:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 07 Sep 2023 06:29:02 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 07 Sep 2023 06:29:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 06:29:25 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Thu, 07 Sep 2023 06:29:25 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 07 Sep 2023 06:29:38 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 07 Sep 2023 06:29:38 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 07 Sep 2023 06:29:38 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 07 Sep 2023 06:29:38 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Thu, 07 Sep 2023 06:29:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 07 Sep 2023 06:29:39 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 06:29:39 GMT
VOLUME [/opt/couchdb/data]
# Thu, 07 Sep 2023 06:29:39 GMT
EXPOSE 4369 5984 9100
# Thu, 07 Sep 2023 06:29:39 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:d7cc66d62b738dea27e341b7322194f45ab1be2e548fe11d8ad953d9d56caaa8`  
		Last Modified: Thu, 07 Sep 2023 00:44:18 GMT  
		Size: 26.0 MB (25967748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db1a3460de8b082d065480bb42e43b82d38d572475712678f2a0e8cb08ecd68`  
		Last Modified: Thu, 07 Sep 2023 06:30:12 GMT  
		Size: 3.4 KB (3434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed35e23a70461e12fcd438827cb8519278d44276ec964b33c88da192dd0940f`  
		Last Modified: Thu, 07 Sep 2023 06:30:11 GMT  
		Size: 6.6 MB (6577629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c53305c4359589237cd7fc085236bc91c664ee1d590cf5c2d7591e8c45c8b8`  
		Last Modified: Thu, 07 Sep 2023 06:30:11 GMT  
		Size: 1.2 MB (1164824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a69248e9df6adcbf06d6ea44fa051926d09f7c852902a71af69930474b01fa`  
		Last Modified: Thu, 07 Sep 2023 06:30:10 GMT  
		Size: 294.4 KB (294415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6409b1c3bfd333a969570a243665ab5a6131b2f3c57bb8eb9165a583a5918085`  
		Last Modified: Thu, 07 Sep 2023 06:30:22 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6137f1ee41d7358868cb9422f225bf92ed95054d88f2c68c4762d632485d58`  
		Last Modified: Thu, 07 Sep 2023 06:30:24 GMT  
		Size: 39.0 MB (39029639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4fed4668ad08fdf1e88385961dc1ab7bf0578e76a7d8282594d3d1a763f87a2`  
		Last Modified: Thu, 07 Sep 2023 06:30:21 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3dd2964f4c6ac733c29477956974849edf04a9161a4c4204c7995470cb2a476`  
		Last Modified: Thu, 07 Sep 2023 06:30:21 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6cbc45427d41229f33c582c7928bb653f9896ffb2206793126fb2fd4d5e70f`  
		Last Modified: Thu, 07 Sep 2023 06:30:21 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c698dafdd90ba0e7e7deec58ecdcea5800d543470110d3b184502570d954ce4f`  
		Last Modified: Thu, 07 Sep 2023 06:30:21 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:35ac8511e5a6846aa8866a0c8d4c1850e324d3050e3e90fd6429797b93ffcc62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:84f72d8c5f4cf534af9a95af8c4a733abdecf8aee32b9f0e577bc0c312fd6b4e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84590398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:971f716e6c1521bc5751c7b351dc76c495f6f1c8731edc3a1d3ad90825e178ef`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:35 GMT
ADD file:9c8b7c79fbbb19d308d151785d178e19bfa7b83257f38d03fa7f30cd41d58530 in / 
# Thu, 07 Sep 2023 00:21:35 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 03:13:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 07 Sep 2023 03:13:06 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 07 Sep 2023 03:13:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 03:13:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 07 Sep 2023 03:13:18 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 07 Sep 2023 03:13:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 03:13:46 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Thu, 07 Sep 2023 03:13:47 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 07 Sep 2023 03:14:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 07 Sep 2023 03:14:05 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 07 Sep 2023 03:14:05 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 07 Sep 2023 03:14:05 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Thu, 07 Sep 2023 03:14:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 07 Sep 2023 03:14:06 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 03:14:06 GMT
VOLUME [/opt/couchdb/data]
# Thu, 07 Sep 2023 03:14:06 GMT
EXPOSE 4369 5984 9100
# Thu, 07 Sep 2023 03:14:06 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:91f01557fe0da558070d4f24631c94e91a80877a24621b52b8b13009b62d8d96`  
		Last Modified: Thu, 07 Sep 2023 00:26:44 GMT  
		Size: 27.2 MB (27187385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc1092381bc12e92f881459a06f8fcde5d883b0563fcf7b65e5e511ce3ffc67`  
		Last Modified: Thu, 07 Sep 2023 03:14:59 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d052afed59bd5876190b7d48e486489a8ba3905254ad4a3e826ef374cefc7df2`  
		Last Modified: Thu, 07 Sep 2023 03:14:58 GMT  
		Size: 6.7 MB (6704555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac30d8a043cb827441c89e5b8830f41291e66d2623cbcb0224b82bcbc865f97`  
		Last Modified: Thu, 07 Sep 2023 03:14:58 GMT  
		Size: 1.3 MB (1259873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced242d5e213b169f1b56b4a6d2ab6910a7091ab511204f6f01ee54edcb81018`  
		Last Modified: Thu, 07 Sep 2023 03:14:57 GMT  
		Size: 294.5 KB (294532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00913b017a468f43fcad144f4e4135d62c9781023142d56629c5d0198fc888de`  
		Last Modified: Thu, 07 Sep 2023 03:15:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb40c3e61db6aa33d343bc8bfaae92f3a3e2f782c7aaacbe303e289f2bf4a0fb`  
		Last Modified: Thu, 07 Sep 2023 03:15:15 GMT  
		Size: 49.1 MB (49137036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e538a885a1a107e2bcb13c5b6a2b582fb7a5198f883e321b4ab0572113c8a568`  
		Last Modified: Thu, 07 Sep 2023 03:15:09 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a11a82bafe89c03ffb91106452e02ab48993695627a04f0bd411f31c5f9d7077`  
		Last Modified: Thu, 07 Sep 2023 03:15:09 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e7ccd73b96f921a094707744b4494c21bede298460a27bcc0e4bc8217a10ce`  
		Last Modified: Thu, 07 Sep 2023 03:15:09 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55017fac998c43da4a403b7ef300f59ea39af4d257e00ded20cfdb88b5a3d05c`  
		Last Modified: Thu, 07 Sep 2023 03:15:09 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:7401f2f09ce6743c95f71659c5f8a9d38d2016f3753917e56f6ac6ce6e09669e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73041292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5940c12b2617e827fec2c1e99e8b9df6be85ab0592d2b6afbcb0b34e8f009a22`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 07 Sep 2023 00:40:08 GMT
ADD file:3521159cdea23e107a3e194ebc9b8f9a6a37ea8188236a267b6ec26e87cf498a in / 
# Thu, 07 Sep 2023 00:40:08 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 06:28:52 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 07 Sep 2023 06:28:52 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 07 Sep 2023 06:28:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 06:29:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 07 Sep 2023 06:29:02 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 07 Sep 2023 06:29:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 06:29:25 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Thu, 07 Sep 2023 06:29:25 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 07 Sep 2023 06:29:38 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 07 Sep 2023 06:29:38 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 07 Sep 2023 06:29:38 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 07 Sep 2023 06:29:38 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Thu, 07 Sep 2023 06:29:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 07 Sep 2023 06:29:39 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 06:29:39 GMT
VOLUME [/opt/couchdb/data]
# Thu, 07 Sep 2023 06:29:39 GMT
EXPOSE 4369 5984 9100
# Thu, 07 Sep 2023 06:29:39 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:d7cc66d62b738dea27e341b7322194f45ab1be2e548fe11d8ad953d9d56caaa8`  
		Last Modified: Thu, 07 Sep 2023 00:44:18 GMT  
		Size: 26.0 MB (25967748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db1a3460de8b082d065480bb42e43b82d38d572475712678f2a0e8cb08ecd68`  
		Last Modified: Thu, 07 Sep 2023 06:30:12 GMT  
		Size: 3.4 KB (3434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed35e23a70461e12fcd438827cb8519278d44276ec964b33c88da192dd0940f`  
		Last Modified: Thu, 07 Sep 2023 06:30:11 GMT  
		Size: 6.6 MB (6577629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c53305c4359589237cd7fc085236bc91c664ee1d590cf5c2d7591e8c45c8b8`  
		Last Modified: Thu, 07 Sep 2023 06:30:11 GMT  
		Size: 1.2 MB (1164824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a69248e9df6adcbf06d6ea44fa051926d09f7c852902a71af69930474b01fa`  
		Last Modified: Thu, 07 Sep 2023 06:30:10 GMT  
		Size: 294.4 KB (294415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6409b1c3bfd333a969570a243665ab5a6131b2f3c57bb8eb9165a583a5918085`  
		Last Modified: Thu, 07 Sep 2023 06:30:22 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6137f1ee41d7358868cb9422f225bf92ed95054d88f2c68c4762d632485d58`  
		Last Modified: Thu, 07 Sep 2023 06:30:24 GMT  
		Size: 39.0 MB (39029639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4fed4668ad08fdf1e88385961dc1ab7bf0578e76a7d8282594d3d1a763f87a2`  
		Last Modified: Thu, 07 Sep 2023 06:30:21 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3dd2964f4c6ac733c29477956974849edf04a9161a4c4204c7995470cb2a476`  
		Last Modified: Thu, 07 Sep 2023 06:30:21 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6cbc45427d41229f33c582c7928bb653f9896ffb2206793126fb2fd4d5e70f`  
		Last Modified: Thu, 07 Sep 2023 06:30:21 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c698dafdd90ba0e7e7deec58ecdcea5800d543470110d3b184502570d954ce4f`  
		Last Modified: Thu, 07 Sep 2023 06:30:21 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:35ac8511e5a6846aa8866a0c8d4c1850e324d3050e3e90fd6429797b93ffcc62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:84f72d8c5f4cf534af9a95af8c4a733abdecf8aee32b9f0e577bc0c312fd6b4e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84590398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:971f716e6c1521bc5751c7b351dc76c495f6f1c8731edc3a1d3ad90825e178ef`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:35 GMT
ADD file:9c8b7c79fbbb19d308d151785d178e19bfa7b83257f38d03fa7f30cd41d58530 in / 
# Thu, 07 Sep 2023 00:21:35 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 03:13:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 07 Sep 2023 03:13:06 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 07 Sep 2023 03:13:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 03:13:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 07 Sep 2023 03:13:18 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 07 Sep 2023 03:13:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 03:13:46 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Thu, 07 Sep 2023 03:13:47 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 07 Sep 2023 03:14:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 07 Sep 2023 03:14:05 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 07 Sep 2023 03:14:05 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 07 Sep 2023 03:14:05 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Thu, 07 Sep 2023 03:14:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 07 Sep 2023 03:14:06 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 03:14:06 GMT
VOLUME [/opt/couchdb/data]
# Thu, 07 Sep 2023 03:14:06 GMT
EXPOSE 4369 5984 9100
# Thu, 07 Sep 2023 03:14:06 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:91f01557fe0da558070d4f24631c94e91a80877a24621b52b8b13009b62d8d96`  
		Last Modified: Thu, 07 Sep 2023 00:26:44 GMT  
		Size: 27.2 MB (27187385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc1092381bc12e92f881459a06f8fcde5d883b0563fcf7b65e5e511ce3ffc67`  
		Last Modified: Thu, 07 Sep 2023 03:14:59 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d052afed59bd5876190b7d48e486489a8ba3905254ad4a3e826ef374cefc7df2`  
		Last Modified: Thu, 07 Sep 2023 03:14:58 GMT  
		Size: 6.7 MB (6704555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac30d8a043cb827441c89e5b8830f41291e66d2623cbcb0224b82bcbc865f97`  
		Last Modified: Thu, 07 Sep 2023 03:14:58 GMT  
		Size: 1.3 MB (1259873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced242d5e213b169f1b56b4a6d2ab6910a7091ab511204f6f01ee54edcb81018`  
		Last Modified: Thu, 07 Sep 2023 03:14:57 GMT  
		Size: 294.5 KB (294532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00913b017a468f43fcad144f4e4135d62c9781023142d56629c5d0198fc888de`  
		Last Modified: Thu, 07 Sep 2023 03:15:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb40c3e61db6aa33d343bc8bfaae92f3a3e2f782c7aaacbe303e289f2bf4a0fb`  
		Last Modified: Thu, 07 Sep 2023 03:15:15 GMT  
		Size: 49.1 MB (49137036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e538a885a1a107e2bcb13c5b6a2b582fb7a5198f883e321b4ab0572113c8a568`  
		Last Modified: Thu, 07 Sep 2023 03:15:09 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a11a82bafe89c03ffb91106452e02ab48993695627a04f0bd411f31c5f9d7077`  
		Last Modified: Thu, 07 Sep 2023 03:15:09 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e7ccd73b96f921a094707744b4494c21bede298460a27bcc0e4bc8217a10ce`  
		Last Modified: Thu, 07 Sep 2023 03:15:09 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55017fac998c43da4a403b7ef300f59ea39af4d257e00ded20cfdb88b5a3d05c`  
		Last Modified: Thu, 07 Sep 2023 03:15:09 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:7401f2f09ce6743c95f71659c5f8a9d38d2016f3753917e56f6ac6ce6e09669e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73041292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5940c12b2617e827fec2c1e99e8b9df6be85ab0592d2b6afbcb0b34e8f009a22`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 07 Sep 2023 00:40:08 GMT
ADD file:3521159cdea23e107a3e194ebc9b8f9a6a37ea8188236a267b6ec26e87cf498a in / 
# Thu, 07 Sep 2023 00:40:08 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 06:28:52 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 07 Sep 2023 06:28:52 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 07 Sep 2023 06:28:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 06:29:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 07 Sep 2023 06:29:02 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 07 Sep 2023 06:29:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 06:29:25 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Thu, 07 Sep 2023 06:29:25 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 07 Sep 2023 06:29:38 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 07 Sep 2023 06:29:38 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Thu, 07 Sep 2023 06:29:38 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 07 Sep 2023 06:29:38 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Thu, 07 Sep 2023 06:29:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 07 Sep 2023 06:29:39 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 06:29:39 GMT
VOLUME [/opt/couchdb/data]
# Thu, 07 Sep 2023 06:29:39 GMT
EXPOSE 4369 5984 9100
# Thu, 07 Sep 2023 06:29:39 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:d7cc66d62b738dea27e341b7322194f45ab1be2e548fe11d8ad953d9d56caaa8`  
		Last Modified: Thu, 07 Sep 2023 00:44:18 GMT  
		Size: 26.0 MB (25967748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db1a3460de8b082d065480bb42e43b82d38d572475712678f2a0e8cb08ecd68`  
		Last Modified: Thu, 07 Sep 2023 06:30:12 GMT  
		Size: 3.4 KB (3434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed35e23a70461e12fcd438827cb8519278d44276ec964b33c88da192dd0940f`  
		Last Modified: Thu, 07 Sep 2023 06:30:11 GMT  
		Size: 6.6 MB (6577629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c53305c4359589237cd7fc085236bc91c664ee1d590cf5c2d7591e8c45c8b8`  
		Last Modified: Thu, 07 Sep 2023 06:30:11 GMT  
		Size: 1.2 MB (1164824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a69248e9df6adcbf06d6ea44fa051926d09f7c852902a71af69930474b01fa`  
		Last Modified: Thu, 07 Sep 2023 06:30:10 GMT  
		Size: 294.4 KB (294415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6409b1c3bfd333a969570a243665ab5a6131b2f3c57bb8eb9165a583a5918085`  
		Last Modified: Thu, 07 Sep 2023 06:30:22 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6137f1ee41d7358868cb9422f225bf92ed95054d88f2c68c4762d632485d58`  
		Last Modified: Thu, 07 Sep 2023 06:30:24 GMT  
		Size: 39.0 MB (39029639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4fed4668ad08fdf1e88385961dc1ab7bf0578e76a7d8282594d3d1a763f87a2`  
		Last Modified: Thu, 07 Sep 2023 06:30:21 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3dd2964f4c6ac733c29477956974849edf04a9161a4c4204c7995470cb2a476`  
		Last Modified: Thu, 07 Sep 2023 06:30:21 GMT  
		Size: 767.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6cbc45427d41229f33c582c7928bb653f9896ffb2206793126fb2fd4d5e70f`  
		Last Modified: Thu, 07 Sep 2023 06:30:21 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c698dafdd90ba0e7e7deec58ecdcea5800d543470110d3b184502570d954ce4f`  
		Last Modified: Thu, 07 Sep 2023 06:30:21 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3`

```console
$ docker pull couchdb@sha256:e8953219cd8060c67f54d22c33dea2ce4fc28ef73dc7ee185f5b7b169fa68d81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:02832d7f19f13a29f2204c7df8d8d291f08458fc4629d391385804e28bb180b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90240618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c17aff6559a55c79fb79af0c34cd1eea8b73c163feaf7cf8bb6c06f45cdfb4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:13 GMT
ADD file:cb5fcc80c057b356a31492a20c6e3a75b70ed70a663506c8e97ad730ae32a02d in / 
# Thu, 07 Sep 2023 00:21:13 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 03:12:14 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 07 Sep 2023 03:12:14 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 07 Sep 2023 03:12:21 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 03:12:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Thu, 07 Sep 2023 03:12:24 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 07 Sep 2023 03:12:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 03:12:30 GMT
ENV COUCHDB_VERSION=3.3.2
# Thu, 07 Sep 2023 03:12:30 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 07 Sep 2023 03:12:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 07 Sep 2023 03:12:44 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 07 Sep 2023 03:12:44 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Thu, 07 Sep 2023 03:12:44 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Thu, 07 Sep 2023 03:12:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 07 Sep 2023 03:12:44 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 03:12:44 GMT
VOLUME [/opt/couchdb/data]
# Thu, 07 Sep 2023 03:12:45 GMT
EXPOSE 4369 5984 9100
# Thu, 07 Sep 2023 03:12:45 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7d97e254a0461b0a30b3f443f1daa0d620a3cc6ff4e2714cc1cfd96ace5b7a7e`  
		Last Modified: Thu, 07 Sep 2023 00:26:03 GMT  
		Size: 31.4 MB (31417503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b10030446fdd0d136101a551c87b3e56c9a0f0e844b023d3e383c7fe3993b0`  
		Last Modified: Thu, 07 Sep 2023 03:14:26 GMT  
		Size: 3.4 KB (3406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd552b907af3faa1ebc8991aad6352e1056fc5af04762561d1cb7a62aad656f`  
		Last Modified: Thu, 07 Sep 2023 03:14:25 GMT  
		Size: 5.2 MB (5224504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e811bda8d2c68d90b0d4e405545695fd9524161110f1f6fec20eb6c4ee916dd1`  
		Last Modified: Thu, 07 Sep 2023 03:14:24 GMT  
		Size: 610.3 KB (610280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879da14f5933aee5916360f94692440f0d23977de3c242a7da7606295f6ae24e`  
		Last Modified: Thu, 07 Sep 2023 03:14:24 GMT  
		Size: 294.4 KB (294434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8360159bbbccf06b8d3871f1c45b590a27af89a1311ed1ac933104ec984983cb`  
		Last Modified: Thu, 07 Sep 2023 03:14:24 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd9bf0116d5301b0177a08522799ad0cbb296d0f751e3a772de170f4f58d027`  
		Last Modified: Thu, 07 Sep 2023 03:14:27 GMT  
		Size: 52.7 MB (52686485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f80c6f991c0d5cca5f5d92d718f6a9b19bc3b33dcdc901e64938f44ea13bcac`  
		Last Modified: Thu, 07 Sep 2023 03:14:22 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:575e513b07df4f16231083a48874564817ce2a73a148c2413bd4cf70d43f7bb9`  
		Last Modified: Thu, 07 Sep 2023 03:14:22 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf3ab5d6201e72b14659296edd3d9097facf30d368f435aedc1a317db0f94f1`  
		Last Modified: Thu, 07 Sep 2023 03:14:22 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021341363b5eb87a0b91fae27aa9246a6b0bf04b76c392e6e2266dd17d993e7d`  
		Last Modified: Thu, 07 Sep 2023 03:14:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:85dc5e7c838060a6fad9ed40f51c411edcdd913166d82fdc8134de2198c9955c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88684894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c368e49fd3cb709a0a99fdf41accaecb295353d6a5f0424d0af0fd3868203c3`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:53 GMT
ADD file:abd1ad48ae3ebec7a6ecc8ce3016c25be2afcbaedfcb904bc89b1ce59400aef0 in / 
# Thu, 07 Sep 2023 00:39:54 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 06:28:07 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 07 Sep 2023 06:28:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 07 Sep 2023 06:28:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 06:28:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Thu, 07 Sep 2023 06:28:17 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 07 Sep 2023 06:28:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 06:28:22 GMT
ENV COUCHDB_VERSION=3.3.2
# Thu, 07 Sep 2023 06:28:22 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 07 Sep 2023 06:28:34 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 07 Sep 2023 06:28:34 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 07 Sep 2023 06:28:35 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Thu, 07 Sep 2023 06:28:35 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Thu, 07 Sep 2023 06:28:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 07 Sep 2023 06:28:35 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 06:28:35 GMT
VOLUME [/opt/couchdb/data]
# Thu, 07 Sep 2023 06:28:35 GMT
EXPOSE 4369 5984 9100
# Thu, 07 Sep 2023 06:28:35 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f96ab15157043879c2ff23e0556e798eba6a6ff3d7fd5d1384de223bb9f66f1d`  
		Last Modified: Thu, 07 Sep 2023 00:43:41 GMT  
		Size: 30.1 MB (30062903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c5c525e9a401f87cbeb96f0fbeeac0a91eaccdcd8db647be875a18d0ecc9e5`  
		Last Modified: Thu, 07 Sep 2023 06:29:53 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1140236b7ef472420d39b000db183b4f5cd0c2b6f67297a94aaedef621bc93d4`  
		Last Modified: Thu, 07 Sep 2023 06:29:52 GMT  
		Size: 5.2 MB (5209505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b70041a20448d6e2ac7c5ca6d48c56ece09df5c2a0d368b03a1d76fb0f6ee4`  
		Last Modified: Thu, 07 Sep 2023 06:29:52 GMT  
		Size: 566.3 KB (566272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7bf33e25a4a45b5ad0d3341279d7b5055f176896ef97bca7676740c93f74e48`  
		Last Modified: Thu, 07 Sep 2023 06:29:52 GMT  
		Size: 294.3 KB (294303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdba8baef2d8ec8e8c63b46f53515805abed670b729452b79e83edb858e09257`  
		Last Modified: Thu, 07 Sep 2023 06:29:51 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9988a1ff60ee8c9b5557dd18b7c66d0afbe26845feb2cc1496836087b5a13208`  
		Last Modified: Thu, 07 Sep 2023 06:29:54 GMT  
		Size: 52.5 MB (52544467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b669cbe915c91df4045d11cfb7d2cb76339d372bd061cfbef8e8ea6fc54ea24`  
		Last Modified: Thu, 07 Sep 2023 06:29:50 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3b30e1fd8d0a982e29ee8ce8c5134088a29deeb62b31c6a42eddac672e0daf`  
		Last Modified: Thu, 07 Sep 2023 06:29:50 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2bf8aab77cdd6688ab927136a0584d5aaa18894964cb40a63678b454e2059f6`  
		Last Modified: Thu, 07 Sep 2023 06:29:49 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb64e9ab99bf15e9ef95b9a0875b45fc34e2425cd3f243032940137ebff8764`  
		Last Modified: Thu, 07 Sep 2023 06:29:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:e4afbddd20d5602c062d5ca41cdb6a1d7a78de696d3964c1cc389141082bda45
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95962425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6c339fc7925afa097c86945fc7b6f20191a882f4ec40849b783ded191c02786`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 07 Sep 2023 00:18:05 GMT
ADD file:bf50998bef8a71b4723f6c17cc5c3e929d9c3b7a71b56060fea91ea0cd3502c4 in / 
# Thu, 07 Sep 2023 00:18:08 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 11:13:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 07 Sep 2023 11:13:10 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 07 Sep 2023 11:13:40 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 11:13:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Thu, 07 Sep 2023 11:13:57 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 07 Sep 2023 11:14:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 11:14:20 GMT
ENV COUCHDB_VERSION=3.3.2
# Thu, 07 Sep 2023 11:14:26 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 07 Sep 2023 11:15:21 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 07 Sep 2023 11:15:24 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 07 Sep 2023 11:15:24 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Thu, 07 Sep 2023 11:15:24 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Thu, 07 Sep 2023 11:15:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 07 Sep 2023 11:15:27 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 11:15:28 GMT
VOLUME [/opt/couchdb/data]
# Thu, 07 Sep 2023 11:15:28 GMT
EXPOSE 4369 5984 9100
# Thu, 07 Sep 2023 11:15:29 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:2365f3cb8bc5e18258159454852d941d92577738f79c1b5594afaec8481b47f3`  
		Last Modified: Thu, 07 Sep 2023 00:24:24 GMT  
		Size: 35.3 MB (35291070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9197661e71fa84ad86506d3d9ac8079e03a137bec2492f459dc5656517510aa`  
		Last Modified: Thu, 07 Sep 2023 11:16:22 GMT  
		Size: 3.4 KB (3408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9690fd9111712c1dade749e94a2e7367551269fdcffb6c26e10ecb52faa0727`  
		Last Modified: Thu, 07 Sep 2023 11:16:22 GMT  
		Size: 6.0 MB (6044149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d822eee3564d1dd298ee8b44c6eb02d708983fa42676fe8bf7cd42e90eb40a3e`  
		Last Modified: Thu, 07 Sep 2023 11:16:21 GMT  
		Size: 662.2 KB (662190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6578c7ea8724a9ca6f541b5abf3c2d2b0f9ea4b642f52c7bbb10e22dc9b9b3`  
		Last Modified: Thu, 07 Sep 2023 11:16:20 GMT  
		Size: 294.4 KB (294428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c794339b279fee84db7b50f5e8af3d2aaf5f4bffd6af7ac283f4a2633db832`  
		Last Modified: Thu, 07 Sep 2023 11:16:20 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df718b6717ac542cea1677798afd4fdca012056d7411d33e32c7ce7a08219de`  
		Last Modified: Thu, 07 Sep 2023 11:16:27 GMT  
		Size: 53.7 MB (53663170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4046af08908fbf960dd19fb398cbd2d25103dc62f9f6ff8decc9accf5c5d524`  
		Last Modified: Thu, 07 Sep 2023 11:16:18 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87160bd19bf8afffdf7d96264be30b0184cf6d61091cc4affaaf9eb33b6f024`  
		Last Modified: Thu, 07 Sep 2023 11:16:18 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c085c9cd3d2feb5d17923b0dd75e1b6cbae59ac438eb18fc8bc971daa3173c53`  
		Last Modified: Thu, 07 Sep 2023 11:16:18 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff09eb10bd8f4ec1918aa9fbd366247acaf103e29ca9c9eddacc7c610e6136a5`  
		Last Modified: Thu, 07 Sep 2023 11:16:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; s390x

```console
$ docker pull couchdb@sha256:29e829b586b1cb6e650b0e13797721b362071a74370a5f6680669c847090f45a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86992619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192ddd69ff7e41d2bdf0975625c068953c9226f56fe985a51b032813e5bb8c66`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 07 Sep 2023 00:44:33 GMT
ADD file:fb2f216acd6d0ecaf48e8d5dd7e3cdb5d1f51d414f2011ed318cb494f96d89ca in / 
# Thu, 07 Sep 2023 00:44:37 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 01:28:56 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 07 Sep 2023 01:28:58 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 07 Sep 2023 01:29:11 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 01:29:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Thu, 07 Sep 2023 01:29:17 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 07 Sep 2023 01:29:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 01:29:27 GMT
ENV COUCHDB_VERSION=3.3.2
# Thu, 07 Sep 2023 01:29:28 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 07 Sep 2023 01:29:56 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 07 Sep 2023 01:30:05 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 07 Sep 2023 01:30:05 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Thu, 07 Sep 2023 01:30:05 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Thu, 07 Sep 2023 01:30:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 07 Sep 2023 01:30:07 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 01:30:07 GMT
VOLUME [/opt/couchdb/data]
# Thu, 07 Sep 2023 01:30:08 GMT
EXPOSE 4369 5984 9100
# Thu, 07 Sep 2023 01:30:09 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c9501ad9402d64e6c612fa1bb94f16df51188e681dc1f28c603a6109f06f22d7`  
		Last Modified: Thu, 07 Sep 2023 00:50:10 GMT  
		Size: 29.7 MB (29652801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996ad4371fbc51ce08543507129d65ab8b90dd855e656f8eabd70335c57bb0a1`  
		Last Modified: Thu, 07 Sep 2023 01:30:26 GMT  
		Size: 3.4 KB (3435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e0fe5808ef043ae040668477d7e9dfe710765ea40e3d011b82fa33031b7ea4`  
		Last Modified: Thu, 07 Sep 2023 01:30:25 GMT  
		Size: 5.1 MB (5110534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f126aebc8a50e39748585e27d5fd5a9836b6a93c873802d3d3403b156cac952`  
		Last Modified: Thu, 07 Sep 2023 01:30:25 GMT  
		Size: 573.0 KB (573029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f00d25b2e1271b6380742fbbeca5c10b9b084a78cfba7f031f12a3d00a87df5`  
		Last Modified: Thu, 07 Sep 2023 01:30:24 GMT  
		Size: 294.5 KB (294462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577394d2327382521d14f38714c2247fd0db46e1ab49b86cb2350c309835db81`  
		Last Modified: Thu, 07 Sep 2023 01:30:24 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4258fc35f99c32658815e5ea98c85edc9f278bcba6613030c57395fc75cae139`  
		Last Modified: Thu, 07 Sep 2023 01:30:28 GMT  
		Size: 51.4 MB (51354348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0bdcf38e015804f9400dd02e2614c14ea270ce30cfc9602fc0bf39c87dd1fb`  
		Last Modified: Thu, 07 Sep 2023 01:30:23 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d67bc37b8d392d13a0a6a7312678435efade4fd7449ec2ed52945c52abe3b85d`  
		Last Modified: Thu, 07 Sep 2023 01:30:23 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3410bb24e7a70dfce7810cf4736b3f0e0a420444d7825a7d1a9a1309c56e7e`  
		Last Modified: Thu, 07 Sep 2023 01:30:23 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e526b2a03229b6f0cd56ffc8d6c5600b8eec7f407d56686697c3684634adbc52`  
		Last Modified: Thu, 07 Sep 2023 01:30:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:df81b96940d190f029f5301ad9f2569756be7c44e5a4adacc6587bb8497cc262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:a9ce91e42358e711a16f2484eccd42ba225c7c107aca6047a04cf40794f133cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80074204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f5b6c45a5104d460ea23b83405bc242019093af6308cc2eb252054da68832f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:35 GMT
ADD file:9c8b7c79fbbb19d308d151785d178e19bfa7b83257f38d03fa7f30cd41d58530 in / 
# Thu, 07 Sep 2023 00:21:35 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 03:13:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 07 Sep 2023 03:13:06 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 07 Sep 2023 03:13:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 03:13:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 07 Sep 2023 03:13:18 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 07 Sep 2023 03:13:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 03:13:24 GMT
ENV COUCHDB_VERSION=3.1.2
# Thu, 07 Sep 2023 03:13:25 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 07 Sep 2023 03:13:39 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 07 Sep 2023 03:13:40 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 07 Sep 2023 03:13:40 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 07 Sep 2023 03:13:40 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Thu, 07 Sep 2023 03:13:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 07 Sep 2023 03:13:41 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 03:13:41 GMT
VOLUME [/opt/couchdb/data]
# Thu, 07 Sep 2023 03:13:41 GMT
EXPOSE 4369 5984 9100
# Thu, 07 Sep 2023 03:13:41 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:91f01557fe0da558070d4f24631c94e91a80877a24621b52b8b13009b62d8d96`  
		Last Modified: Thu, 07 Sep 2023 00:26:44 GMT  
		Size: 27.2 MB (27187385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc1092381bc12e92f881459a06f8fcde5d883b0563fcf7b65e5e511ce3ffc67`  
		Last Modified: Thu, 07 Sep 2023 03:14:59 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d052afed59bd5876190b7d48e486489a8ba3905254ad4a3e826ef374cefc7df2`  
		Last Modified: Thu, 07 Sep 2023 03:14:58 GMT  
		Size: 6.7 MB (6704555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac30d8a043cb827441c89e5b8830f41291e66d2623cbcb0224b82bcbc865f97`  
		Last Modified: Thu, 07 Sep 2023 03:14:58 GMT  
		Size: 1.3 MB (1259873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced242d5e213b169f1b56b4a6d2ab6910a7091ab511204f6f01ee54edcb81018`  
		Last Modified: Thu, 07 Sep 2023 03:14:57 GMT  
		Size: 294.5 KB (294532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc59953cbe30e5b1a7ffebfc5dd4337669e2761805e54f88123ebe3404caf1fe`  
		Last Modified: Thu, 07 Sep 2023 03:14:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b1667bfaf44d69237e60f57ead3a6a619bc5cf15ee1bc3f7db92a70d1c9eee`  
		Last Modified: Thu, 07 Sep 2023 03:15:00 GMT  
		Size: 44.6 MB (44620847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64eac70dd0672b0f900a479458b94375a6f61a9c3afe8889d5753c402ad729be`  
		Last Modified: Thu, 07 Sep 2023 03:14:55 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a74a7cffe10aa333e3beaa55d67579ef3d51722e5dc8b37694b15f5d904dff5`  
		Last Modified: Thu, 07 Sep 2023 03:14:55 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38e78a9aa0e9f3f716208ec1e2254b872ef06c743e040679ae8e3b0ec686a7e`  
		Last Modified: Thu, 07 Sep 2023 03:14:55 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3542fe57a29cbca95bd5b40a53034d48e310e1ad35b59ae6c0969abad58bf2`  
		Last Modified: Thu, 07 Sep 2023 03:14:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:376bf8083e373d42870533af689ffc51f7d7cf1946166b3ba9942434a5576570
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75138247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d3d0d374bb2fe4d01586ca4fa48520f8516770eaa1ad5b71e9a78073a4aa7cc`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 07 Sep 2023 00:40:08 GMT
ADD file:3521159cdea23e107a3e194ebc9b8f9a6a37ea8188236a267b6ec26e87cf498a in / 
# Thu, 07 Sep 2023 00:40:08 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 06:28:52 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 07 Sep 2023 06:28:52 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 07 Sep 2023 06:28:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 06:29:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 07 Sep 2023 06:29:02 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 07 Sep 2023 06:29:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 06:29:08 GMT
ENV COUCHDB_VERSION=3.1.2
# Thu, 07 Sep 2023 06:29:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 07 Sep 2023 06:29:20 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 07 Sep 2023 06:29:21 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 07 Sep 2023 06:29:21 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 07 Sep 2023 06:29:21 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Thu, 07 Sep 2023 06:29:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 07 Sep 2023 06:29:21 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 06:29:22 GMT
VOLUME [/opt/couchdb/data]
# Thu, 07 Sep 2023 06:29:22 GMT
EXPOSE 4369 5984 9100
# Thu, 07 Sep 2023 06:29:22 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:d7cc66d62b738dea27e341b7322194f45ab1be2e548fe11d8ad953d9d56caaa8`  
		Last Modified: Thu, 07 Sep 2023 00:44:18 GMT  
		Size: 26.0 MB (25967748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db1a3460de8b082d065480bb42e43b82d38d572475712678f2a0e8cb08ecd68`  
		Last Modified: Thu, 07 Sep 2023 06:30:12 GMT  
		Size: 3.4 KB (3434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed35e23a70461e12fcd438827cb8519278d44276ec964b33c88da192dd0940f`  
		Last Modified: Thu, 07 Sep 2023 06:30:11 GMT  
		Size: 6.6 MB (6577629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c53305c4359589237cd7fc085236bc91c664ee1d590cf5c2d7591e8c45c8b8`  
		Last Modified: Thu, 07 Sep 2023 06:30:11 GMT  
		Size: 1.2 MB (1164824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a69248e9df6adcbf06d6ea44fa051926d09f7c852902a71af69930474b01fa`  
		Last Modified: Thu, 07 Sep 2023 06:30:10 GMT  
		Size: 294.4 KB (294415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f63c870171d7b350190ac2ef361bae4e56227db25db7f8ffe4f9e4e3caaf21`  
		Last Modified: Thu, 07 Sep 2023 06:30:10 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674bbed78ae048167564b59d0c1d96b57a57ee5ab952c5d5546ea62a40d84382`  
		Last Modified: Thu, 07 Sep 2023 06:30:12 GMT  
		Size: 41.1 MB (41126593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704fcb46059d3f143697ba0c57f6fa80482b281bf23763e335108afa21b3ac18`  
		Last Modified: Thu, 07 Sep 2023 06:30:08 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83301d736f2ff8aecbd75b8d05121c8273e5e77760bfa6bab4bb6d01a4ec842d`  
		Last Modified: Thu, 07 Sep 2023 06:30:08 GMT  
		Size: 768.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8887a0af277e2b66f4162ae4e988e97aa88c1f6c85ce2fffae448f8702b0dd5`  
		Last Modified: Thu, 07 Sep 2023 06:30:08 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3154d454cb3b96d9ed8a89645f3f0adca381cdf05c89534d6f2ec613025af3d8`  
		Last Modified: Thu, 07 Sep 2023 06:30:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1.2`

```console
$ docker pull couchdb@sha256:df81b96940d190f029f5301ad9f2569756be7c44e5a4adacc6587bb8497cc262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1.2` - linux; amd64

```console
$ docker pull couchdb@sha256:a9ce91e42358e711a16f2484eccd42ba225c7c107aca6047a04cf40794f133cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80074204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f5b6c45a5104d460ea23b83405bc242019093af6308cc2eb252054da68832f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:35 GMT
ADD file:9c8b7c79fbbb19d308d151785d178e19bfa7b83257f38d03fa7f30cd41d58530 in / 
# Thu, 07 Sep 2023 00:21:35 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 03:13:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 07 Sep 2023 03:13:06 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 07 Sep 2023 03:13:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 03:13:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 07 Sep 2023 03:13:18 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 07 Sep 2023 03:13:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 03:13:24 GMT
ENV COUCHDB_VERSION=3.1.2
# Thu, 07 Sep 2023 03:13:25 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 07 Sep 2023 03:13:39 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 07 Sep 2023 03:13:40 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 07 Sep 2023 03:13:40 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 07 Sep 2023 03:13:40 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Thu, 07 Sep 2023 03:13:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 07 Sep 2023 03:13:41 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 03:13:41 GMT
VOLUME [/opt/couchdb/data]
# Thu, 07 Sep 2023 03:13:41 GMT
EXPOSE 4369 5984 9100
# Thu, 07 Sep 2023 03:13:41 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:91f01557fe0da558070d4f24631c94e91a80877a24621b52b8b13009b62d8d96`  
		Last Modified: Thu, 07 Sep 2023 00:26:44 GMT  
		Size: 27.2 MB (27187385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc1092381bc12e92f881459a06f8fcde5d883b0563fcf7b65e5e511ce3ffc67`  
		Last Modified: Thu, 07 Sep 2023 03:14:59 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d052afed59bd5876190b7d48e486489a8ba3905254ad4a3e826ef374cefc7df2`  
		Last Modified: Thu, 07 Sep 2023 03:14:58 GMT  
		Size: 6.7 MB (6704555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac30d8a043cb827441c89e5b8830f41291e66d2623cbcb0224b82bcbc865f97`  
		Last Modified: Thu, 07 Sep 2023 03:14:58 GMT  
		Size: 1.3 MB (1259873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced242d5e213b169f1b56b4a6d2ab6910a7091ab511204f6f01ee54edcb81018`  
		Last Modified: Thu, 07 Sep 2023 03:14:57 GMT  
		Size: 294.5 KB (294532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc59953cbe30e5b1a7ffebfc5dd4337669e2761805e54f88123ebe3404caf1fe`  
		Last Modified: Thu, 07 Sep 2023 03:14:57 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b1667bfaf44d69237e60f57ead3a6a619bc5cf15ee1bc3f7db92a70d1c9eee`  
		Last Modified: Thu, 07 Sep 2023 03:15:00 GMT  
		Size: 44.6 MB (44620847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64eac70dd0672b0f900a479458b94375a6f61a9c3afe8889d5753c402ad729be`  
		Last Modified: Thu, 07 Sep 2023 03:14:55 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a74a7cffe10aa333e3beaa55d67579ef3d51722e5dc8b37694b15f5d904dff5`  
		Last Modified: Thu, 07 Sep 2023 03:14:55 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38e78a9aa0e9f3f716208ec1e2254b872ef06c743e040679ae8e3b0ec686a7e`  
		Last Modified: Thu, 07 Sep 2023 03:14:55 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3542fe57a29cbca95bd5b40a53034d48e310e1ad35b59ae6c0969abad58bf2`  
		Last Modified: Thu, 07 Sep 2023 03:14:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:376bf8083e373d42870533af689ffc51f7d7cf1946166b3ba9942434a5576570
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75138247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d3d0d374bb2fe4d01586ca4fa48520f8516770eaa1ad5b71e9a78073a4aa7cc`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 07 Sep 2023 00:40:08 GMT
ADD file:3521159cdea23e107a3e194ebc9b8f9a6a37ea8188236a267b6ec26e87cf498a in / 
# Thu, 07 Sep 2023 00:40:08 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 06:28:52 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 07 Sep 2023 06:28:52 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 07 Sep 2023 06:28:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 06:29:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 07 Sep 2023 06:29:02 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 07 Sep 2023 06:29:08 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 06:29:08 GMT
ENV COUCHDB_VERSION=3.1.2
# Thu, 07 Sep 2023 06:29:08 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 07 Sep 2023 06:29:20 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 07 Sep 2023 06:29:21 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 07 Sep 2023 06:29:21 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 07 Sep 2023 06:29:21 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Thu, 07 Sep 2023 06:29:21 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 07 Sep 2023 06:29:21 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 06:29:22 GMT
VOLUME [/opt/couchdb/data]
# Thu, 07 Sep 2023 06:29:22 GMT
EXPOSE 4369 5984 9100
# Thu, 07 Sep 2023 06:29:22 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:d7cc66d62b738dea27e341b7322194f45ab1be2e548fe11d8ad953d9d56caaa8`  
		Last Modified: Thu, 07 Sep 2023 00:44:18 GMT  
		Size: 26.0 MB (25967748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db1a3460de8b082d065480bb42e43b82d38d572475712678f2a0e8cb08ecd68`  
		Last Modified: Thu, 07 Sep 2023 06:30:12 GMT  
		Size: 3.4 KB (3434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed35e23a70461e12fcd438827cb8519278d44276ec964b33c88da192dd0940f`  
		Last Modified: Thu, 07 Sep 2023 06:30:11 GMT  
		Size: 6.6 MB (6577629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c53305c4359589237cd7fc085236bc91c664ee1d590cf5c2d7591e8c45c8b8`  
		Last Modified: Thu, 07 Sep 2023 06:30:11 GMT  
		Size: 1.2 MB (1164824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a69248e9df6adcbf06d6ea44fa051926d09f7c852902a71af69930474b01fa`  
		Last Modified: Thu, 07 Sep 2023 06:30:10 GMT  
		Size: 294.4 KB (294415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f63c870171d7b350190ac2ef361bae4e56227db25db7f8ffe4f9e4e3caaf21`  
		Last Modified: Thu, 07 Sep 2023 06:30:10 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674bbed78ae048167564b59d0c1d96b57a57ee5ab952c5d5546ea62a40d84382`  
		Last Modified: Thu, 07 Sep 2023 06:30:12 GMT  
		Size: 41.1 MB (41126593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704fcb46059d3f143697ba0c57f6fa80482b281bf23763e335108afa21b3ac18`  
		Last Modified: Thu, 07 Sep 2023 06:30:08 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83301d736f2ff8aecbd75b8d05121c8273e5e77760bfa6bab4bb6d01a4ec842d`  
		Last Modified: Thu, 07 Sep 2023 06:30:08 GMT  
		Size: 768.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8887a0af277e2b66f4162ae4e988e97aa88c1f6c85ce2fffae448f8702b0dd5`  
		Last Modified: Thu, 07 Sep 2023 06:30:08 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3154d454cb3b96d9ed8a89645f3f0adca381cdf05c89534d6f2ec613025af3d8`  
		Last Modified: Thu, 07 Sep 2023 06:30:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2`

```console
$ docker pull couchdb@sha256:575763f128c290e53a5498b82922d12a92370872d572d74ef00afce8c3705f2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:589a5498a16085f977a3ee19072439169ec1f60ade0193d1a57cae55846fa98e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89740438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d10e31f34c59200dcd13d7c7ea7fc13b7a1f45e4c0b3f1e4687e99e40e8cc39`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:13 GMT
ADD file:cb5fcc80c057b356a31492a20c6e3a75b70ed70a663506c8e97ad730ae32a02d in / 
# Thu, 07 Sep 2023 00:21:13 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 03:12:14 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 07 Sep 2023 03:12:14 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 07 Sep 2023 03:12:21 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 03:12:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Thu, 07 Sep 2023 03:12:24 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 07 Sep 2023 03:12:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 03:12:48 GMT
ENV COUCHDB_VERSION=3.2.3
# Thu, 07 Sep 2023 03:12:48 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 07 Sep 2023 03:13:01 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 07 Sep 2023 03:13:01 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 07 Sep 2023 03:13:02 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Thu, 07 Sep 2023 03:13:02 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Thu, 07 Sep 2023 03:13:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 07 Sep 2023 03:13:02 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 03:13:02 GMT
VOLUME [/opt/couchdb/data]
# Thu, 07 Sep 2023 03:13:02 GMT
EXPOSE 4369 5984 9100
# Thu, 07 Sep 2023 03:13:02 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7d97e254a0461b0a30b3f443f1daa0d620a3cc6ff4e2714cc1cfd96ace5b7a7e`  
		Last Modified: Thu, 07 Sep 2023 00:26:03 GMT  
		Size: 31.4 MB (31417503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b10030446fdd0d136101a551c87b3e56c9a0f0e844b023d3e383c7fe3993b0`  
		Last Modified: Thu, 07 Sep 2023 03:14:26 GMT  
		Size: 3.4 KB (3406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd552b907af3faa1ebc8991aad6352e1056fc5af04762561d1cb7a62aad656f`  
		Last Modified: Thu, 07 Sep 2023 03:14:25 GMT  
		Size: 5.2 MB (5224504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e811bda8d2c68d90b0d4e405545695fd9524161110f1f6fec20eb6c4ee916dd1`  
		Last Modified: Thu, 07 Sep 2023 03:14:24 GMT  
		Size: 610.3 KB (610280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879da14f5933aee5916360f94692440f0d23977de3c242a7da7606295f6ae24e`  
		Last Modified: Thu, 07 Sep 2023 03:14:24 GMT  
		Size: 294.4 KB (294434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74211937f6a7b23abdbfd0eca2a214e4d9632bb9301d74cc262e3e9f97f77e17`  
		Last Modified: Thu, 07 Sep 2023 03:14:42 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c10040687e3e56ed14e507572a4cca4da3b7eb8243e60eab4f9f179d6056f8`  
		Last Modified: Thu, 07 Sep 2023 03:14:46 GMT  
		Size: 52.2 MB (52186306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c730731ce3dd7c2b9c02a79f065a62acae92ec784df4be9435e76d9fefd2a5`  
		Last Modified: Thu, 07 Sep 2023 03:14:40 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3f2eb40fdf854d918b5cee57dc527cac6d93c1b65fa05197d20a61068890ee`  
		Last Modified: Thu, 07 Sep 2023 03:14:40 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c47fe8c4c3c350407d8559ce3788660b338f7f9e9a1e4715732ebad9f0da4b7`  
		Last Modified: Thu, 07 Sep 2023 03:14:40 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5760393e2349dd9567ed2d64d2050b0f9ff6844944d448a2b7cb05082ab8692`  
		Last Modified: Thu, 07 Sep 2023 03:14:41 GMT  
		Size: 121.0 B  
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
$ docker pull couchdb@sha256:d5fe4cf7af1ef2ad65311737ca4cfcfe6a2441f058ce6312b87f80ad6cfb68b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchdb:3.2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:589a5498a16085f977a3ee19072439169ec1f60ade0193d1a57cae55846fa98e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89740438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d10e31f34c59200dcd13d7c7ea7fc13b7a1f45e4c0b3f1e4687e99e40e8cc39`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:13 GMT
ADD file:cb5fcc80c057b356a31492a20c6e3a75b70ed70a663506c8e97ad730ae32a02d in / 
# Thu, 07 Sep 2023 00:21:13 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 03:12:14 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 07 Sep 2023 03:12:14 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 07 Sep 2023 03:12:21 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 03:12:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Thu, 07 Sep 2023 03:12:24 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 07 Sep 2023 03:12:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 03:12:48 GMT
ENV COUCHDB_VERSION=3.2.3
# Thu, 07 Sep 2023 03:12:48 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 07 Sep 2023 03:13:01 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 07 Sep 2023 03:13:01 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 07 Sep 2023 03:13:02 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Thu, 07 Sep 2023 03:13:02 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Thu, 07 Sep 2023 03:13:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 07 Sep 2023 03:13:02 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 03:13:02 GMT
VOLUME [/opt/couchdb/data]
# Thu, 07 Sep 2023 03:13:02 GMT
EXPOSE 4369 5984 9100
# Thu, 07 Sep 2023 03:13:02 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7d97e254a0461b0a30b3f443f1daa0d620a3cc6ff4e2714cc1cfd96ace5b7a7e`  
		Last Modified: Thu, 07 Sep 2023 00:26:03 GMT  
		Size: 31.4 MB (31417503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b10030446fdd0d136101a551c87b3e56c9a0f0e844b023d3e383c7fe3993b0`  
		Last Modified: Thu, 07 Sep 2023 03:14:26 GMT  
		Size: 3.4 KB (3406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd552b907af3faa1ebc8991aad6352e1056fc5af04762561d1cb7a62aad656f`  
		Last Modified: Thu, 07 Sep 2023 03:14:25 GMT  
		Size: 5.2 MB (5224504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e811bda8d2c68d90b0d4e405545695fd9524161110f1f6fec20eb6c4ee916dd1`  
		Last Modified: Thu, 07 Sep 2023 03:14:24 GMT  
		Size: 610.3 KB (610280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879da14f5933aee5916360f94692440f0d23977de3c242a7da7606295f6ae24e`  
		Last Modified: Thu, 07 Sep 2023 03:14:24 GMT  
		Size: 294.4 KB (294434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74211937f6a7b23abdbfd0eca2a214e4d9632bb9301d74cc262e3e9f97f77e17`  
		Last Modified: Thu, 07 Sep 2023 03:14:42 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c10040687e3e56ed14e507572a4cca4da3b7eb8243e60eab4f9f179d6056f8`  
		Last Modified: Thu, 07 Sep 2023 03:14:46 GMT  
		Size: 52.2 MB (52186306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c730731ce3dd7c2b9c02a79f065a62acae92ec784df4be9435e76d9fefd2a5`  
		Last Modified: Thu, 07 Sep 2023 03:14:40 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3f2eb40fdf854d918b5cee57dc527cac6d93c1b65fa05197d20a61068890ee`  
		Last Modified: Thu, 07 Sep 2023 03:14:40 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c47fe8c4c3c350407d8559ce3788660b338f7f9e9a1e4715732ebad9f0da4b7`  
		Last Modified: Thu, 07 Sep 2023 03:14:40 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5760393e2349dd9567ed2d64d2050b0f9ff6844944d448a2b7cb05082ab8692`  
		Last Modified: Thu, 07 Sep 2023 03:14:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.3`

```console
$ docker pull couchdb@sha256:e8953219cd8060c67f54d22c33dea2ce4fc28ef73dc7ee185f5b7b169fa68d81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `couchdb:3.3` - linux; amd64

```console
$ docker pull couchdb@sha256:02832d7f19f13a29f2204c7df8d8d291f08458fc4629d391385804e28bb180b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90240618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c17aff6559a55c79fb79af0c34cd1eea8b73c163feaf7cf8bb6c06f45cdfb4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:13 GMT
ADD file:cb5fcc80c057b356a31492a20c6e3a75b70ed70a663506c8e97ad730ae32a02d in / 
# Thu, 07 Sep 2023 00:21:13 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 03:12:14 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 07 Sep 2023 03:12:14 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 07 Sep 2023 03:12:21 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 03:12:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Thu, 07 Sep 2023 03:12:24 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 07 Sep 2023 03:12:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 03:12:30 GMT
ENV COUCHDB_VERSION=3.3.2
# Thu, 07 Sep 2023 03:12:30 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 07 Sep 2023 03:12:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 07 Sep 2023 03:12:44 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 07 Sep 2023 03:12:44 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Thu, 07 Sep 2023 03:12:44 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Thu, 07 Sep 2023 03:12:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 07 Sep 2023 03:12:44 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 03:12:44 GMT
VOLUME [/opt/couchdb/data]
# Thu, 07 Sep 2023 03:12:45 GMT
EXPOSE 4369 5984 9100
# Thu, 07 Sep 2023 03:12:45 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7d97e254a0461b0a30b3f443f1daa0d620a3cc6ff4e2714cc1cfd96ace5b7a7e`  
		Last Modified: Thu, 07 Sep 2023 00:26:03 GMT  
		Size: 31.4 MB (31417503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b10030446fdd0d136101a551c87b3e56c9a0f0e844b023d3e383c7fe3993b0`  
		Last Modified: Thu, 07 Sep 2023 03:14:26 GMT  
		Size: 3.4 KB (3406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd552b907af3faa1ebc8991aad6352e1056fc5af04762561d1cb7a62aad656f`  
		Last Modified: Thu, 07 Sep 2023 03:14:25 GMT  
		Size: 5.2 MB (5224504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e811bda8d2c68d90b0d4e405545695fd9524161110f1f6fec20eb6c4ee916dd1`  
		Last Modified: Thu, 07 Sep 2023 03:14:24 GMT  
		Size: 610.3 KB (610280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879da14f5933aee5916360f94692440f0d23977de3c242a7da7606295f6ae24e`  
		Last Modified: Thu, 07 Sep 2023 03:14:24 GMT  
		Size: 294.4 KB (294434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8360159bbbccf06b8d3871f1c45b590a27af89a1311ed1ac933104ec984983cb`  
		Last Modified: Thu, 07 Sep 2023 03:14:24 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd9bf0116d5301b0177a08522799ad0cbb296d0f751e3a772de170f4f58d027`  
		Last Modified: Thu, 07 Sep 2023 03:14:27 GMT  
		Size: 52.7 MB (52686485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f80c6f991c0d5cca5f5d92d718f6a9b19bc3b33dcdc901e64938f44ea13bcac`  
		Last Modified: Thu, 07 Sep 2023 03:14:22 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:575e513b07df4f16231083a48874564817ce2a73a148c2413bd4cf70d43f7bb9`  
		Last Modified: Thu, 07 Sep 2023 03:14:22 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf3ab5d6201e72b14659296edd3d9097facf30d368f435aedc1a317db0f94f1`  
		Last Modified: Thu, 07 Sep 2023 03:14:22 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021341363b5eb87a0b91fae27aa9246a6b0bf04b76c392e6e2266dd17d993e7d`  
		Last Modified: Thu, 07 Sep 2023 03:14:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:85dc5e7c838060a6fad9ed40f51c411edcdd913166d82fdc8134de2198c9955c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88684894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c368e49fd3cb709a0a99fdf41accaecb295353d6a5f0424d0af0fd3868203c3`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:53 GMT
ADD file:abd1ad48ae3ebec7a6ecc8ce3016c25be2afcbaedfcb904bc89b1ce59400aef0 in / 
# Thu, 07 Sep 2023 00:39:54 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 06:28:07 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 07 Sep 2023 06:28:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 07 Sep 2023 06:28:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 06:28:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Thu, 07 Sep 2023 06:28:17 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 07 Sep 2023 06:28:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 06:28:22 GMT
ENV COUCHDB_VERSION=3.3.2
# Thu, 07 Sep 2023 06:28:22 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 07 Sep 2023 06:28:34 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 07 Sep 2023 06:28:34 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 07 Sep 2023 06:28:35 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Thu, 07 Sep 2023 06:28:35 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Thu, 07 Sep 2023 06:28:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 07 Sep 2023 06:28:35 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 06:28:35 GMT
VOLUME [/opt/couchdb/data]
# Thu, 07 Sep 2023 06:28:35 GMT
EXPOSE 4369 5984 9100
# Thu, 07 Sep 2023 06:28:35 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f96ab15157043879c2ff23e0556e798eba6a6ff3d7fd5d1384de223bb9f66f1d`  
		Last Modified: Thu, 07 Sep 2023 00:43:41 GMT  
		Size: 30.1 MB (30062903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c5c525e9a401f87cbeb96f0fbeeac0a91eaccdcd8db647be875a18d0ecc9e5`  
		Last Modified: Thu, 07 Sep 2023 06:29:53 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1140236b7ef472420d39b000db183b4f5cd0c2b6f67297a94aaedef621bc93d4`  
		Last Modified: Thu, 07 Sep 2023 06:29:52 GMT  
		Size: 5.2 MB (5209505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b70041a20448d6e2ac7c5ca6d48c56ece09df5c2a0d368b03a1d76fb0f6ee4`  
		Last Modified: Thu, 07 Sep 2023 06:29:52 GMT  
		Size: 566.3 KB (566272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7bf33e25a4a45b5ad0d3341279d7b5055f176896ef97bca7676740c93f74e48`  
		Last Modified: Thu, 07 Sep 2023 06:29:52 GMT  
		Size: 294.3 KB (294303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdba8baef2d8ec8e8c63b46f53515805abed670b729452b79e83edb858e09257`  
		Last Modified: Thu, 07 Sep 2023 06:29:51 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9988a1ff60ee8c9b5557dd18b7c66d0afbe26845feb2cc1496836087b5a13208`  
		Last Modified: Thu, 07 Sep 2023 06:29:54 GMT  
		Size: 52.5 MB (52544467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b669cbe915c91df4045d11cfb7d2cb76339d372bd061cfbef8e8ea6fc54ea24`  
		Last Modified: Thu, 07 Sep 2023 06:29:50 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3b30e1fd8d0a982e29ee8ce8c5134088a29deeb62b31c6a42eddac672e0daf`  
		Last Modified: Thu, 07 Sep 2023 06:29:50 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2bf8aab77cdd6688ab927136a0584d5aaa18894964cb40a63678b454e2059f6`  
		Last Modified: Thu, 07 Sep 2023 06:29:49 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb64e9ab99bf15e9ef95b9a0875b45fc34e2425cd3f243032940137ebff8764`  
		Last Modified: Thu, 07 Sep 2023 06:29:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:e4afbddd20d5602c062d5ca41cdb6a1d7a78de696d3964c1cc389141082bda45
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95962425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6c339fc7925afa097c86945fc7b6f20191a882f4ec40849b783ded191c02786`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 07 Sep 2023 00:18:05 GMT
ADD file:bf50998bef8a71b4723f6c17cc5c3e929d9c3b7a71b56060fea91ea0cd3502c4 in / 
# Thu, 07 Sep 2023 00:18:08 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 11:13:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 07 Sep 2023 11:13:10 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 07 Sep 2023 11:13:40 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 11:13:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Thu, 07 Sep 2023 11:13:57 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 07 Sep 2023 11:14:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 11:14:20 GMT
ENV COUCHDB_VERSION=3.3.2
# Thu, 07 Sep 2023 11:14:26 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 07 Sep 2023 11:15:21 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 07 Sep 2023 11:15:24 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 07 Sep 2023 11:15:24 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Thu, 07 Sep 2023 11:15:24 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Thu, 07 Sep 2023 11:15:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 07 Sep 2023 11:15:27 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 11:15:28 GMT
VOLUME [/opt/couchdb/data]
# Thu, 07 Sep 2023 11:15:28 GMT
EXPOSE 4369 5984 9100
# Thu, 07 Sep 2023 11:15:29 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:2365f3cb8bc5e18258159454852d941d92577738f79c1b5594afaec8481b47f3`  
		Last Modified: Thu, 07 Sep 2023 00:24:24 GMT  
		Size: 35.3 MB (35291070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9197661e71fa84ad86506d3d9ac8079e03a137bec2492f459dc5656517510aa`  
		Last Modified: Thu, 07 Sep 2023 11:16:22 GMT  
		Size: 3.4 KB (3408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9690fd9111712c1dade749e94a2e7367551269fdcffb6c26e10ecb52faa0727`  
		Last Modified: Thu, 07 Sep 2023 11:16:22 GMT  
		Size: 6.0 MB (6044149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d822eee3564d1dd298ee8b44c6eb02d708983fa42676fe8bf7cd42e90eb40a3e`  
		Last Modified: Thu, 07 Sep 2023 11:16:21 GMT  
		Size: 662.2 KB (662190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6578c7ea8724a9ca6f541b5abf3c2d2b0f9ea4b642f52c7bbb10e22dc9b9b3`  
		Last Modified: Thu, 07 Sep 2023 11:16:20 GMT  
		Size: 294.4 KB (294428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c794339b279fee84db7b50f5e8af3d2aaf5f4bffd6af7ac283f4a2633db832`  
		Last Modified: Thu, 07 Sep 2023 11:16:20 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df718b6717ac542cea1677798afd4fdca012056d7411d33e32c7ce7a08219de`  
		Last Modified: Thu, 07 Sep 2023 11:16:27 GMT  
		Size: 53.7 MB (53663170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4046af08908fbf960dd19fb398cbd2d25103dc62f9f6ff8decc9accf5c5d524`  
		Last Modified: Thu, 07 Sep 2023 11:16:18 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87160bd19bf8afffdf7d96264be30b0184cf6d61091cc4affaaf9eb33b6f024`  
		Last Modified: Thu, 07 Sep 2023 11:16:18 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c085c9cd3d2feb5d17923b0dd75e1b6cbae59ac438eb18fc8bc971daa3173c53`  
		Last Modified: Thu, 07 Sep 2023 11:16:18 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff09eb10bd8f4ec1918aa9fbd366247acaf103e29ca9c9eddacc7c610e6136a5`  
		Last Modified: Thu, 07 Sep 2023 11:16:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3` - linux; s390x

```console
$ docker pull couchdb@sha256:29e829b586b1cb6e650b0e13797721b362071a74370a5f6680669c847090f45a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86992619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192ddd69ff7e41d2bdf0975625c068953c9226f56fe985a51b032813e5bb8c66`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 07 Sep 2023 00:44:33 GMT
ADD file:fb2f216acd6d0ecaf48e8d5dd7e3cdb5d1f51d414f2011ed318cb494f96d89ca in / 
# Thu, 07 Sep 2023 00:44:37 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 01:28:56 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 07 Sep 2023 01:28:58 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 07 Sep 2023 01:29:11 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 01:29:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Thu, 07 Sep 2023 01:29:17 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 07 Sep 2023 01:29:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 01:29:27 GMT
ENV COUCHDB_VERSION=3.3.2
# Thu, 07 Sep 2023 01:29:28 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 07 Sep 2023 01:29:56 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 07 Sep 2023 01:30:05 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 07 Sep 2023 01:30:05 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Thu, 07 Sep 2023 01:30:05 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Thu, 07 Sep 2023 01:30:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 07 Sep 2023 01:30:07 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 01:30:07 GMT
VOLUME [/opt/couchdb/data]
# Thu, 07 Sep 2023 01:30:08 GMT
EXPOSE 4369 5984 9100
# Thu, 07 Sep 2023 01:30:09 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c9501ad9402d64e6c612fa1bb94f16df51188e681dc1f28c603a6109f06f22d7`  
		Last Modified: Thu, 07 Sep 2023 00:50:10 GMT  
		Size: 29.7 MB (29652801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996ad4371fbc51ce08543507129d65ab8b90dd855e656f8eabd70335c57bb0a1`  
		Last Modified: Thu, 07 Sep 2023 01:30:26 GMT  
		Size: 3.4 KB (3435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e0fe5808ef043ae040668477d7e9dfe710765ea40e3d011b82fa33031b7ea4`  
		Last Modified: Thu, 07 Sep 2023 01:30:25 GMT  
		Size: 5.1 MB (5110534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f126aebc8a50e39748585e27d5fd5a9836b6a93c873802d3d3403b156cac952`  
		Last Modified: Thu, 07 Sep 2023 01:30:25 GMT  
		Size: 573.0 KB (573029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f00d25b2e1271b6380742fbbeca5c10b9b084a78cfba7f031f12a3d00a87df5`  
		Last Modified: Thu, 07 Sep 2023 01:30:24 GMT  
		Size: 294.5 KB (294462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577394d2327382521d14f38714c2247fd0db46e1ab49b86cb2350c309835db81`  
		Last Modified: Thu, 07 Sep 2023 01:30:24 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4258fc35f99c32658815e5ea98c85edc9f278bcba6613030c57395fc75cae139`  
		Last Modified: Thu, 07 Sep 2023 01:30:28 GMT  
		Size: 51.4 MB (51354348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0bdcf38e015804f9400dd02e2614c14ea270ce30cfc9602fc0bf39c87dd1fb`  
		Last Modified: Thu, 07 Sep 2023 01:30:23 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d67bc37b8d392d13a0a6a7312678435efade4fd7449ec2ed52945c52abe3b85d`  
		Last Modified: Thu, 07 Sep 2023 01:30:23 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3410bb24e7a70dfce7810cf4736b3f0e0a420444d7825a7d1a9a1309c56e7e`  
		Last Modified: Thu, 07 Sep 2023 01:30:23 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e526b2a03229b6f0cd56ffc8d6c5600b8eec7f407d56686697c3684634adbc52`  
		Last Modified: Thu, 07 Sep 2023 01:30:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.3.2`

```console
$ docker pull couchdb@sha256:e8953219cd8060c67f54d22c33dea2ce4fc28ef73dc7ee185f5b7b169fa68d81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `couchdb:3.3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:02832d7f19f13a29f2204c7df8d8d291f08458fc4629d391385804e28bb180b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90240618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c17aff6559a55c79fb79af0c34cd1eea8b73c163feaf7cf8bb6c06f45cdfb4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:13 GMT
ADD file:cb5fcc80c057b356a31492a20c6e3a75b70ed70a663506c8e97ad730ae32a02d in / 
# Thu, 07 Sep 2023 00:21:13 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 03:12:14 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 07 Sep 2023 03:12:14 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 07 Sep 2023 03:12:21 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 03:12:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Thu, 07 Sep 2023 03:12:24 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 07 Sep 2023 03:12:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 03:12:30 GMT
ENV COUCHDB_VERSION=3.3.2
# Thu, 07 Sep 2023 03:12:30 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 07 Sep 2023 03:12:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 07 Sep 2023 03:12:44 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 07 Sep 2023 03:12:44 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Thu, 07 Sep 2023 03:12:44 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Thu, 07 Sep 2023 03:12:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 07 Sep 2023 03:12:44 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 03:12:44 GMT
VOLUME [/opt/couchdb/data]
# Thu, 07 Sep 2023 03:12:45 GMT
EXPOSE 4369 5984 9100
# Thu, 07 Sep 2023 03:12:45 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7d97e254a0461b0a30b3f443f1daa0d620a3cc6ff4e2714cc1cfd96ace5b7a7e`  
		Last Modified: Thu, 07 Sep 2023 00:26:03 GMT  
		Size: 31.4 MB (31417503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b10030446fdd0d136101a551c87b3e56c9a0f0e844b023d3e383c7fe3993b0`  
		Last Modified: Thu, 07 Sep 2023 03:14:26 GMT  
		Size: 3.4 KB (3406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd552b907af3faa1ebc8991aad6352e1056fc5af04762561d1cb7a62aad656f`  
		Last Modified: Thu, 07 Sep 2023 03:14:25 GMT  
		Size: 5.2 MB (5224504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e811bda8d2c68d90b0d4e405545695fd9524161110f1f6fec20eb6c4ee916dd1`  
		Last Modified: Thu, 07 Sep 2023 03:14:24 GMT  
		Size: 610.3 KB (610280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879da14f5933aee5916360f94692440f0d23977de3c242a7da7606295f6ae24e`  
		Last Modified: Thu, 07 Sep 2023 03:14:24 GMT  
		Size: 294.4 KB (294434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8360159bbbccf06b8d3871f1c45b590a27af89a1311ed1ac933104ec984983cb`  
		Last Modified: Thu, 07 Sep 2023 03:14:24 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd9bf0116d5301b0177a08522799ad0cbb296d0f751e3a772de170f4f58d027`  
		Last Modified: Thu, 07 Sep 2023 03:14:27 GMT  
		Size: 52.7 MB (52686485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f80c6f991c0d5cca5f5d92d718f6a9b19bc3b33dcdc901e64938f44ea13bcac`  
		Last Modified: Thu, 07 Sep 2023 03:14:22 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:575e513b07df4f16231083a48874564817ce2a73a148c2413bd4cf70d43f7bb9`  
		Last Modified: Thu, 07 Sep 2023 03:14:22 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf3ab5d6201e72b14659296edd3d9097facf30d368f435aedc1a317db0f94f1`  
		Last Modified: Thu, 07 Sep 2023 03:14:22 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021341363b5eb87a0b91fae27aa9246a6b0bf04b76c392e6e2266dd17d993e7d`  
		Last Modified: Thu, 07 Sep 2023 03:14:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:85dc5e7c838060a6fad9ed40f51c411edcdd913166d82fdc8134de2198c9955c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88684894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c368e49fd3cb709a0a99fdf41accaecb295353d6a5f0424d0af0fd3868203c3`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:53 GMT
ADD file:abd1ad48ae3ebec7a6ecc8ce3016c25be2afcbaedfcb904bc89b1ce59400aef0 in / 
# Thu, 07 Sep 2023 00:39:54 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 06:28:07 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 07 Sep 2023 06:28:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 07 Sep 2023 06:28:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 06:28:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Thu, 07 Sep 2023 06:28:17 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 07 Sep 2023 06:28:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 06:28:22 GMT
ENV COUCHDB_VERSION=3.3.2
# Thu, 07 Sep 2023 06:28:22 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 07 Sep 2023 06:28:34 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 07 Sep 2023 06:28:34 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 07 Sep 2023 06:28:35 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Thu, 07 Sep 2023 06:28:35 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Thu, 07 Sep 2023 06:28:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 07 Sep 2023 06:28:35 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 06:28:35 GMT
VOLUME [/opt/couchdb/data]
# Thu, 07 Sep 2023 06:28:35 GMT
EXPOSE 4369 5984 9100
# Thu, 07 Sep 2023 06:28:35 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f96ab15157043879c2ff23e0556e798eba6a6ff3d7fd5d1384de223bb9f66f1d`  
		Last Modified: Thu, 07 Sep 2023 00:43:41 GMT  
		Size: 30.1 MB (30062903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c5c525e9a401f87cbeb96f0fbeeac0a91eaccdcd8db647be875a18d0ecc9e5`  
		Last Modified: Thu, 07 Sep 2023 06:29:53 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1140236b7ef472420d39b000db183b4f5cd0c2b6f67297a94aaedef621bc93d4`  
		Last Modified: Thu, 07 Sep 2023 06:29:52 GMT  
		Size: 5.2 MB (5209505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b70041a20448d6e2ac7c5ca6d48c56ece09df5c2a0d368b03a1d76fb0f6ee4`  
		Last Modified: Thu, 07 Sep 2023 06:29:52 GMT  
		Size: 566.3 KB (566272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7bf33e25a4a45b5ad0d3341279d7b5055f176896ef97bca7676740c93f74e48`  
		Last Modified: Thu, 07 Sep 2023 06:29:52 GMT  
		Size: 294.3 KB (294303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdba8baef2d8ec8e8c63b46f53515805abed670b729452b79e83edb858e09257`  
		Last Modified: Thu, 07 Sep 2023 06:29:51 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9988a1ff60ee8c9b5557dd18b7c66d0afbe26845feb2cc1496836087b5a13208`  
		Last Modified: Thu, 07 Sep 2023 06:29:54 GMT  
		Size: 52.5 MB (52544467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b669cbe915c91df4045d11cfb7d2cb76339d372bd061cfbef8e8ea6fc54ea24`  
		Last Modified: Thu, 07 Sep 2023 06:29:50 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3b30e1fd8d0a982e29ee8ce8c5134088a29deeb62b31c6a42eddac672e0daf`  
		Last Modified: Thu, 07 Sep 2023 06:29:50 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2bf8aab77cdd6688ab927136a0584d5aaa18894964cb40a63678b454e2059f6`  
		Last Modified: Thu, 07 Sep 2023 06:29:49 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb64e9ab99bf15e9ef95b9a0875b45fc34e2425cd3f243032940137ebff8764`  
		Last Modified: Thu, 07 Sep 2023 06:29:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3.2` - linux; ppc64le

```console
$ docker pull couchdb@sha256:e4afbddd20d5602c062d5ca41cdb6a1d7a78de696d3964c1cc389141082bda45
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95962425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6c339fc7925afa097c86945fc7b6f20191a882f4ec40849b783ded191c02786`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 07 Sep 2023 00:18:05 GMT
ADD file:bf50998bef8a71b4723f6c17cc5c3e929d9c3b7a71b56060fea91ea0cd3502c4 in / 
# Thu, 07 Sep 2023 00:18:08 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 11:13:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 07 Sep 2023 11:13:10 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 07 Sep 2023 11:13:40 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 11:13:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Thu, 07 Sep 2023 11:13:57 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 07 Sep 2023 11:14:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 11:14:20 GMT
ENV COUCHDB_VERSION=3.3.2
# Thu, 07 Sep 2023 11:14:26 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 07 Sep 2023 11:15:21 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 07 Sep 2023 11:15:24 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 07 Sep 2023 11:15:24 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Thu, 07 Sep 2023 11:15:24 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Thu, 07 Sep 2023 11:15:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 07 Sep 2023 11:15:27 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 11:15:28 GMT
VOLUME [/opt/couchdb/data]
# Thu, 07 Sep 2023 11:15:28 GMT
EXPOSE 4369 5984 9100
# Thu, 07 Sep 2023 11:15:29 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:2365f3cb8bc5e18258159454852d941d92577738f79c1b5594afaec8481b47f3`  
		Last Modified: Thu, 07 Sep 2023 00:24:24 GMT  
		Size: 35.3 MB (35291070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9197661e71fa84ad86506d3d9ac8079e03a137bec2492f459dc5656517510aa`  
		Last Modified: Thu, 07 Sep 2023 11:16:22 GMT  
		Size: 3.4 KB (3408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9690fd9111712c1dade749e94a2e7367551269fdcffb6c26e10ecb52faa0727`  
		Last Modified: Thu, 07 Sep 2023 11:16:22 GMT  
		Size: 6.0 MB (6044149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d822eee3564d1dd298ee8b44c6eb02d708983fa42676fe8bf7cd42e90eb40a3e`  
		Last Modified: Thu, 07 Sep 2023 11:16:21 GMT  
		Size: 662.2 KB (662190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6578c7ea8724a9ca6f541b5abf3c2d2b0f9ea4b642f52c7bbb10e22dc9b9b3`  
		Last Modified: Thu, 07 Sep 2023 11:16:20 GMT  
		Size: 294.4 KB (294428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c794339b279fee84db7b50f5e8af3d2aaf5f4bffd6af7ac283f4a2633db832`  
		Last Modified: Thu, 07 Sep 2023 11:16:20 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df718b6717ac542cea1677798afd4fdca012056d7411d33e32c7ce7a08219de`  
		Last Modified: Thu, 07 Sep 2023 11:16:27 GMT  
		Size: 53.7 MB (53663170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4046af08908fbf960dd19fb398cbd2d25103dc62f9f6ff8decc9accf5c5d524`  
		Last Modified: Thu, 07 Sep 2023 11:16:18 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87160bd19bf8afffdf7d96264be30b0184cf6d61091cc4affaaf9eb33b6f024`  
		Last Modified: Thu, 07 Sep 2023 11:16:18 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c085c9cd3d2feb5d17923b0dd75e1b6cbae59ac438eb18fc8bc971daa3173c53`  
		Last Modified: Thu, 07 Sep 2023 11:16:18 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff09eb10bd8f4ec1918aa9fbd366247acaf103e29ca9c9eddacc7c610e6136a5`  
		Last Modified: Thu, 07 Sep 2023 11:16:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3.2` - linux; s390x

```console
$ docker pull couchdb@sha256:29e829b586b1cb6e650b0e13797721b362071a74370a5f6680669c847090f45a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86992619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192ddd69ff7e41d2bdf0975625c068953c9226f56fe985a51b032813e5bb8c66`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 07 Sep 2023 00:44:33 GMT
ADD file:fb2f216acd6d0ecaf48e8d5dd7e3cdb5d1f51d414f2011ed318cb494f96d89ca in / 
# Thu, 07 Sep 2023 00:44:37 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 01:28:56 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 07 Sep 2023 01:28:58 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 07 Sep 2023 01:29:11 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 01:29:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Thu, 07 Sep 2023 01:29:17 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 07 Sep 2023 01:29:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 01:29:27 GMT
ENV COUCHDB_VERSION=3.3.2
# Thu, 07 Sep 2023 01:29:28 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 07 Sep 2023 01:29:56 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 07 Sep 2023 01:30:05 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 07 Sep 2023 01:30:05 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Thu, 07 Sep 2023 01:30:05 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Thu, 07 Sep 2023 01:30:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 07 Sep 2023 01:30:07 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 01:30:07 GMT
VOLUME [/opt/couchdb/data]
# Thu, 07 Sep 2023 01:30:08 GMT
EXPOSE 4369 5984 9100
# Thu, 07 Sep 2023 01:30:09 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c9501ad9402d64e6c612fa1bb94f16df51188e681dc1f28c603a6109f06f22d7`  
		Last Modified: Thu, 07 Sep 2023 00:50:10 GMT  
		Size: 29.7 MB (29652801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996ad4371fbc51ce08543507129d65ab8b90dd855e656f8eabd70335c57bb0a1`  
		Last Modified: Thu, 07 Sep 2023 01:30:26 GMT  
		Size: 3.4 KB (3435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e0fe5808ef043ae040668477d7e9dfe710765ea40e3d011b82fa33031b7ea4`  
		Last Modified: Thu, 07 Sep 2023 01:30:25 GMT  
		Size: 5.1 MB (5110534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f126aebc8a50e39748585e27d5fd5a9836b6a93c873802d3d3403b156cac952`  
		Last Modified: Thu, 07 Sep 2023 01:30:25 GMT  
		Size: 573.0 KB (573029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f00d25b2e1271b6380742fbbeca5c10b9b084a78cfba7f031f12a3d00a87df5`  
		Last Modified: Thu, 07 Sep 2023 01:30:24 GMT  
		Size: 294.5 KB (294462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577394d2327382521d14f38714c2247fd0db46e1ab49b86cb2350c309835db81`  
		Last Modified: Thu, 07 Sep 2023 01:30:24 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4258fc35f99c32658815e5ea98c85edc9f278bcba6613030c57395fc75cae139`  
		Last Modified: Thu, 07 Sep 2023 01:30:28 GMT  
		Size: 51.4 MB (51354348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0bdcf38e015804f9400dd02e2614c14ea270ce30cfc9602fc0bf39c87dd1fb`  
		Last Modified: Thu, 07 Sep 2023 01:30:23 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d67bc37b8d392d13a0a6a7312678435efade4fd7449ec2ed52945c52abe3b85d`  
		Last Modified: Thu, 07 Sep 2023 01:30:23 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3410bb24e7a70dfce7810cf4736b3f0e0a420444d7825a7d1a9a1309c56e7e`  
		Last Modified: Thu, 07 Sep 2023 01:30:23 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e526b2a03229b6f0cd56ffc8d6c5600b8eec7f407d56686697c3684634adbc52`  
		Last Modified: Thu, 07 Sep 2023 01:30:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:e8953219cd8060c67f54d22c33dea2ce4fc28ef73dc7ee185f5b7b169fa68d81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:02832d7f19f13a29f2204c7df8d8d291f08458fc4629d391385804e28bb180b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90240618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c17aff6559a55c79fb79af0c34cd1eea8b73c163feaf7cf8bb6c06f45cdfb4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:13 GMT
ADD file:cb5fcc80c057b356a31492a20c6e3a75b70ed70a663506c8e97ad730ae32a02d in / 
# Thu, 07 Sep 2023 00:21:13 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 03:12:14 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 07 Sep 2023 03:12:14 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 07 Sep 2023 03:12:21 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 03:12:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Thu, 07 Sep 2023 03:12:24 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 07 Sep 2023 03:12:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 03:12:30 GMT
ENV COUCHDB_VERSION=3.3.2
# Thu, 07 Sep 2023 03:12:30 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 07 Sep 2023 03:12:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 07 Sep 2023 03:12:44 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 07 Sep 2023 03:12:44 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Thu, 07 Sep 2023 03:12:44 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Thu, 07 Sep 2023 03:12:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 07 Sep 2023 03:12:44 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 03:12:44 GMT
VOLUME [/opt/couchdb/data]
# Thu, 07 Sep 2023 03:12:45 GMT
EXPOSE 4369 5984 9100
# Thu, 07 Sep 2023 03:12:45 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7d97e254a0461b0a30b3f443f1daa0d620a3cc6ff4e2714cc1cfd96ace5b7a7e`  
		Last Modified: Thu, 07 Sep 2023 00:26:03 GMT  
		Size: 31.4 MB (31417503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b10030446fdd0d136101a551c87b3e56c9a0f0e844b023d3e383c7fe3993b0`  
		Last Modified: Thu, 07 Sep 2023 03:14:26 GMT  
		Size: 3.4 KB (3406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd552b907af3faa1ebc8991aad6352e1056fc5af04762561d1cb7a62aad656f`  
		Last Modified: Thu, 07 Sep 2023 03:14:25 GMT  
		Size: 5.2 MB (5224504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e811bda8d2c68d90b0d4e405545695fd9524161110f1f6fec20eb6c4ee916dd1`  
		Last Modified: Thu, 07 Sep 2023 03:14:24 GMT  
		Size: 610.3 KB (610280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879da14f5933aee5916360f94692440f0d23977de3c242a7da7606295f6ae24e`  
		Last Modified: Thu, 07 Sep 2023 03:14:24 GMT  
		Size: 294.4 KB (294434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8360159bbbccf06b8d3871f1c45b590a27af89a1311ed1ac933104ec984983cb`  
		Last Modified: Thu, 07 Sep 2023 03:14:24 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd9bf0116d5301b0177a08522799ad0cbb296d0f751e3a772de170f4f58d027`  
		Last Modified: Thu, 07 Sep 2023 03:14:27 GMT  
		Size: 52.7 MB (52686485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f80c6f991c0d5cca5f5d92d718f6a9b19bc3b33dcdc901e64938f44ea13bcac`  
		Last Modified: Thu, 07 Sep 2023 03:14:22 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:575e513b07df4f16231083a48874564817ce2a73a148c2413bd4cf70d43f7bb9`  
		Last Modified: Thu, 07 Sep 2023 03:14:22 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf3ab5d6201e72b14659296edd3d9097facf30d368f435aedc1a317db0f94f1`  
		Last Modified: Thu, 07 Sep 2023 03:14:22 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021341363b5eb87a0b91fae27aa9246a6b0bf04b76c392e6e2266dd17d993e7d`  
		Last Modified: Thu, 07 Sep 2023 03:14:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:85dc5e7c838060a6fad9ed40f51c411edcdd913166d82fdc8134de2198c9955c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88684894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c368e49fd3cb709a0a99fdf41accaecb295353d6a5f0424d0af0fd3868203c3`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:53 GMT
ADD file:abd1ad48ae3ebec7a6ecc8ce3016c25be2afcbaedfcb904bc89b1ce59400aef0 in / 
# Thu, 07 Sep 2023 00:39:54 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 06:28:07 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 07 Sep 2023 06:28:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 07 Sep 2023 06:28:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 06:28:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Thu, 07 Sep 2023 06:28:17 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 07 Sep 2023 06:28:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 06:28:22 GMT
ENV COUCHDB_VERSION=3.3.2
# Thu, 07 Sep 2023 06:28:22 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 07 Sep 2023 06:28:34 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 07 Sep 2023 06:28:34 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 07 Sep 2023 06:28:35 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Thu, 07 Sep 2023 06:28:35 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Thu, 07 Sep 2023 06:28:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 07 Sep 2023 06:28:35 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 06:28:35 GMT
VOLUME [/opt/couchdb/data]
# Thu, 07 Sep 2023 06:28:35 GMT
EXPOSE 4369 5984 9100
# Thu, 07 Sep 2023 06:28:35 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:f96ab15157043879c2ff23e0556e798eba6a6ff3d7fd5d1384de223bb9f66f1d`  
		Last Modified: Thu, 07 Sep 2023 00:43:41 GMT  
		Size: 30.1 MB (30062903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c5c525e9a401f87cbeb96f0fbeeac0a91eaccdcd8db647be875a18d0ecc9e5`  
		Last Modified: Thu, 07 Sep 2023 06:29:53 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1140236b7ef472420d39b000db183b4f5cd0c2b6f67297a94aaedef621bc93d4`  
		Last Modified: Thu, 07 Sep 2023 06:29:52 GMT  
		Size: 5.2 MB (5209505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b70041a20448d6e2ac7c5ca6d48c56ece09df5c2a0d368b03a1d76fb0f6ee4`  
		Last Modified: Thu, 07 Sep 2023 06:29:52 GMT  
		Size: 566.3 KB (566272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7bf33e25a4a45b5ad0d3341279d7b5055f176896ef97bca7676740c93f74e48`  
		Last Modified: Thu, 07 Sep 2023 06:29:52 GMT  
		Size: 294.3 KB (294303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdba8baef2d8ec8e8c63b46f53515805abed670b729452b79e83edb858e09257`  
		Last Modified: Thu, 07 Sep 2023 06:29:51 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9988a1ff60ee8c9b5557dd18b7c66d0afbe26845feb2cc1496836087b5a13208`  
		Last Modified: Thu, 07 Sep 2023 06:29:54 GMT  
		Size: 52.5 MB (52544467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b669cbe915c91df4045d11cfb7d2cb76339d372bd061cfbef8e8ea6fc54ea24`  
		Last Modified: Thu, 07 Sep 2023 06:29:50 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3b30e1fd8d0a982e29ee8ce8c5134088a29deeb62b31c6a42eddac672e0daf`  
		Last Modified: Thu, 07 Sep 2023 06:29:50 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2bf8aab77cdd6688ab927136a0584d5aaa18894964cb40a63678b454e2059f6`  
		Last Modified: Thu, 07 Sep 2023 06:29:49 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb64e9ab99bf15e9ef95b9a0875b45fc34e2425cd3f243032940137ebff8764`  
		Last Modified: Thu, 07 Sep 2023 06:29:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:e4afbddd20d5602c062d5ca41cdb6a1d7a78de696d3964c1cc389141082bda45
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95962425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6c339fc7925afa097c86945fc7b6f20191a882f4ec40849b783ded191c02786`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 07 Sep 2023 00:18:05 GMT
ADD file:bf50998bef8a71b4723f6c17cc5c3e929d9c3b7a71b56060fea91ea0cd3502c4 in / 
# Thu, 07 Sep 2023 00:18:08 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 11:13:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 07 Sep 2023 11:13:10 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 07 Sep 2023 11:13:40 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 11:13:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Thu, 07 Sep 2023 11:13:57 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 07 Sep 2023 11:14:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 11:14:20 GMT
ENV COUCHDB_VERSION=3.3.2
# Thu, 07 Sep 2023 11:14:26 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 07 Sep 2023 11:15:21 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 07 Sep 2023 11:15:24 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 07 Sep 2023 11:15:24 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Thu, 07 Sep 2023 11:15:24 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Thu, 07 Sep 2023 11:15:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 07 Sep 2023 11:15:27 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 11:15:28 GMT
VOLUME [/opt/couchdb/data]
# Thu, 07 Sep 2023 11:15:28 GMT
EXPOSE 4369 5984 9100
# Thu, 07 Sep 2023 11:15:29 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:2365f3cb8bc5e18258159454852d941d92577738f79c1b5594afaec8481b47f3`  
		Last Modified: Thu, 07 Sep 2023 00:24:24 GMT  
		Size: 35.3 MB (35291070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9197661e71fa84ad86506d3d9ac8079e03a137bec2492f459dc5656517510aa`  
		Last Modified: Thu, 07 Sep 2023 11:16:22 GMT  
		Size: 3.4 KB (3408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9690fd9111712c1dade749e94a2e7367551269fdcffb6c26e10ecb52faa0727`  
		Last Modified: Thu, 07 Sep 2023 11:16:22 GMT  
		Size: 6.0 MB (6044149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d822eee3564d1dd298ee8b44c6eb02d708983fa42676fe8bf7cd42e90eb40a3e`  
		Last Modified: Thu, 07 Sep 2023 11:16:21 GMT  
		Size: 662.2 KB (662190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6578c7ea8724a9ca6f541b5abf3c2d2b0f9ea4b642f52c7bbb10e22dc9b9b3`  
		Last Modified: Thu, 07 Sep 2023 11:16:20 GMT  
		Size: 294.4 KB (294428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c794339b279fee84db7b50f5e8af3d2aaf5f4bffd6af7ac283f4a2633db832`  
		Last Modified: Thu, 07 Sep 2023 11:16:20 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df718b6717ac542cea1677798afd4fdca012056d7411d33e32c7ce7a08219de`  
		Last Modified: Thu, 07 Sep 2023 11:16:27 GMT  
		Size: 53.7 MB (53663170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4046af08908fbf960dd19fb398cbd2d25103dc62f9f6ff8decc9accf5c5d524`  
		Last Modified: Thu, 07 Sep 2023 11:16:18 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87160bd19bf8afffdf7d96264be30b0184cf6d61091cc4affaaf9eb33b6f024`  
		Last Modified: Thu, 07 Sep 2023 11:16:18 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c085c9cd3d2feb5d17923b0dd75e1b6cbae59ac438eb18fc8bc971daa3173c53`  
		Last Modified: Thu, 07 Sep 2023 11:16:18 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff09eb10bd8f4ec1918aa9fbd366247acaf103e29ca9c9eddacc7c610e6136a5`  
		Last Modified: Thu, 07 Sep 2023 11:16:18 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:29e829b586b1cb6e650b0e13797721b362071a74370a5f6680669c847090f45a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86992619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192ddd69ff7e41d2bdf0975625c068953c9226f56fe985a51b032813e5bb8c66`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 07 Sep 2023 00:44:33 GMT
ADD file:fb2f216acd6d0ecaf48e8d5dd7e3cdb5d1f51d414f2011ed318cb494f96d89ca in / 
# Thu, 07 Sep 2023 00:44:37 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 01:28:56 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 07 Sep 2023 01:28:58 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 07 Sep 2023 01:29:11 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 01:29:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Thu, 07 Sep 2023 01:29:17 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 07 Sep 2023 01:29:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 01:29:27 GMT
ENV COUCHDB_VERSION=3.3.2
# Thu, 07 Sep 2023 01:29:28 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 07 Sep 2023 01:29:56 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 07 Sep 2023 01:30:05 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 07 Sep 2023 01:30:05 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Thu, 07 Sep 2023 01:30:05 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Thu, 07 Sep 2023 01:30:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 07 Sep 2023 01:30:07 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 01:30:07 GMT
VOLUME [/opt/couchdb/data]
# Thu, 07 Sep 2023 01:30:08 GMT
EXPOSE 4369 5984 9100
# Thu, 07 Sep 2023 01:30:09 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c9501ad9402d64e6c612fa1bb94f16df51188e681dc1f28c603a6109f06f22d7`  
		Last Modified: Thu, 07 Sep 2023 00:50:10 GMT  
		Size: 29.7 MB (29652801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996ad4371fbc51ce08543507129d65ab8b90dd855e656f8eabd70335c57bb0a1`  
		Last Modified: Thu, 07 Sep 2023 01:30:26 GMT  
		Size: 3.4 KB (3435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e0fe5808ef043ae040668477d7e9dfe710765ea40e3d011b82fa33031b7ea4`  
		Last Modified: Thu, 07 Sep 2023 01:30:25 GMT  
		Size: 5.1 MB (5110534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f126aebc8a50e39748585e27d5fd5a9836b6a93c873802d3d3403b156cac952`  
		Last Modified: Thu, 07 Sep 2023 01:30:25 GMT  
		Size: 573.0 KB (573029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f00d25b2e1271b6380742fbbeca5c10b9b084a78cfba7f031f12a3d00a87df5`  
		Last Modified: Thu, 07 Sep 2023 01:30:24 GMT  
		Size: 294.5 KB (294462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577394d2327382521d14f38714c2247fd0db46e1ab49b86cb2350c309835db81`  
		Last Modified: Thu, 07 Sep 2023 01:30:24 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4258fc35f99c32658815e5ea98c85edc9f278bcba6613030c57395fc75cae139`  
		Last Modified: Thu, 07 Sep 2023 01:30:28 GMT  
		Size: 51.4 MB (51354348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0bdcf38e015804f9400dd02e2614c14ea270ce30cfc9602fc0bf39c87dd1fb`  
		Last Modified: Thu, 07 Sep 2023 01:30:23 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d67bc37b8d392d13a0a6a7312678435efade4fd7449ec2ed52945c52abe3b85d`  
		Last Modified: Thu, 07 Sep 2023 01:30:23 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3410bb24e7a70dfce7810cf4736b3f0e0a420444d7825a7d1a9a1309c56e7e`  
		Last Modified: Thu, 07 Sep 2023 01:30:23 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e526b2a03229b6f0cd56ffc8d6c5600b8eec7f407d56686697c3684634adbc52`  
		Last Modified: Thu, 07 Sep 2023 01:30:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
