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
