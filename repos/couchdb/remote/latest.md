## `couchdb:latest`

```console
$ docker pull couchdb@sha256:ca82ef134e60134eb3e6c008b0392d94a55d4214940fea9346c02bd9bfd5682c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:5ccc6c66424ba8f001e32cb6958d2c670eb7e64cd8faa673ebe464701e3ef2ac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.4 MB (87437899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f8f8b3f38bc0cac4b5a00c27798b2f2417779f874d2123002b8bc619a6b74d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:35 GMT
ADD file:90495c24c897ec47982e200f732f8be3109fcd791691ddffae0756898f91024f in / 
# Wed, 26 Jan 2022 01:40:36 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:11:06 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 01 Mar 2022 02:11:06 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 01 Mar 2022 02:11:16 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 02:11:20 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 01 Mar 2022 02:11:20 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 01 Mar 2022 02:11:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 02:11:26 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Tue, 01 Mar 2022 02:11:26 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 01 Mar 2022 02:11:40 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 01 Mar 2022 02:11:40 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 01 Mar 2022 02:11:40 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 01 Mar 2022 02:11:40 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 01 Mar 2022 02:11:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 02:11:41 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 01 Mar 2022 02:11:41 GMT
VOLUME [/opt/couchdb/data]
# Tue, 01 Mar 2022 02:11:41 GMT
EXPOSE 4369 5984 9100
# Tue, 01 Mar 2022 02:11:41 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5eb5b503b37671af16371272f9c5313a3e82f1d0756e14506704489ad9900803`  
		Last Modified: Wed, 26 Jan 2022 01:46:39 GMT  
		Size: 31.4 MB (31366257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249b60f6deae79893785078b94133026ff5258e152ca360f3aab041bc9cc449c`  
		Last Modified: Tue, 01 Mar 2022 02:12:09 GMT  
		Size: 3.4 KB (3415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed17d6794ec71c2196a33c2ce7da8ba1a1bb0cd785feffc0e3a2e05b4d639373`  
		Last Modified: Tue, 01 Mar 2022 02:12:08 GMT  
		Size: 5.2 MB (5223226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96e537ae6fdaae9f7bea89d448d4843963b3ffea37778d244f39ee0e1f9e853`  
		Last Modified: Tue, 01 Mar 2022 02:12:07 GMT  
		Size: 1.6 MB (1553190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276430a271a5c2cb684da4f25f94df530e8e064e3f30e26866e282681f3fa331`  
		Last Modified: Tue, 01 Mar 2022 02:12:06 GMT  
		Size: 295.5 KB (295504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c81ae7113b157517edd2f307ca24ff806f8bd6e898df739185e86a26da68f5`  
		Last Modified: Tue, 01 Mar 2022 02:12:06 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012359ac5520cb0dab6b68a9991eca49f5602027bd0cce151a722cb257b39db0`  
		Last Modified: Tue, 01 Mar 2022 02:12:10 GMT  
		Size: 49.0 MB (48992574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03bd5346849e436082925d6823e19f635e9c3515123f02bd5041b048e04170ed`  
		Last Modified: Tue, 01 Mar 2022 02:12:04 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0538ab5322ad2797801b5c69426076c6c6602d8f95e908861e7aabac740db1fe`  
		Last Modified: Tue, 01 Mar 2022 02:12:04 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b435e070bac806072558aad51c8a49ac5f36aa9f2abef6b06a6e832009dbce`  
		Last Modified: Tue, 01 Mar 2022 02:12:04 GMT  
		Size: 2.2 KB (2189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a3375a5e2f6634706348f0dadcc9a7214f9ba05913a4a72f65eb236198e82e`  
		Last Modified: Tue, 01 Mar 2022 02:12:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:e5d35957f912e3052da1f811da4b4274634b794e1df0d3010f6f4298e1fbf524
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85578592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8234b78f6be5f35bfc91ce645114ad87939e55ef9b84f78cf2c91c8939199661`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:31 GMT
ADD file:0ec6f47a8857bf8e6cef71ed8f864be7ce1790ff6ed04fd4201e7dbde4728d3a in / 
# Wed, 26 Jan 2022 01:42:31 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 02:08:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 01 Mar 2022 02:08:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 01 Mar 2022 02:08:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 02:08:41 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 01 Mar 2022 02:08:42 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 01 Mar 2022 02:08:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 02:08:49 GMT
ENV COUCHDB_VERSION=3.2.1-1
# Tue, 01 Mar 2022 02:08:50 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 01 Mar 2022 02:09:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 01 Mar 2022 02:09:11 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 01 Mar 2022 02:09:12 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 01 Mar 2022 02:09:13 GMT
COPY file:0a26a859e55e89f8409b5ab4022d28cfe05edddfe16a742ba28c73ecdbcff9c1 in /usr/local/bin 
# Tue, 01 Mar 2022 02:09:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 02:09:14 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 01 Mar 2022 02:09:15 GMT
VOLUME [/opt/couchdb/data]
# Tue, 01 Mar 2022 02:09:16 GMT
EXPOSE 4369 5984 9100
# Tue, 01 Mar 2022 02:09:17 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:8998bd30e6a1204d13403045766edbe14f941b52087465f5d140ab63c8b113bf`  
		Last Modified: Wed, 26 Jan 2022 01:49:04 GMT  
		Size: 30.1 MB (30056774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5456ab3a7062aab6aaa4c5027fb4dc91c3767d0f67b263e0314e2d1676e66b5`  
		Last Modified: Tue, 01 Mar 2022 02:10:04 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220168defc5d939708db54c362b659b652e4efa42a9a5e2f9844ede2e235d997`  
		Last Modified: Tue, 01 Mar 2022 02:10:03 GMT  
		Size: 5.2 MB (5207997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041bf56f1d38e036c637a141a5e8ba27091616520de82ac56cb8129ba805a9f2`  
		Last Modified: Tue, 01 Mar 2022 02:10:02 GMT  
		Size: 1.2 MB (1220992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e43455933f95ad347fe7fa5ad03bc08e5fb1cd09821bc8ff69066013b0d65ba`  
		Last Modified: Tue, 01 Mar 2022 02:10:01 GMT  
		Size: 79.1 KB (79102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38eaa07951d9f39880560eba53b7c5ee98a8615b11aaa36fc64d0b2dd9221a1f`  
		Last Modified: Tue, 01 Mar 2022 02:10:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2a13362604627b4182542d67eea0a400f2c5c6b0b8548b410eff57379a64f5`  
		Last Modified: Tue, 01 Mar 2022 02:10:05 GMT  
		Size: 49.0 MB (49006669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab82342528b131665edf57239753899130d3e1bfce68e051171f434f545ad0cc`  
		Last Modified: Tue, 01 Mar 2022 02:09:59 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176dba8f6fce2e90ee5ab3ff6729e349225a32e72ac8923c3cc9bfbbe56c2c66`  
		Last Modified: Tue, 01 Mar 2022 02:09:59 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a70be98bbcf4d0e95881552c73a4addb595b993e1200c67db1c24bb08b6fab`  
		Last Modified: Tue, 01 Mar 2022 02:09:59 GMT  
		Size: 2.2 KB (2188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d967c6ba0b8d2a7690631426dc0326a8b6b94bb0075165e5055fe117a4fba482`  
		Last Modified: Tue, 01 Mar 2022 02:09:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:92fdcff2acc7fd2cd527494e222e1d706dc01024461fb474ccc1780073d6cce9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88524339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec66a11c353a0bd55a16bc9e3df7c1f8436b50846e164d74bbfc74a0e46883dd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 12 Mar 2021 02:32:43 GMT
ADD file:6a0c0cfa71979cf6fdd859dce1e32582f0e55ed382b9e17b77a2001defc2c9db in / 
# Fri, 12 Mar 2021 02:32:50 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 19:37:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 12 Mar 2021 19:37:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Fri, 12 Mar 2021 19:40:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 19:40:05 GMT
ENV GOSU_VERSION=1.11
# Fri, 12 Mar 2021 19:40:07 GMT
ENV TINI_VERSION=0.18.0
# Fri, 12 Mar 2021 19:42:25 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends wget;     rm -rf /var/lib/apt/lists/*;         dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')";         wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/${GOSU_VERSION}/gosu-$dpkgArch";     wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && break || : ;     done;     gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu;     rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc;     chmod +x /usr/local/bin/gosu;     gosu nobody true;         wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch";     wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v${TINI_VERSION}/tini-$dpkgArch.asc";     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do     gpg --batch --keyserver $server --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7 && break || : ;     done;     gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini;     rm -rf "$GNUPGHOME" /usr/local/bin/tini.asc;     chmod +x /usr/local/bin/tini;     apt-get purge -y --auto-remove wget;     tini --version
# Fri, 12 Mar 2021 19:42:43 GMT
ENV GPG_COUCH_KEY=8756C4F765C9AC3CB6B85D62379CE192D401AB61
# Fri, 12 Mar 2021 19:43:05 GMT
RUN set -xe;     export GNUPGHOME="$(mktemp -d)";     echo "disable-ipv6" >> ${GNUPGHOME}/dirmngr.conf;     for server in $(shuf -e pgpkeys.mit.edu         ha.pool.sks-keyservers.net         hkp://p80.pool.sks-keyservers.net:80         pgp.mit.edu) ; do         gpg --batch --keyserver $server --recv-keys $GPG_COUCH_KEY && break || : ;     done;     gpg --batch --export $GPG_COUCH_KEY > /etc/apt/trusted.gpg.d/couchdb.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list
# Fri, 12 Mar 2021 19:43:21 GMT
ENV COUCHDB_VERSION=3.1.1
# Fri, 12 Mar 2021 19:43:54 GMT
RUN echo "deb https://apache.bintray.com/couchdb-deb buster main" > /etc/apt/sources.list.d/couchdb.list
# Fri, 12 Mar 2021 19:45:52 GMT
RUN set -xe;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Fri, 12 Mar 2021 19:45:58 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Fri, 12 Mar 2021 19:46:00 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Fri, 12 Mar 2021 19:46:02 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Fri, 12 Mar 2021 19:46:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Fri, 12 Mar 2021 19:46:17 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 12 Mar 2021 19:46:26 GMT
VOLUME [/opt/couchdb/data]
# Fri, 12 Mar 2021 19:46:33 GMT
EXPOSE 4369 5984 9100
# Fri, 12 Mar 2021 19:46:38 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:1d686056fdac1848f4fd78ba2b335502055ffe98c79619e21d0c2fb7db95257e`  
		Last Modified: Fri, 12 Mar 2021 02:45:35 GMT  
		Size: 30.5 MB (30525728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5946aff0873110b0478f9227873604e78c676af18e0dfcd1792e829269a797`  
		Last Modified: Fri, 12 Mar 2021 19:50:07 GMT  
		Size: 3.4 KB (3418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459905054f02704e0526a50655150b20d4241a97be26f9464d997ec614782ce4`  
		Last Modified: Fri, 12 Mar 2021 19:50:07 GMT  
		Size: 7.6 MB (7597596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0fddccd01ec6846d36516b8583c310ef4af1b4df7e5ff47e9a5433bb7b1a6f1`  
		Last Modified: Fri, 12 Mar 2021 19:50:06 GMT  
		Size: 1.1 MB (1116351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a9cab3ce9525a6a24f4c1b583168b57d95c20d76c59eeec12e2e975f5bd6a1`  
		Last Modified: Fri, 12 Mar 2021 19:50:05 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09139ee3a9e5b64209b42b240aa99578fbf71585ea905c2eefccbd7c73cf31f3`  
		Last Modified: Fri, 12 Mar 2021 19:50:04 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7604a9876a71e095a20526d121d304d331595fb5d6a437dad6550e85747fde6e`  
		Last Modified: Fri, 12 Mar 2021 19:50:08 GMT  
		Size: 49.3 MB (49275194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:776c0c6539d199f069a602efa1cda1b72fb94ecd2bbc595b97f2df4e19ccb3e6`  
		Last Modified: Fri, 12 Mar 2021 19:49:59 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc447f4db7d5f4bbcd08dc6219def27d69bad292d2775d1e9cf212ca4277a1be`  
		Last Modified: Fri, 12 Mar 2021 19:49:59 GMT  
		Size: 769.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0524070537bcddee5cbfd0aef55fc47bd89ae91bd05bd1919fec7dc348e00d28`  
		Last Modified: Fri, 12 Mar 2021 19:49:59 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc8c9fce47f6e73a0786f841a42845cb7d720417f296a19ce54fd978cb02f0e`  
		Last Modified: Fri, 12 Mar 2021 19:49:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
