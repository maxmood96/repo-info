<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchdb`

-	[`couchdb:3`](#couchdb3)
-	[`couchdb:3-nouveau`](#couchdb3-nouveau)
-	[`couchdb:3.3`](#couchdb33)
-	[`couchdb:3.3.3`](#couchdb333)
-	[`couchdb:3.4`](#couchdb34)
-	[`couchdb:3.4-nouveau`](#couchdb34-nouveau)
-	[`couchdb:3.4.1`](#couchdb341)
-	[`couchdb:3.4.1-nouveau`](#couchdb341-nouveau)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:3`

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

### `couchdb:3` - linux; amd64

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

### `couchdb:3` - unknown; unknown

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

### `couchdb:3` - linux; arm64 variant v8

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

### `couchdb:3` - unknown; unknown

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

### `couchdb:3` - linux; s390x

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

### `couchdb:3` - unknown; unknown

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

## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:dd187ee0c0829bdc3819cef150fe9fcccdec6caf5a03a50ac808bbf09a30a66d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:885df064cb7f9f5892cecfc70fd831cb2f0eb6d0695de7e993581336a5102f38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156247373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a19989cad8dbbdf9b8f56268ec1d0d6de575642c55c3d0916154b5d8c54acab`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/nouveau/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33653f2927b43102562901f4ae62d9d6675e3a7f5d126f98ed040467893010de`  
		Last Modified: Mon, 07 Oct 2024 17:59:25 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e238f481969c183be48d295409e193dd470a7a9e5a4b3a7a4bb5e3e2ffe83e0`  
		Last Modified: Mon, 07 Oct 2024 17:59:25 GMT  
		Size: 7.9 MB (7874377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27bd32a1ff3bb1f6b1b1ccb604692dba9778f6603524d5e9fd9833455e00c2c`  
		Last Modified: Mon, 07 Oct 2024 17:59:27 GMT  
		Size: 77.2 MB (77212242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6a71fdecfbf9da4f94abf241f89775fd26013dc2ef370cae3c1c702ad253bc`  
		Last Modified: Mon, 07 Oct 2024 17:59:25 GMT  
		Size: 414.9 KB (414930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ce06074cf5459e36c5a0906563bbd712a9f77069b2f8b35e41e3fdc365ad51`  
		Last Modified: Mon, 07 Oct 2024 17:59:26 GMT  
		Size: 99.3 KB (99252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6032057b04a40c57bf7970f18fb9f6cb71835caa1ee3838fb16eedbf64992d6`  
		Last Modified: Mon, 07 Oct 2024 17:59:26 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f2840be8ea5b47f7fd71da83efba4c4f8a4a9dcdd901673d014aa4b1af5d14`  
		Last Modified: Mon, 07 Oct 2024 17:59:28 GMT  
		Size: 41.5 MB (41518417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30b4e1ba8dbc907b015bb92f002dbbbf3ca0eb88eeeb198f7301530a4cb8e5f`  
		Last Modified: Mon, 07 Oct 2024 17:59:27 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:e9ce7fbe6ab4a81bfb593226302c7774615de3cb051b1929eb6b974cb1f4c390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3478614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2ffc122b49f3e0eec151cff09a9bc1d5561a8c96144e83a67bfc14379b1e5c`

```dockerfile
```

-	Layers:
	-	`sha256:42b8ed0d4a92a4db59e3fc19647fd427e54b18f39f1529b728dbe8d9c52d6412`  
		Last Modified: Mon, 07 Oct 2024 17:59:25 GMT  
		Size: 3.5 MB (3454275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34b7fcd426ecb7f91ba873d97031a7b24124b4b1fc5a5e066ca2a7625974853b`  
		Last Modified: Mon, 07 Oct 2024 17:59:25 GMT  
		Size: 24.3 KB (24339 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:6cb6aa93c071a1f3d35eddad7dd50bde831a6b69f0e0b3eb25b855da2c5795ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155211011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6720b48cd575172fe484da0a28d6e560e005e57eaedf0d66422fa1f685c424a0`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/nouveau/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0dd4e3ec72ebd08003da9bae2a4f91d7054c7f219464df5c99dff6b44357474`  
		Last Modified: Mon, 07 Oct 2024 18:00:21 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b137a87f378e3c4b496ef8aee954623363575617dc3a5c7483f8c3ad1e6d2f`  
		Last Modified: Mon, 07 Oct 2024 18:00:22 GMT  
		Size: 7.7 MB (7653599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438ad86fea8079ebaffc58a077adcfe370c3ebf5fdcc586a3a436f3fe702b64d`  
		Last Modified: Mon, 07 Oct 2024 18:00:24 GMT  
		Size: 76.5 MB (76508600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3de680e3bb5f4da4aa8fb277abfa4e3f9c789f961838de4afe48155fb5703f`  
		Last Modified: Mon, 07 Oct 2024 18:00:22 GMT  
		Size: 371.7 KB (371699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c47625cd46d9f532742c73d6953d6f24d949e77ca64418792b5f53b862d254`  
		Last Modified: Mon, 07 Oct 2024 18:00:22 GMT  
		Size: 99.2 KB (99217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413d1f9143bb84d6b7c608ee25f6afea8af5874e2ae35e88d5c30d0da7ffe310`  
		Last Modified: Mon, 07 Oct 2024 18:00:23 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d508b85b561fba7d2e644cd77f5b8a05aed8f90a778f04fddd00ffa7253bcd2`  
		Last Modified: Mon, 07 Oct 2024 18:00:25 GMT  
		Size: 41.4 MB (41419645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b28d630547bae5f947878ebecabba5ef9b005b5f9fc3048b4edd72f28b51e9`  
		Last Modified: Mon, 07 Oct 2024 18:00:23 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:f017d58d202848d8c80f74a5bcab5b6764f4e0c5c5051b4ce573865abdc4e42a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3477517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3d3c9e59015ec1d1b521062e7c828ab3abcb3628a8738b55effe9f47eaa5dd`

```dockerfile
```

-	Layers:
	-	`sha256:3a582c389a53f22cadcb0f1e17a3270ec996f89250ca740ea9dd3572660cf229`  
		Last Modified: Mon, 07 Oct 2024 18:00:22 GMT  
		Size: 3.5 MB (3452948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0ab1f52acee1d1347095589a024c76cdb40a50b698e950c8dd8d1cd4a966ebb`  
		Last Modified: Mon, 07 Oct 2024 18:00:21 GMT  
		Size: 24.6 KB (24569 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.3`

```console
$ docker pull couchdb@sha256:10b2956fc011a434562993d1088bd5e2a70b2db2189fe706c50faf0f40d12ce9
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
$ docker pull couchdb@sha256:21c06d69178efc7724e73e7b6313376ef463b0f5bc711ad7594f4f2264cd506b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97624557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e726a0a305477f5bd5993357f484338e02247f0388a327206361948502facd5c`
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
ENV COUCHDB_VERSION=3.3.3
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
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
	-	`sha256:f4312823ca5d674be3626b69b631574f0243c32cfa92fd3616dcf03e50167a9d`  
		Last Modified: Mon, 07 Oct 2024 17:59:17 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d325b8329fdd7f3eaf33a3ebdaf687e3b8ce3260c91e35cb2e01251d9c5220`  
		Last Modified: Mon, 07 Oct 2024 17:59:17 GMT  
		Size: 7.9 MB (7874334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba71a7f4c0610502e55c0abaf4ee99074ca1e4684b847b893886bc27ab58bb3`  
		Last Modified: Mon, 07 Oct 2024 17:59:17 GMT  
		Size: 392.1 KB (392100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1594c3f188544099dc57af233e81d18d834489b9b484a1097df45f7d067bac6c`  
		Last Modified: Mon, 07 Oct 2024 17:59:17 GMT  
		Size: 76.2 KB (76239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe482798f29c61b169f055368665fdb388083f9e6b66a95bee945f78bedee1e`  
		Last Modified: Mon, 07 Oct 2024 17:59:17 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c9565dc7ddd20a54d63d36ce6a7bd71537450974ba645372c1e8213a100f50`  
		Last Modified: Mon, 07 Oct 2024 17:59:18 GMT  
		Size: 60.2 MB (60150175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2a0a7ff53f2f1b46bc4816f81bfc1992c03cfe0dc2487f88d8a11af52e7c01`  
		Last Modified: Mon, 07 Oct 2024 17:59:18 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc0359a0fea1c589b0391cb128e123099ef7be545d3050c49bdfe548a5e0100`  
		Last Modified: Mon, 07 Oct 2024 17:59:18 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cbd64abf7145cdb22b975a0ce78053318096425f961569e86d772bef9ef403e`  
		Last Modified: Mon, 07 Oct 2024 17:59:18 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f397ff66b0d863acf1d58a551f0ccf246913de6135b2366824884081d0ec9941`  
		Last Modified: Mon, 07 Oct 2024 17:59:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:a65ad41312d52e3c657563beb7932ab08e463cde28e3a1d571a8a2a6ca2bf420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3754049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04998b33c6881103f5d2ea0cc84e998eb3ec564583910d6deebcfbeb9d366268`

```dockerfile
```

-	Layers:
	-	`sha256:a2b55eecc5aaf8d222645475848706b70629ca5744f97e7163b6ce2ea43b1e8d`  
		Last Modified: Mon, 07 Oct 2024 17:59:17 GMT  
		Size: 3.7 MB (3723082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:579eae888937e2cc0ac0e3914d41668d6e06cfcc58e5d4fa4c92cccec4b98a01`  
		Last Modified: Mon, 07 Oct 2024 17:59:17 GMT  
		Size: 31.0 KB (30967 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:bfba3256d6594ae3decef473b0d0e7e25496980c3a6cbf49bb6201da039f9da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97174904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2834df946e286bac5bb3e61c8471ad3282188d54935c94e9129a7831124e141`
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
ENV COUCHDB_VERSION=3.3.3
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
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
	-	`sha256:0f035e84dc1280869bf96e6d56d1b44c820b292ea52e02edb891390a01159b0c`  
		Last Modified: Mon, 07 Oct 2024 18:01:13 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53dbaf5123802bd20022593c0a411ca5cc49aaa292ea10fb492d4004dc51a89d`  
		Last Modified: Mon, 07 Oct 2024 18:01:14 GMT  
		Size: 59.9 MB (59934303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9235d516056e5c801c36bc82cf4f764231b499a835357b7b6baba89185324bd1`  
		Last Modified: Mon, 07 Oct 2024 18:01:12 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38d2de30a2b11e03b7863ee0c8d989c844b05ed193688af7a5a4f35c0a8558f`  
		Last Modified: Mon, 07 Oct 2024 18:01:12 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca735c111823e0dc69173ce4a264440acadd3c94a15f16657ee5fd01dae2f22`  
		Last Modified: Mon, 07 Oct 2024 18:01:13 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efdd3b9c1edd642c3cfbb48875d8c17d0c7f3552ae5e897fb41455138d974a4`  
		Last Modified: Mon, 07 Oct 2024 18:01:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:a30ef4cbc9c696c26b7db3263e230f3c1a5a5080f3b82aeb12369c85c9c22c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3754547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a17c79f5ef930a6655202539e34ad785d1e9f7f67fc74fe21972547d15b53e11`

```dockerfile
```

-	Layers:
	-	`sha256:eefac6e18d06e1e3a897f337366bfd3167e5a6ac50c43afae7ec9dd3a8382eba`  
		Last Modified: Mon, 07 Oct 2024 18:01:12 GMT  
		Size: 3.7 MB (3723350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:905f9b4ba2b5c7b97bedf399ab54e99ecbf7e3ee5966e38d918f41c6c895686d`  
		Last Modified: Mon, 07 Oct 2024 18:01:12 GMT  
		Size: 31.2 KB (31197 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:04bff6ceed09e06ac0b30edc8ee238153689f9ffb31176eae6357a2e7f77aee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103912491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf476920a697d99b3ed85392cbc66870cc285c1c9d2e1bb5abefb27a9fbb2af8`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 27 Sep 2024 05:33:07 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
# Fri, 27 Sep 2024 05:33:08 GMT
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
ENV COUCHDB_VERSION=3.3.3
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
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
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41698c9fbcff28a77380d6b33b4c23081ea6f07b1b5125bf8326e814066b0d1`  
		Last Modified: Mon, 07 Oct 2024 18:00:09 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488ca9e9df03960d4a7c7726ecbeb2bd6a9e9a7526b3dcd8269c277db4d6835b`  
		Last Modified: Mon, 07 Oct 2024 18:00:10 GMT  
		Size: 8.9 MB (8889106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b18341bfbcf911e9404b817f237a867bcee2a3f0b25343d4cf496393102aa0`  
		Last Modified: Mon, 07 Oct 2024 18:00:10 GMT  
		Size: 444.6 KB (444630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc8c045086e7d18a739dd758b5c6fe8833ac133bbc71b98d0f1ba6fa33dca0d`  
		Last Modified: Mon, 07 Oct 2024 18:00:09 GMT  
		Size: 76.3 KB (76252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3842e7092ea67b8f9149bed6094f2775c2cddfdaf1e124e3d9ce8076e3d981c6`  
		Last Modified: Mon, 07 Oct 2024 18:00:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24fc4e6ceb73ba1bcb4700d032901ab945ee077eed25608513bc5085e4ca0187`  
		Last Modified: Mon, 07 Oct 2024 18:00:15 GMT  
		Size: 61.4 MB (61374904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a55281672e703fb64d5e50bfa5743e7d738697da78268449926293a3c65ceec`  
		Last Modified: Mon, 07 Oct 2024 18:00:11 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f393efab50cfcaedffffab3d2c7e639c3e923947b9a37c3375e50ab64004a01a`  
		Last Modified: Mon, 07 Oct 2024 18:00:11 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae082e12b73df448b4c5fa34fc4232a7028ce7bd30ff10b85b1e93beab8317d1`  
		Last Modified: Mon, 07 Oct 2024 18:00:12 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7a2b1687e3a8e5c3154903e8805e70599e7b010f6c1f3c9a056c21f1c38577`  
		Last Modified: Mon, 07 Oct 2024 18:00:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:c3b544ff91da0c3901092e28f834e00f9e4019e73552889eeada4694eaed3a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3758656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2ef65c417f6dac4a0ffd6ed15d474069e8bac78f03708440d29d9de2d66035a`

```dockerfile
```

-	Layers:
	-	`sha256:98fe2be65cbfa970f28b082afcdeadb48df5f780af0c331e4a42e503836111f3`  
		Last Modified: Mon, 07 Oct 2024 18:00:10 GMT  
		Size: 3.7 MB (3727585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcff7f9e334ad90ec29f88b4fbe91fc18e524d4f9b7efca6e92a39b57b6aad10`  
		Last Modified: Mon, 07 Oct 2024 18:00:09 GMT  
		Size: 31.1 KB (31071 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; s390x

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

### `couchdb:3.3` - unknown; unknown

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

## `couchdb:3.3.3`

```console
$ docker pull couchdb@sha256:10b2956fc011a434562993d1088bd5e2a70b2db2189fe706c50faf0f40d12ce9
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
$ docker pull couchdb@sha256:21c06d69178efc7724e73e7b6313376ef463b0f5bc711ad7594f4f2264cd506b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97624557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e726a0a305477f5bd5993357f484338e02247f0388a327206361948502facd5c`
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
ENV COUCHDB_VERSION=3.3.3
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
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
	-	`sha256:f4312823ca5d674be3626b69b631574f0243c32cfa92fd3616dcf03e50167a9d`  
		Last Modified: Mon, 07 Oct 2024 17:59:17 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d325b8329fdd7f3eaf33a3ebdaf687e3b8ce3260c91e35cb2e01251d9c5220`  
		Last Modified: Mon, 07 Oct 2024 17:59:17 GMT  
		Size: 7.9 MB (7874334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba71a7f4c0610502e55c0abaf4ee99074ca1e4684b847b893886bc27ab58bb3`  
		Last Modified: Mon, 07 Oct 2024 17:59:17 GMT  
		Size: 392.1 KB (392100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1594c3f188544099dc57af233e81d18d834489b9b484a1097df45f7d067bac6c`  
		Last Modified: Mon, 07 Oct 2024 17:59:17 GMT  
		Size: 76.2 KB (76239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe482798f29c61b169f055368665fdb388083f9e6b66a95bee945f78bedee1e`  
		Last Modified: Mon, 07 Oct 2024 17:59:17 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c9565dc7ddd20a54d63d36ce6a7bd71537450974ba645372c1e8213a100f50`  
		Last Modified: Mon, 07 Oct 2024 17:59:18 GMT  
		Size: 60.2 MB (60150175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2a0a7ff53f2f1b46bc4816f81bfc1992c03cfe0dc2487f88d8a11af52e7c01`  
		Last Modified: Mon, 07 Oct 2024 17:59:18 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc0359a0fea1c589b0391cb128e123099ef7be545d3050c49bdfe548a5e0100`  
		Last Modified: Mon, 07 Oct 2024 17:59:18 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cbd64abf7145cdb22b975a0ce78053318096425f961569e86d772bef9ef403e`  
		Last Modified: Mon, 07 Oct 2024 17:59:18 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f397ff66b0d863acf1d58a551f0ccf246913de6135b2366824884081d0ec9941`  
		Last Modified: Mon, 07 Oct 2024 17:59:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:a65ad41312d52e3c657563beb7932ab08e463cde28e3a1d571a8a2a6ca2bf420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3754049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04998b33c6881103f5d2ea0cc84e998eb3ec564583910d6deebcfbeb9d366268`

```dockerfile
```

-	Layers:
	-	`sha256:a2b55eecc5aaf8d222645475848706b70629ca5744f97e7163b6ce2ea43b1e8d`  
		Last Modified: Mon, 07 Oct 2024 17:59:17 GMT  
		Size: 3.7 MB (3723082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:579eae888937e2cc0ac0e3914d41668d6e06cfcc58e5d4fa4c92cccec4b98a01`  
		Last Modified: Mon, 07 Oct 2024 17:59:17 GMT  
		Size: 31.0 KB (30967 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:bfba3256d6594ae3decef473b0d0e7e25496980c3a6cbf49bb6201da039f9da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97174904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2834df946e286bac5bb3e61c8471ad3282188d54935c94e9129a7831124e141`
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
ENV COUCHDB_VERSION=3.3.3
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
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
	-	`sha256:0f035e84dc1280869bf96e6d56d1b44c820b292ea52e02edb891390a01159b0c`  
		Last Modified: Mon, 07 Oct 2024 18:01:13 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53dbaf5123802bd20022593c0a411ca5cc49aaa292ea10fb492d4004dc51a89d`  
		Last Modified: Mon, 07 Oct 2024 18:01:14 GMT  
		Size: 59.9 MB (59934303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9235d516056e5c801c36bc82cf4f764231b499a835357b7b6baba89185324bd1`  
		Last Modified: Mon, 07 Oct 2024 18:01:12 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38d2de30a2b11e03b7863ee0c8d989c844b05ed193688af7a5a4f35c0a8558f`  
		Last Modified: Mon, 07 Oct 2024 18:01:12 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca735c111823e0dc69173ce4a264440acadd3c94a15f16657ee5fd01dae2f22`  
		Last Modified: Mon, 07 Oct 2024 18:01:13 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efdd3b9c1edd642c3cfbb48875d8c17d0c7f3552ae5e897fb41455138d974a4`  
		Last Modified: Mon, 07 Oct 2024 18:01:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:a30ef4cbc9c696c26b7db3263e230f3c1a5a5080f3b82aeb12369c85c9c22c9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3754547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a17c79f5ef930a6655202539e34ad785d1e9f7f67fc74fe21972547d15b53e11`

```dockerfile
```

-	Layers:
	-	`sha256:eefac6e18d06e1e3a897f337366bfd3167e5a6ac50c43afae7ec9dd3a8382eba`  
		Last Modified: Mon, 07 Oct 2024 18:01:12 GMT  
		Size: 3.7 MB (3723350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:905f9b4ba2b5c7b97bedf399ab54e99ecbf7e3ee5966e38d918f41c6c895686d`  
		Last Modified: Mon, 07 Oct 2024 18:01:12 GMT  
		Size: 31.2 KB (31197 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:04bff6ceed09e06ac0b30edc8ee238153689f9ffb31176eae6357a2e7f77aee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103912491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf476920a697d99b3ed85392cbc66870cc285c1c9d2e1bb5abefb27a9fbb2af8`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Fri, 27 Sep 2024 05:33:07 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
# Fri, 27 Sep 2024 05:33:08 GMT
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
ENV COUCHDB_VERSION=3.3.3
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
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
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41698c9fbcff28a77380d6b33b4c23081ea6f07b1b5125bf8326e814066b0d1`  
		Last Modified: Mon, 07 Oct 2024 18:00:09 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488ca9e9df03960d4a7c7726ecbeb2bd6a9e9a7526b3dcd8269c277db4d6835b`  
		Last Modified: Mon, 07 Oct 2024 18:00:10 GMT  
		Size: 8.9 MB (8889106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b18341bfbcf911e9404b817f237a867bcee2a3f0b25343d4cf496393102aa0`  
		Last Modified: Mon, 07 Oct 2024 18:00:10 GMT  
		Size: 444.6 KB (444630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc8c045086e7d18a739dd758b5c6fe8833ac133bbc71b98d0f1ba6fa33dca0d`  
		Last Modified: Mon, 07 Oct 2024 18:00:09 GMT  
		Size: 76.3 KB (76252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3842e7092ea67b8f9149bed6094f2775c2cddfdaf1e124e3d9ce8076e3d981c6`  
		Last Modified: Mon, 07 Oct 2024 18:00:11 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24fc4e6ceb73ba1bcb4700d032901ab945ee077eed25608513bc5085e4ca0187`  
		Last Modified: Mon, 07 Oct 2024 18:00:15 GMT  
		Size: 61.4 MB (61374904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a55281672e703fb64d5e50bfa5743e7d738697da78268449926293a3c65ceec`  
		Last Modified: Mon, 07 Oct 2024 18:00:11 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f393efab50cfcaedffffab3d2c7e639c3e923947b9a37c3375e50ab64004a01a`  
		Last Modified: Mon, 07 Oct 2024 18:00:11 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae082e12b73df448b4c5fa34fc4232a7028ce7bd30ff10b85b1e93beab8317d1`  
		Last Modified: Mon, 07 Oct 2024 18:00:12 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7a2b1687e3a8e5c3154903e8805e70599e7b010f6c1f3c9a056c21f1c38577`  
		Last Modified: Mon, 07 Oct 2024 18:00:12 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:c3b544ff91da0c3901092e28f834e00f9e4019e73552889eeada4694eaed3a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3758656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2ef65c417f6dac4a0ffd6ed15d474069e8bac78f03708440d29d9de2d66035a`

```dockerfile
```

-	Layers:
	-	`sha256:98fe2be65cbfa970f28b082afcdeadb48df5f780af0c331e4a42e503836111f3`  
		Last Modified: Mon, 07 Oct 2024 18:00:10 GMT  
		Size: 3.7 MB (3727585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcff7f9e334ad90ec29f88b4fbe91fc18e524d4f9b7efca6e92a39b57b6aad10`  
		Last Modified: Mon, 07 Oct 2024 18:00:09 GMT  
		Size: 31.1 KB (31071 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; s390x

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

### `couchdb:3.3.3` - unknown; unknown

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

## `couchdb:3.4`

```console
$ docker pull couchdb@sha256:1658ba10df69f3a6d16a33e2459e8c0ef5627a6faaf6d86f26992fbdf5f7e06e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.4` - linux; amd64

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

### `couchdb:3.4` - unknown; unknown

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

### `couchdb:3.4` - linux; arm64 variant v8

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

### `couchdb:3.4` - unknown; unknown

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

## `couchdb:3.4-nouveau`

```console
$ docker pull couchdb@sha256:dd187ee0c0829bdc3819cef150fe9fcccdec6caf5a03a50ac808bbf09a30a66d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.4-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:885df064cb7f9f5892cecfc70fd831cb2f0eb6d0695de7e993581336a5102f38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156247373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a19989cad8dbbdf9b8f56268ec1d0d6de575642c55c3d0916154b5d8c54acab`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/nouveau/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33653f2927b43102562901f4ae62d9d6675e3a7f5d126f98ed040467893010de`  
		Last Modified: Mon, 07 Oct 2024 17:59:25 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e238f481969c183be48d295409e193dd470a7a9e5a4b3a7a4bb5e3e2ffe83e0`  
		Last Modified: Mon, 07 Oct 2024 17:59:25 GMT  
		Size: 7.9 MB (7874377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27bd32a1ff3bb1f6b1b1ccb604692dba9778f6603524d5e9fd9833455e00c2c`  
		Last Modified: Mon, 07 Oct 2024 17:59:27 GMT  
		Size: 77.2 MB (77212242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6a71fdecfbf9da4f94abf241f89775fd26013dc2ef370cae3c1c702ad253bc`  
		Last Modified: Mon, 07 Oct 2024 17:59:25 GMT  
		Size: 414.9 KB (414930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ce06074cf5459e36c5a0906563bbd712a9f77069b2f8b35e41e3fdc365ad51`  
		Last Modified: Mon, 07 Oct 2024 17:59:26 GMT  
		Size: 99.3 KB (99252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6032057b04a40c57bf7970f18fb9f6cb71835caa1ee3838fb16eedbf64992d6`  
		Last Modified: Mon, 07 Oct 2024 17:59:26 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f2840be8ea5b47f7fd71da83efba4c4f8a4a9dcdd901673d014aa4b1af5d14`  
		Last Modified: Mon, 07 Oct 2024 17:59:28 GMT  
		Size: 41.5 MB (41518417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30b4e1ba8dbc907b015bb92f002dbbbf3ca0eb88eeeb198f7301530a4cb8e5f`  
		Last Modified: Mon, 07 Oct 2024 17:59:27 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:e9ce7fbe6ab4a81bfb593226302c7774615de3cb051b1929eb6b974cb1f4c390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3478614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2ffc122b49f3e0eec151cff09a9bc1d5561a8c96144e83a67bfc14379b1e5c`

```dockerfile
```

-	Layers:
	-	`sha256:42b8ed0d4a92a4db59e3fc19647fd427e54b18f39f1529b728dbe8d9c52d6412`  
		Last Modified: Mon, 07 Oct 2024 17:59:25 GMT  
		Size: 3.5 MB (3454275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34b7fcd426ecb7f91ba873d97031a7b24124b4b1fc5a5e066ca2a7625974853b`  
		Last Modified: Mon, 07 Oct 2024 17:59:25 GMT  
		Size: 24.3 KB (24339 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:6cb6aa93c071a1f3d35eddad7dd50bde831a6b69f0e0b3eb25b855da2c5795ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155211011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6720b48cd575172fe484da0a28d6e560e005e57eaedf0d66422fa1f685c424a0`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/nouveau/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0dd4e3ec72ebd08003da9bae2a4f91d7054c7f219464df5c99dff6b44357474`  
		Last Modified: Mon, 07 Oct 2024 18:00:21 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b137a87f378e3c4b496ef8aee954623363575617dc3a5c7483f8c3ad1e6d2f`  
		Last Modified: Mon, 07 Oct 2024 18:00:22 GMT  
		Size: 7.7 MB (7653599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438ad86fea8079ebaffc58a077adcfe370c3ebf5fdcc586a3a436f3fe702b64d`  
		Last Modified: Mon, 07 Oct 2024 18:00:24 GMT  
		Size: 76.5 MB (76508600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3de680e3bb5f4da4aa8fb277abfa4e3f9c789f961838de4afe48155fb5703f`  
		Last Modified: Mon, 07 Oct 2024 18:00:22 GMT  
		Size: 371.7 KB (371699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c47625cd46d9f532742c73d6953d6f24d949e77ca64418792b5f53b862d254`  
		Last Modified: Mon, 07 Oct 2024 18:00:22 GMT  
		Size: 99.2 KB (99217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413d1f9143bb84d6b7c608ee25f6afea8af5874e2ae35e88d5c30d0da7ffe310`  
		Last Modified: Mon, 07 Oct 2024 18:00:23 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d508b85b561fba7d2e644cd77f5b8a05aed8f90a778f04fddd00ffa7253bcd2`  
		Last Modified: Mon, 07 Oct 2024 18:00:25 GMT  
		Size: 41.4 MB (41419645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b28d630547bae5f947878ebecabba5ef9b005b5f9fc3048b4edd72f28b51e9`  
		Last Modified: Mon, 07 Oct 2024 18:00:23 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:f017d58d202848d8c80f74a5bcab5b6764f4e0c5c5051b4ce573865abdc4e42a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3477517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3d3c9e59015ec1d1b521062e7c828ab3abcb3628a8738b55effe9f47eaa5dd`

```dockerfile
```

-	Layers:
	-	`sha256:3a582c389a53f22cadcb0f1e17a3270ec996f89250ca740ea9dd3572660cf229`  
		Last Modified: Mon, 07 Oct 2024 18:00:22 GMT  
		Size: 3.5 MB (3452948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0ab1f52acee1d1347095589a024c76cdb40a50b698e950c8dd8d1cd4a966ebb`  
		Last Modified: Mon, 07 Oct 2024 18:00:21 GMT  
		Size: 24.6 KB (24569 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.1`

```console
$ docker pull couchdb@sha256:1658ba10df69f3a6d16a33e2459e8c0ef5627a6faaf6d86f26992fbdf5f7e06e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.4.1` - linux; amd64

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

### `couchdb:3.4.1` - unknown; unknown

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

### `couchdb:3.4.1` - linux; arm64 variant v8

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

### `couchdb:3.4.1` - unknown; unknown

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

## `couchdb:3.4.1-nouveau`

```console
$ docker pull couchdb@sha256:dd187ee0c0829bdc3819cef150fe9fcccdec6caf5a03a50ac808bbf09a30a66d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.4.1-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:885df064cb7f9f5892cecfc70fd831cb2f0eb6d0695de7e993581336a5102f38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156247373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a19989cad8dbbdf9b8f56268ec1d0d6de575642c55c3d0916154b5d8c54acab`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/nouveau/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33653f2927b43102562901f4ae62d9d6675e3a7f5d126f98ed040467893010de`  
		Last Modified: Mon, 07 Oct 2024 17:59:25 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e238f481969c183be48d295409e193dd470a7a9e5a4b3a7a4bb5e3e2ffe83e0`  
		Last Modified: Mon, 07 Oct 2024 17:59:25 GMT  
		Size: 7.9 MB (7874377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27bd32a1ff3bb1f6b1b1ccb604692dba9778f6603524d5e9fd9833455e00c2c`  
		Last Modified: Mon, 07 Oct 2024 17:59:27 GMT  
		Size: 77.2 MB (77212242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6a71fdecfbf9da4f94abf241f89775fd26013dc2ef370cae3c1c702ad253bc`  
		Last Modified: Mon, 07 Oct 2024 17:59:25 GMT  
		Size: 414.9 KB (414930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ce06074cf5459e36c5a0906563bbd712a9f77069b2f8b35e41e3fdc365ad51`  
		Last Modified: Mon, 07 Oct 2024 17:59:26 GMT  
		Size: 99.3 KB (99252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6032057b04a40c57bf7970f18fb9f6cb71835caa1ee3838fb16eedbf64992d6`  
		Last Modified: Mon, 07 Oct 2024 17:59:26 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f2840be8ea5b47f7fd71da83efba4c4f8a4a9dcdd901673d014aa4b1af5d14`  
		Last Modified: Mon, 07 Oct 2024 17:59:28 GMT  
		Size: 41.5 MB (41518417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30b4e1ba8dbc907b015bb92f002dbbbf3ca0eb88eeeb198f7301530a4cb8e5f`  
		Last Modified: Mon, 07 Oct 2024 17:59:27 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:e9ce7fbe6ab4a81bfb593226302c7774615de3cb051b1929eb6b974cb1f4c390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3478614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2ffc122b49f3e0eec151cff09a9bc1d5561a8c96144e83a67bfc14379b1e5c`

```dockerfile
```

-	Layers:
	-	`sha256:42b8ed0d4a92a4db59e3fc19647fd427e54b18f39f1529b728dbe8d9c52d6412`  
		Last Modified: Mon, 07 Oct 2024 17:59:25 GMT  
		Size: 3.5 MB (3454275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34b7fcd426ecb7f91ba873d97031a7b24124b4b1fc5a5e066ca2a7625974853b`  
		Last Modified: Mon, 07 Oct 2024 17:59:25 GMT  
		Size: 24.3 KB (24339 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.1-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:6cb6aa93c071a1f3d35eddad7dd50bde831a6b69f0e0b3eb25b855da2c5795ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.2 MB (155211011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6720b48cd575172fe484da0a28d6e560e005e57eaedf0d66422fa1f685c424a0`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Fri, 04 Oct 2024 23:09:59 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Fri, 04 Oct 2024 23:09:59 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Fri, 04 Oct 2024 23:09:59 GMT
VOLUME [/opt/nouveau/data]
# Fri, 04 Oct 2024 23:09:59 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Fri, 04 Oct 2024 23:09:59 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0dd4e3ec72ebd08003da9bae2a4f91d7054c7f219464df5c99dff6b44357474`  
		Last Modified: Mon, 07 Oct 2024 18:00:21 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b137a87f378e3c4b496ef8aee954623363575617dc3a5c7483f8c3ad1e6d2f`  
		Last Modified: Mon, 07 Oct 2024 18:00:22 GMT  
		Size: 7.7 MB (7653599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438ad86fea8079ebaffc58a077adcfe370c3ebf5fdcc586a3a436f3fe702b64d`  
		Last Modified: Mon, 07 Oct 2024 18:00:24 GMT  
		Size: 76.5 MB (76508600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3de680e3bb5f4da4aa8fb277abfa4e3f9c789f961838de4afe48155fb5703f`  
		Last Modified: Mon, 07 Oct 2024 18:00:22 GMT  
		Size: 371.7 KB (371699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c47625cd46d9f532742c73d6953d6f24d949e77ca64418792b5f53b862d254`  
		Last Modified: Mon, 07 Oct 2024 18:00:22 GMT  
		Size: 99.2 KB (99217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413d1f9143bb84d6b7c608ee25f6afea8af5874e2ae35e88d5c30d0da7ffe310`  
		Last Modified: Mon, 07 Oct 2024 18:00:23 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d508b85b561fba7d2e644cd77f5b8a05aed8f90a778f04fddd00ffa7253bcd2`  
		Last Modified: Mon, 07 Oct 2024 18:00:25 GMT  
		Size: 41.4 MB (41419645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b28d630547bae5f947878ebecabba5ef9b005b5f9fc3048b4edd72f28b51e9`  
		Last Modified: Mon, 07 Oct 2024 18:00:23 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:f017d58d202848d8c80f74a5bcab5b6764f4e0c5c5051b4ce573865abdc4e42a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3477517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f3d3c9e59015ec1d1b521062e7c828ab3abcb3628a8738b55effe9f47eaa5dd`

```dockerfile
```

-	Layers:
	-	`sha256:3a582c389a53f22cadcb0f1e17a3270ec996f89250ca740ea9dd3572660cf229`  
		Last Modified: Mon, 07 Oct 2024 18:00:22 GMT  
		Size: 3.5 MB (3452948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0ab1f52acee1d1347095589a024c76cdb40a50b698e950c8dd8d1cd4a966ebb`  
		Last Modified: Mon, 07 Oct 2024 18:00:21 GMT  
		Size: 24.6 KB (24569 bytes)  
		MIME: application/vnd.in-toto+json

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
