## `couchdb:latest`

```console
$ docker pull couchdb@sha256:25eab97850b89dfc4406a3e39c73a20dec7ce58f43b683d794b13c052dbfd8ae
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
$ docker pull couchdb@sha256:ba7d266cfcafd953c89ec0ad7fef8fe84b8e90d5a5547a9f1448665cc22f3529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134019745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfc65a758ed063bbfb136bf9388d27ac24c8d9d37a80798ee4abd25d7b386c55`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV COUCHDB_VERSION=3.4.1
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/couchdb/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04428aa47dc2724ff9a3c096e683413eadb6d72f9f35652d634c29e9bd3c858f`  
		Last Modified: Mon, 07 Oct 2024 17:59:15 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f9b3858f3817d0558d3270c568e8deb410ee1a0af169a0fbe36541c0811f3a`  
		Last Modified: Mon, 07 Oct 2024 17:59:16 GMT  
		Size: 7.9 MB (7874366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2404d461c3b8c6c2269f8be0f7a7e28ac21b0c163a3cc4bc9753448d56f9ecba`  
		Last Modified: Mon, 07 Oct 2024 17:59:15 GMT  
		Size: 392.1 KB (392100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cafc78cca8ca1eb27b5af6c1c92255c7b2217695e7c82e45ad16958737d835`  
		Last Modified: Mon, 07 Oct 2024 17:59:16 GMT  
		Size: 76.2 KB (76249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90f7030ac8134b76c575b67e3efe11890c565b9720b20f884aa39e51379fa8a`  
		Last Modified: Mon, 07 Oct 2024 17:59:16 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcecf4166164b5f91eee2c068c9cf10032384222cf945a98db42f52b6524a306`  
		Last Modified: Mon, 07 Oct 2024 17:59:18 GMT  
		Size: 96.5 MB (96545322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55eb2cc9860c705c47459c162624097ffaa2c7ea7d45788ba015b3a372b1ff04`  
		Last Modified: Mon, 07 Oct 2024 17:59:16 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0537911dadd550e9169d87a8ed784d29c824c6ed899a9e89557b8469f7ad1225`  
		Last Modified: Mon, 07 Oct 2024 17:59:17 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c636312fa8bec76c423e9c0d9ff20fe4700069b29cad3e92cadc651704b70306`  
		Last Modified: Mon, 07 Oct 2024 17:59:17 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f24160517ec536644395bfcf007b9a9f0070102d531f12f6a4fd477c4ea6040`  
		Last Modified: Mon, 07 Oct 2024 17:59:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:471cdaf0bcb8e42aa90d948c32eb06807239ed5cef308b18dba8d9d00c0e0fd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3962411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00dcae559f1c6f8f15554eeadb0c361d6bd18be0e01e302aceae9620b9ff52f9`

```dockerfile
```

-	Layers:
	-	`sha256:11cb481141b35a0178d667dd916b080d4df8afe780ee6ce016bbe21ae838018d`  
		Last Modified: Mon, 07 Oct 2024 17:59:15 GMT  
		Size: 3.9 MB (3930860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50cb49a436060a16d5a8c299e8baf0ae61182ffdc0482073ecd4cb65588243cd`  
		Last Modified: Mon, 07 Oct 2024 17:59:15 GMT  
		Size: 31.6 KB (31551 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:6f7304af9afc8cf0f0bee740d867584e2534bcd365aaba854f6a85d746ce695b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133500332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212fb806a99dd40948d6bbbd4a823fb5cf3329b47232a91cf38d126dfb028eff`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV COUCHDB_VERSION=3.4.1
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/couchdb/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9442d790d6635e0b482db9e87cfb0cac90976dba8b8c97587193528324018d86`  
		Last Modified: Mon, 07 Oct 2024 17:59:12 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdc3f69418039c0518a92ae7aba5811a85e436c9a6eb5122c28aae5b5f11c2e`  
		Last Modified: Mon, 07 Oct 2024 17:59:13 GMT  
		Size: 7.7 MB (7653622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae297c75ee602d28290f293b626460f25e418eee654ce55b3832094ed3b8ad01`  
		Last Modified: Mon, 07 Oct 2024 17:59:12 GMT  
		Size: 348.9 KB (348918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4250e6935cc5320d6b60fcb18f04d395f7da1124ffcf71b4e45e039776e94553`  
		Last Modified: Mon, 07 Oct 2024 17:59:12 GMT  
		Size: 76.2 KB (76249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c412911b39adbd44f52383546496c2af710b6ccca5c9989e0ba373bc50b80e90`  
		Last Modified: Mon, 07 Oct 2024 17:59:13 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd475490e141a14ac69667f3c350fcb6d140936cef9cd3007aa305d77e4cc5f6`  
		Last Modified: Mon, 07 Oct 2024 17:59:16 GMT  
		Size: 96.3 MB (96259732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5baaeef047eea69480cf0707d9e80c07f9a3d1b48f91eaa2ab40c01b1154d6`  
		Last Modified: Mon, 07 Oct 2024 17:59:13 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374a0dd7ca701907840fe7937240a0ef12b8cb0daaf89a1cb2840a377272b8ec`  
		Last Modified: Mon, 07 Oct 2024 17:59:14 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f09a5ca8e0ba7b12c4986347521af7a048b284dfb4bbad8c7f7bcbbc00118e`  
		Last Modified: Mon, 07 Oct 2024 17:59:14 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8552ede7fbb1fb7d79984a5d6f3b386b0e261ad872026f1379e57881d893d42f`  
		Last Modified: Mon, 07 Oct 2024 17:59:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:7b455ba696ae595140ce2d3688b57a4598a900bcc9ae90f74ee05e42d9eddc50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3962957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9186f946aa7677ff5ce63c3755037aa75a3aaae00792b50fc00810fa16c96d23`

```dockerfile
```

-	Layers:
	-	`sha256:801a118eeb4f2f9e15b2a6fc955a4ffb05cf4f24a93952313e4299fea8503d19`  
		Last Modified: Mon, 07 Oct 2024 17:59:12 GMT  
		Size: 3.9 MB (3931152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e2a446b8215c1076b2dbea9b42b9b660a0c1f2effda481e563ed7da921101ed`  
		Last Modified: Mon, 07 Oct 2024 17:59:12 GMT  
		Size: 31.8 KB (31805 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:06bf5736ac28ad74acac4191254d5af4a2b7934c480599422c55286cbe0b84cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86587938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875c9de9dc6617a7e8f91399d2ae3820aaa197d1175eb7efb3c02c49fc4d275e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:301629b0d8ae489e6705aa09fa33dae1617ec0882c0376c2a9b5ec18197190f0 in / 
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
	-	`sha256:ffc4ad031bdde6abf6ae0c4570ad3e4d72f747634c83ee773ce85b5582490bad`  
		Last Modified: Wed, 04 Sep 2024 21:48:09 GMT  
		Size: 29.7 MB (29663447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50a0e61111278bf52f92ec3aba4e8062bbf670bcce16d7a19f968e14031f6a4`  
		Last Modified: Thu, 05 Sep 2024 00:29:56 GMT  
		Size: 3.4 KB (3356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5380a02e92b9d85a22a8565255e5c23c66a332edf530ab8a7c6bbdf11cbb5a`  
		Last Modified: Thu, 05 Sep 2024 00:29:57 GMT  
		Size: 5.1 MB (5109265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ffd63688c6f352b8c1ac59c7c701c828c27496ef91a877ee1f276305799e7a`  
		Last Modified: Thu, 05 Sep 2024 00:29:56 GMT  
		Size: 357.5 KB (357455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9139d63de80e4a5ae92cb9633d4a6cc6582f2d966feae57876758a2eedc78b0`  
		Last Modified: Thu, 05 Sep 2024 00:29:57 GMT  
		Size: 77.8 KB (77819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9751d61e14d141d574b3f9b414116820e82c3d17bedf21e396aa6bb24fd32f63`  
		Last Modified: Thu, 05 Sep 2024 00:29:57 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f852a7a9d2444a087cdde32b42d6cf7e5e45dded57d278ff84d1be9b869fc3`  
		Last Modified: Thu, 05 Sep 2024 00:30:04 GMT  
		Size: 51.4 MB (51372348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f7bfc024286bf1cc40684cb5afdb4839df24e914dabfac0329f7ed9d7834f4`  
		Last Modified: Thu, 05 Sep 2024 00:29:58 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944dad9a9de85d1cf2093ff9fab2258cfdae56e8917f2b4a934e7f15ae76b670`  
		Last Modified: Thu, 05 Sep 2024 00:29:58 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09953c3d45221fb66223af7a494c5e03ad397484906d03dcf825b8ea3698f7ac`  
		Last Modified: Thu, 05 Sep 2024 00:29:58 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b41e11f23832919d76c7e1fe84a5847fd63916bcbb5e25b4512362468252f3e`  
		Last Modified: Thu, 05 Sep 2024 00:29:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:f865f93a9a64a53efb5d294019a7ff8c50d1c7e78f079b706f356fbfd926831b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4031275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca04fbb8335ce31cdc717a038427b236f6532f1ce55f04187964430e9418ae8f`

```dockerfile
```

-	Layers:
	-	`sha256:378b4cbb251408c94cbf0f81f1411eab3e141759047f6b4c29ddba95ed73f77d`  
		Last Modified: Thu, 05 Sep 2024 00:29:56 GMT  
		Size: 4.0 MB (3999663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09e4c7d531739a0ceb270b3f1279adee13234f948c36f749f0da588ea5756f8d`  
		Last Modified: Thu, 05 Sep 2024 00:29:56 GMT  
		Size: 31.6 KB (31612 bytes)  
		MIME: application/vnd.in-toto+json
