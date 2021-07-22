## `couchdb:latest`

```console
$ docker pull couchdb@sha256:ade1703ef61ebb276b574675d43de47a24808df59cb50d79b0b69786b4c14099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:aa4ca065a91c36bbee201730dbd34bed1685a11a75e15bb4973268407a15bf79
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.8 MB (83771234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cf953a0e1c4aa635d7979afd3b6e4c7c723955e4527dd39b91f1efb018c7bbc`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:29:49 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 22 Jul 2021 01:29:50 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 22 Jul 2021 01:29:58 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:30:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 22 Jul 2021 01:30:03 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 22 Jul 2021 01:30:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:30:11 GMT
ENV COUCHDB_VERSION=3.1.1
# Thu, 22 Jul 2021 01:30:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 22 Jul 2021 01:30:31 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 22 Jul 2021 01:30:31 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 22 Jul 2021 01:30:32 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 22 Jul 2021 01:30:32 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Thu, 22 Jul 2021 01:30:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 22 Jul 2021 01:30:34 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 22 Jul 2021 01:30:34 GMT
VOLUME [/opt/couchdb/data]
# Thu, 22 Jul 2021 01:30:35 GMT
EXPOSE 4369 5984 9100
# Thu, 22 Jul 2021 01:30:35 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835b688d207b5ab9e89d8cca5f4bf328bfe1f1ede763194a4538ea6fa23da011`  
		Last Modified: Thu, 22 Jul 2021 01:31:45 GMT  
		Size: 3.4 KB (3415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04943acd4d5ea8d1bedf669be78f6a293687056354f3d796a81843b9ec6d2f6e`  
		Last Modified: Thu, 22 Jul 2021 01:31:45 GMT  
		Size: 6.7 MB (6690574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9997c1f5399e25cd41b8489eb0e0394b2f5fba04b0d872a546cb32cf7c272535`  
		Last Modified: Thu, 22 Jul 2021 01:31:43 GMT  
		Size: 1.3 MB (1258344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429ec9af1234b1a0ca0cb627723e4f03410bc1972d6fe4f15b4a730bd3bfd651`  
		Last Modified: Thu, 22 Jul 2021 01:31:42 GMT  
		Size: 293.0 KB (293013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfc6e010df6e6b577a74e9eea1410a6eed1ad69db8d5cfce8c7b0fefc22609b9`  
		Last Modified: Thu, 22 Jul 2021 01:31:42 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c88c15d7fabfe39975f3b6b5d177076bdfae08e05b8462f20bea42544c8aa8`  
		Last Modified: Thu, 22 Jul 2021 01:31:48 GMT  
		Size: 48.4 MB (48376497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97242ba0044f0aec5fbf85a67230ca43fa4981f44ed600a3452fc15492d43374`  
		Last Modified: Thu, 22 Jul 2021 01:31:40 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6403aee522aab15bca7e6422b1ce27325056865370e375bd73f4f660ee9ce5`  
		Last Modified: Thu, 22 Jul 2021 01:31:39 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a327d1fe4ab8fce33608f39b7631107d9c8573e22e829fe9f914463bff6a02e2`  
		Last Modified: Thu, 22 Jul 2021 01:31:39 GMT  
		Size: 2.1 KB (2055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c492e57bffa3b58bf0eb05858221452abb78712c4c06bd72d08193648342b699`  
		Last Modified: Thu, 22 Jul 2021 01:31:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:37d8d0c80c78a6e9633eeb6412b807ea08a55a1a91c29e85a7f8ae900299351b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.8 MB (78786504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a26a990102953a196bd6c1ee011b46f2f4d9f32f31b4e4d06d4bf73eeff0dd9`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Thu, 22 Jul 2021 00:40:14 GMT
ADD file:074ffc2065bab83c9a5c596576656b04d271dd78406aadad160b68e38f38269f in / 
# Thu, 22 Jul 2021 00:40:14 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 04:10:26 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Thu, 22 Jul 2021 04:10:27 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Thu, 22 Jul 2021 04:10:35 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 04:10:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Thu, 22 Jul 2021 04:10:39 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Thu, 22 Jul 2021 04:10:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 04:10:46 GMT
ENV COUCHDB_VERSION=3.1.1
# Thu, 22 Jul 2021 04:10:46 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Thu, 22 Jul 2021 04:10:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Thu, 22 Jul 2021 04:10:59 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Thu, 22 Jul 2021 04:11:00 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Thu, 22 Jul 2021 04:11:00 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Thu, 22 Jul 2021 04:11:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Thu, 22 Jul 2021 04:11:01 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Thu, 22 Jul 2021 04:11:01 GMT
VOLUME [/opt/couchdb/data]
# Thu, 22 Jul 2021 04:11:01 GMT
EXPOSE 4369 5984 9100
# Thu, 22 Jul 2021 04:11:01 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:513c6babab2b9079da61a69300c0e26d1037ca98910376098e9ae87baeb112c0`  
		Last Modified: Thu, 22 Jul 2021 00:45:53 GMT  
		Size: 25.9 MB (25914794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3563217664ef686801ac1f16499d3078070568e6f515fa31bb0cecfe3c4160cb`  
		Last Modified: Thu, 22 Jul 2021 04:11:57 GMT  
		Size: 3.4 KB (3439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8649c33ded578f444c54f5681c656884d0535152ffc9dfdddc9cc427c26f0499`  
		Last Modified: Thu, 22 Jul 2021 04:11:57 GMT  
		Size: 6.6 MB (6550164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf3e3eb52319d0aec41210287a76db19674c90a22f24ab94406318cf2ad4119`  
		Last Modified: Thu, 22 Jul 2021 04:11:56 GMT  
		Size: 1.2 MB (1163428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6740836a203deb0450b7e2700c90c1580ea8da5397a230ace7271ce6759f4b0a`  
		Last Modified: Thu, 22 Jul 2021 04:11:56 GMT  
		Size: 292.8 KB (292841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80173b905d901864e3a8408953243ff8f4b921e8038f2a19b3e2673d12324b9d`  
		Last Modified: Thu, 22 Jul 2021 04:11:54 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8d2ba4beb97afa6bed0b23529fc32bb187c9e15d08678866385d6cee9d65fc`  
		Last Modified: Thu, 22 Jul 2021 04:11:58 GMT  
		Size: 44.9 MB (44858243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9067bf77df10c52493a9a0327397455c82c45323164c69a31a63c559d1b1756`  
		Last Modified: Thu, 22 Jul 2021 04:11:52 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a439b4e9ff2e13e922f55dd64190526d9a444809d3fa39f1e1f8f27ebf84f302`  
		Last Modified: Thu, 22 Jul 2021 04:11:53 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8780f4b4f0e2aaa3c6ba582a58fe58879cb8e6fb19ab8adebb3c929349b6a6`  
		Last Modified: Thu, 22 Jul 2021 04:11:52 GMT  
		Size: 2.1 KB (2055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe05ca9838e9992880344232d33f935ee56df3399413109bc70436ecf754fd4`  
		Last Modified: Thu, 22 Jul 2021 04:11:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
