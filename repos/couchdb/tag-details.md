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
$ docker pull couchdb@sha256:ddfb19f4790a031d6ec710b47c8ca87e3c7196d86bd72a6df49f915f6fc42688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:19be5733a588e013e2c291d4859912263be55b51ccf536eb1bd7bc1d43c1ae57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84601725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ee8e9e2374fc1d5a8f7e6ace34246c2ce60e99b8566c0d1ce0f9d307c41b83`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:33 GMT
ADD file:29d3eb64d192a97184f2aa169407b58e969b06268c6372b49eefb72bcadb6e99 in / 
# Wed, 01 Nov 2023 00:21:34 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:47:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 01 Nov 2023 01:47:36 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 01 Nov 2023 01:47:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:47:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 01 Nov 2023 01:47:47 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 01 Nov 2023 01:47:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:48:16 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 01 Nov 2023 01:48:17 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 01 Nov 2023 01:48:34 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 01 Nov 2023 01:48:35 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 01 Nov 2023 01:48:35 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 01 Nov 2023 01:48:35 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 01 Nov 2023 01:48:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 01 Nov 2023 01:48:36 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 01 Nov 2023 01:48:36 GMT
VOLUME [/opt/couchdb/data]
# Wed, 01 Nov 2023 01:48:36 GMT
EXPOSE 4369 5984 9100
# Wed, 01 Nov 2023 01:48:36 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:113c6ad4754853f4a2ae632cff7d90eba9145cca0bd6fa4d60aa432bd26be6c7`  
		Last Modified: Wed, 01 Nov 2023 00:26:56 GMT  
		Size: 27.2 MB (27187422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365ea17356912d8ab65ea5e3a1e839d36823f7303a6f99fec14eb169f5a4f2e1`  
		Last Modified: Wed, 01 Nov 2023 01:49:33 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2706b6ad14bfc13aa94a94269c8479e367a22ebbf64f230b4a133b8198b51523`  
		Last Modified: Wed, 01 Nov 2023 01:49:32 GMT  
		Size: 6.7 MB (6704557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3cbd037256b0218774d56e4d3151275a32733815758ef37784eae1b624c9831`  
		Last Modified: Wed, 01 Nov 2023 01:49:31 GMT  
		Size: 1.3 MB (1259891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7bc073931afdef902766bdbf4440108b63b7e7a8afc61c51d5132e2b366910`  
		Last Modified: Wed, 01 Nov 2023 01:49:31 GMT  
		Size: 294.5 KB (294533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b65f0118e1821e295770007c76deb6fe634a42524867a48e15ec8f7a13ae28`  
		Last Modified: Wed, 01 Nov 2023 01:49:45 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba2feaa281f86c66f6d3385abb0a3c253bb921c23c2fb5b7f037c54dfd0e9fc`  
		Last Modified: Wed, 01 Nov 2023 01:49:48 GMT  
		Size: 49.1 MB (49148308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60a8b754ebf89dcda4a9b032fc7d76cfaf67b4d1cdd88a92fd548bfdde80785`  
		Last Modified: Wed, 01 Nov 2023 01:49:43 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199951c325e2234c69de9082ae7590bd8eeb37f76ccf34d718f5393cdbe10f76`  
		Last Modified: Wed, 01 Nov 2023 01:49:43 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f41fd1ccaf8d2e0c1c37dc2a8a78d3d6ebe9650c37c188cc04833e726242a4a`  
		Last Modified: Wed, 01 Nov 2023 01:49:43 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ad5245583de27094c466123980bca3addac07d4fc43887ea3f7598abcec934`  
		Last Modified: Wed, 01 Nov 2023 01:49:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:f6c2eb09ebaa599f0a93c7f28e5f47185121416af39120dd80ee27ae42e90a63
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73042770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ab83c5db3e862a9904f8a1d3e4821e2ab1d2eb563d33313ac79316b544b348`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:34 GMT
ADD file:475e94b9a8f65c7cd4d4156af31e83190240ff35d8038f3fa86ad124d4d5d299 in / 
# Tue, 21 Nov 2023 06:27:35 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:53:23 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 21 Nov 2023 07:53:24 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 21 Nov 2023 07:53:33 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:53:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 21 Nov 2023 07:53:37 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 21 Nov 2023 07:53:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:54:03 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 21 Nov 2023 07:54:04 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 21 Nov 2023 07:54:15 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 21 Nov 2023 07:54:16 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 21 Nov 2023 07:54:16 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 21 Nov 2023 07:54:16 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 21 Nov 2023 07:54:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 21 Nov 2023 07:54:16 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 07:54:16 GMT
VOLUME [/opt/couchdb/data]
# Tue, 21 Nov 2023 07:54:17 GMT
EXPOSE 4369 5984 9100
# Tue, 21 Nov 2023 07:54:17 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:78b429e3efdd9f2b163abf0bca6b1462a25b1c5eddc1dd47f5d3445c6413cfa1`  
		Last Modified: Tue, 21 Nov 2023 06:31:45 GMT  
		Size: 26.0 MB (25967796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3c5bfaccf97ef74c924764aca27d055d3cab8446f6ef59870cd544056d4cec`  
		Last Modified: Tue, 21 Nov 2023 07:54:50 GMT  
		Size: 3.4 KB (3434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff6bf33f9c2e30b4f1ce3f1bf6149231315457866fad15eedffdf007ad01f5e`  
		Last Modified: Tue, 21 Nov 2023 07:54:49 GMT  
		Size: 6.6 MB (6577624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0040bf5cab2106c8e662145f7f764673fdd1f2b1ea63a2f64a94333049636031`  
		Last Modified: Tue, 21 Nov 2023 07:54:48 GMT  
		Size: 1.2 MB (1164833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f6ff98dded5f418fecd217598fdeb4a722749c105e50a53dce349adc0872191`  
		Last Modified: Tue, 21 Nov 2023 07:54:48 GMT  
		Size: 294.4 KB (294403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b62b412c39c27d6b0bb77c29580f219e6832aa220a1ed8f0e2bb8ac5e792a8c`  
		Last Modified: Tue, 21 Nov 2023 07:55:00 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb05dfa0bb3aaeb852e7044d0f340c9f2ab0670711209b60bcd59af90662d446`  
		Last Modified: Tue, 21 Nov 2023 07:55:01 GMT  
		Size: 39.0 MB (39031078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b0733c721e2ac151b2a04aa4474c02909229c16794206a817831aaf359c3586`  
		Last Modified: Tue, 21 Nov 2023 07:54:58 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898bac72b3df0026173253ea7ec67fdf05a7b81e4b1b35117bbefeeb74161be3`  
		Last Modified: Tue, 21 Nov 2023 07:54:58 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df6dfa461e8b59dabcba0ba599e8cf4ac4467d94a12592cfac6025ae0656cb7`  
		Last Modified: Tue, 21 Nov 2023 07:54:58 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d16e9798ed2dcc347e66efbb5cc6cb53f4a73440518bf6a3c0adad2ee71cfd`  
		Last Modified: Tue, 21 Nov 2023 07:54:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:ddfb19f4790a031d6ec710b47c8ca87e3c7196d86bd72a6df49f915f6fc42688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:19be5733a588e013e2c291d4859912263be55b51ccf536eb1bd7bc1d43c1ae57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84601725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ee8e9e2374fc1d5a8f7e6ace34246c2ce60e99b8566c0d1ce0f9d307c41b83`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:33 GMT
ADD file:29d3eb64d192a97184f2aa169407b58e969b06268c6372b49eefb72bcadb6e99 in / 
# Wed, 01 Nov 2023 00:21:34 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:47:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 01 Nov 2023 01:47:36 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 01 Nov 2023 01:47:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:47:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 01 Nov 2023 01:47:47 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 01 Nov 2023 01:47:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:48:16 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 01 Nov 2023 01:48:17 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 01 Nov 2023 01:48:34 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 01 Nov 2023 01:48:35 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 01 Nov 2023 01:48:35 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 01 Nov 2023 01:48:35 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 01 Nov 2023 01:48:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 01 Nov 2023 01:48:36 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 01 Nov 2023 01:48:36 GMT
VOLUME [/opt/couchdb/data]
# Wed, 01 Nov 2023 01:48:36 GMT
EXPOSE 4369 5984 9100
# Wed, 01 Nov 2023 01:48:36 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:113c6ad4754853f4a2ae632cff7d90eba9145cca0bd6fa4d60aa432bd26be6c7`  
		Last Modified: Wed, 01 Nov 2023 00:26:56 GMT  
		Size: 27.2 MB (27187422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365ea17356912d8ab65ea5e3a1e839d36823f7303a6f99fec14eb169f5a4f2e1`  
		Last Modified: Wed, 01 Nov 2023 01:49:33 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2706b6ad14bfc13aa94a94269c8479e367a22ebbf64f230b4a133b8198b51523`  
		Last Modified: Wed, 01 Nov 2023 01:49:32 GMT  
		Size: 6.7 MB (6704557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3cbd037256b0218774d56e4d3151275a32733815758ef37784eae1b624c9831`  
		Last Modified: Wed, 01 Nov 2023 01:49:31 GMT  
		Size: 1.3 MB (1259891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7bc073931afdef902766bdbf4440108b63b7e7a8afc61c51d5132e2b366910`  
		Last Modified: Wed, 01 Nov 2023 01:49:31 GMT  
		Size: 294.5 KB (294533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b65f0118e1821e295770007c76deb6fe634a42524867a48e15ec8f7a13ae28`  
		Last Modified: Wed, 01 Nov 2023 01:49:45 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba2feaa281f86c66f6d3385abb0a3c253bb921c23c2fb5b7f037c54dfd0e9fc`  
		Last Modified: Wed, 01 Nov 2023 01:49:48 GMT  
		Size: 49.1 MB (49148308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60a8b754ebf89dcda4a9b032fc7d76cfaf67b4d1cdd88a92fd548bfdde80785`  
		Last Modified: Wed, 01 Nov 2023 01:49:43 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199951c325e2234c69de9082ae7590bd8eeb37f76ccf34d718f5393cdbe10f76`  
		Last Modified: Wed, 01 Nov 2023 01:49:43 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f41fd1ccaf8d2e0c1c37dc2a8a78d3d6ebe9650c37c188cc04833e726242a4a`  
		Last Modified: Wed, 01 Nov 2023 01:49:43 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ad5245583de27094c466123980bca3addac07d4fc43887ea3f7598abcec934`  
		Last Modified: Wed, 01 Nov 2023 01:49:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:f6c2eb09ebaa599f0a93c7f28e5f47185121416af39120dd80ee27ae42e90a63
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73042770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ab83c5db3e862a9904f8a1d3e4821e2ab1d2eb563d33313ac79316b544b348`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:34 GMT
ADD file:475e94b9a8f65c7cd4d4156af31e83190240ff35d8038f3fa86ad124d4d5d299 in / 
# Tue, 21 Nov 2023 06:27:35 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:53:23 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 21 Nov 2023 07:53:24 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 21 Nov 2023 07:53:33 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:53:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 21 Nov 2023 07:53:37 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 21 Nov 2023 07:53:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:54:03 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 21 Nov 2023 07:54:04 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 21 Nov 2023 07:54:15 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 21 Nov 2023 07:54:16 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 21 Nov 2023 07:54:16 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 21 Nov 2023 07:54:16 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 21 Nov 2023 07:54:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 21 Nov 2023 07:54:16 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 07:54:16 GMT
VOLUME [/opt/couchdb/data]
# Tue, 21 Nov 2023 07:54:17 GMT
EXPOSE 4369 5984 9100
# Tue, 21 Nov 2023 07:54:17 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:78b429e3efdd9f2b163abf0bca6b1462a25b1c5eddc1dd47f5d3445c6413cfa1`  
		Last Modified: Tue, 21 Nov 2023 06:31:45 GMT  
		Size: 26.0 MB (25967796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3c5bfaccf97ef74c924764aca27d055d3cab8446f6ef59870cd544056d4cec`  
		Last Modified: Tue, 21 Nov 2023 07:54:50 GMT  
		Size: 3.4 KB (3434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff6bf33f9c2e30b4f1ce3f1bf6149231315457866fad15eedffdf007ad01f5e`  
		Last Modified: Tue, 21 Nov 2023 07:54:49 GMT  
		Size: 6.6 MB (6577624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0040bf5cab2106c8e662145f7f764673fdd1f2b1ea63a2f64a94333049636031`  
		Last Modified: Tue, 21 Nov 2023 07:54:48 GMT  
		Size: 1.2 MB (1164833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f6ff98dded5f418fecd217598fdeb4a722749c105e50a53dce349adc0872191`  
		Last Modified: Tue, 21 Nov 2023 07:54:48 GMT  
		Size: 294.4 KB (294403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b62b412c39c27d6b0bb77c29580f219e6832aa220a1ed8f0e2bb8ac5e792a8c`  
		Last Modified: Tue, 21 Nov 2023 07:55:00 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb05dfa0bb3aaeb852e7044d0f340c9f2ab0670711209b60bcd59af90662d446`  
		Last Modified: Tue, 21 Nov 2023 07:55:01 GMT  
		Size: 39.0 MB (39031078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b0733c721e2ac151b2a04aa4474c02909229c16794206a817831aaf359c3586`  
		Last Modified: Tue, 21 Nov 2023 07:54:58 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898bac72b3df0026173253ea7ec67fdf05a7b81e4b1b35117bbefeeb74161be3`  
		Last Modified: Tue, 21 Nov 2023 07:54:58 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df6dfa461e8b59dabcba0ba599e8cf4ac4467d94a12592cfac6025ae0656cb7`  
		Last Modified: Tue, 21 Nov 2023 07:54:58 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d16e9798ed2dcc347e66efbb5cc6cb53f4a73440518bf6a3c0adad2ee71cfd`  
		Last Modified: Tue, 21 Nov 2023 07:54:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:ddfb19f4790a031d6ec710b47c8ca87e3c7196d86bd72a6df49f915f6fc42688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:19be5733a588e013e2c291d4859912263be55b51ccf536eb1bd7bc1d43c1ae57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84601725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ee8e9e2374fc1d5a8f7e6ace34246c2ce60e99b8566c0d1ce0f9d307c41b83`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:33 GMT
ADD file:29d3eb64d192a97184f2aa169407b58e969b06268c6372b49eefb72bcadb6e99 in / 
# Wed, 01 Nov 2023 00:21:34 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:47:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 01 Nov 2023 01:47:36 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 01 Nov 2023 01:47:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:47:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 01 Nov 2023 01:47:47 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 01 Nov 2023 01:47:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:48:16 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 01 Nov 2023 01:48:17 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 01 Nov 2023 01:48:34 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 01 Nov 2023 01:48:35 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 01 Nov 2023 01:48:35 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 01 Nov 2023 01:48:35 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 01 Nov 2023 01:48:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 01 Nov 2023 01:48:36 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 01 Nov 2023 01:48:36 GMT
VOLUME [/opt/couchdb/data]
# Wed, 01 Nov 2023 01:48:36 GMT
EXPOSE 4369 5984 9100
# Wed, 01 Nov 2023 01:48:36 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:113c6ad4754853f4a2ae632cff7d90eba9145cca0bd6fa4d60aa432bd26be6c7`  
		Last Modified: Wed, 01 Nov 2023 00:26:56 GMT  
		Size: 27.2 MB (27187422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365ea17356912d8ab65ea5e3a1e839d36823f7303a6f99fec14eb169f5a4f2e1`  
		Last Modified: Wed, 01 Nov 2023 01:49:33 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2706b6ad14bfc13aa94a94269c8479e367a22ebbf64f230b4a133b8198b51523`  
		Last Modified: Wed, 01 Nov 2023 01:49:32 GMT  
		Size: 6.7 MB (6704557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3cbd037256b0218774d56e4d3151275a32733815758ef37784eae1b624c9831`  
		Last Modified: Wed, 01 Nov 2023 01:49:31 GMT  
		Size: 1.3 MB (1259891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7bc073931afdef902766bdbf4440108b63b7e7a8afc61c51d5132e2b366910`  
		Last Modified: Wed, 01 Nov 2023 01:49:31 GMT  
		Size: 294.5 KB (294533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b65f0118e1821e295770007c76deb6fe634a42524867a48e15ec8f7a13ae28`  
		Last Modified: Wed, 01 Nov 2023 01:49:45 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba2feaa281f86c66f6d3385abb0a3c253bb921c23c2fb5b7f037c54dfd0e9fc`  
		Last Modified: Wed, 01 Nov 2023 01:49:48 GMT  
		Size: 49.1 MB (49148308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60a8b754ebf89dcda4a9b032fc7d76cfaf67b4d1cdd88a92fd548bfdde80785`  
		Last Modified: Wed, 01 Nov 2023 01:49:43 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199951c325e2234c69de9082ae7590bd8eeb37f76ccf34d718f5393cdbe10f76`  
		Last Modified: Wed, 01 Nov 2023 01:49:43 GMT  
		Size: 764.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f41fd1ccaf8d2e0c1c37dc2a8a78d3d6ebe9650c37c188cc04833e726242a4a`  
		Last Modified: Wed, 01 Nov 2023 01:49:43 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ad5245583de27094c466123980bca3addac07d4fc43887ea3f7598abcec934`  
		Last Modified: Wed, 01 Nov 2023 01:49:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:f6c2eb09ebaa599f0a93c7f28e5f47185121416af39120dd80ee27ae42e90a63
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73042770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ab83c5db3e862a9904f8a1d3e4821e2ab1d2eb563d33313ac79316b544b348`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:34 GMT
ADD file:475e94b9a8f65c7cd4d4156af31e83190240ff35d8038f3fa86ad124d4d5d299 in / 
# Tue, 21 Nov 2023 06:27:35 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:53:23 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 21 Nov 2023 07:53:24 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 21 Nov 2023 07:53:33 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:53:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 21 Nov 2023 07:53:37 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 21 Nov 2023 07:53:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:54:03 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 21 Nov 2023 07:54:04 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 21 Nov 2023 07:54:15 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 21 Nov 2023 07:54:16 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 21 Nov 2023 07:54:16 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 21 Nov 2023 07:54:16 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 21 Nov 2023 07:54:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 21 Nov 2023 07:54:16 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 07:54:16 GMT
VOLUME [/opt/couchdb/data]
# Tue, 21 Nov 2023 07:54:17 GMT
EXPOSE 4369 5984 9100
# Tue, 21 Nov 2023 07:54:17 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:78b429e3efdd9f2b163abf0bca6b1462a25b1c5eddc1dd47f5d3445c6413cfa1`  
		Last Modified: Tue, 21 Nov 2023 06:31:45 GMT  
		Size: 26.0 MB (25967796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3c5bfaccf97ef74c924764aca27d055d3cab8446f6ef59870cd544056d4cec`  
		Last Modified: Tue, 21 Nov 2023 07:54:50 GMT  
		Size: 3.4 KB (3434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff6bf33f9c2e30b4f1ce3f1bf6149231315457866fad15eedffdf007ad01f5e`  
		Last Modified: Tue, 21 Nov 2023 07:54:49 GMT  
		Size: 6.6 MB (6577624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0040bf5cab2106c8e662145f7f764673fdd1f2b1ea63a2f64a94333049636031`  
		Last Modified: Tue, 21 Nov 2023 07:54:48 GMT  
		Size: 1.2 MB (1164833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f6ff98dded5f418fecd217598fdeb4a722749c105e50a53dce349adc0872191`  
		Last Modified: Tue, 21 Nov 2023 07:54:48 GMT  
		Size: 294.4 KB (294403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b62b412c39c27d6b0bb77c29580f219e6832aa220a1ed8f0e2bb8ac5e792a8c`  
		Last Modified: Tue, 21 Nov 2023 07:55:00 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb05dfa0bb3aaeb852e7044d0f340c9f2ab0670711209b60bcd59af90662d446`  
		Last Modified: Tue, 21 Nov 2023 07:55:01 GMT  
		Size: 39.0 MB (39031078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b0733c721e2ac151b2a04aa4474c02909229c16794206a817831aaf359c3586`  
		Last Modified: Tue, 21 Nov 2023 07:54:58 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898bac72b3df0026173253ea7ec67fdf05a7b81e4b1b35117bbefeeb74161be3`  
		Last Modified: Tue, 21 Nov 2023 07:54:58 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df6dfa461e8b59dabcba0ba599e8cf4ac4467d94a12592cfac6025ae0656cb7`  
		Last Modified: Tue, 21 Nov 2023 07:54:58 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d16e9798ed2dcc347e66efbb5cc6cb53f4a73440518bf6a3c0adad2ee71cfd`  
		Last Modified: Tue, 21 Nov 2023 07:54:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3`

```console
$ docker pull couchdb@sha256:dc6bcc8ef7381be4ff0975b27e4cddaafd45bba68c2d5c8f7524f260d62cef93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:3c609bc33e472d4cb0a4ea0b117359bd0c9ed4f0628899131e8344fd13fbe01a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90245671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fff4b56666dbf396fc0b2eedb70c70b8990ccb6dc5d8447206f2243d21c1986c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:46:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 01 Nov 2023 01:46:41 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 01 Nov 2023 01:46:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:46:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 01 Nov 2023 01:46:51 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 01 Nov 2023 01:46:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:46:56 GMT
ENV COUCHDB_VERSION=3.3.2
# Wed, 01 Nov 2023 01:46:56 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 01 Nov 2023 01:47:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 01 Nov 2023 01:47:10 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 01 Nov 2023 01:47:10 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 01 Nov 2023 01:47:11 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 01 Nov 2023 01:47:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 01 Nov 2023 01:47:11 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 01 Nov 2023 01:47:11 GMT
VOLUME [/opt/couchdb/data]
# Wed, 01 Nov 2023 01:47:11 GMT
EXPOSE 4369 5984 9100
# Wed, 01 Nov 2023 01:47:11 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbba1a29bfe2ee9664ccd0caa145b5aa7a5480c276f1c42fd77ac32ef2c440c1`  
		Last Modified: Wed, 01 Nov 2023 01:48:53 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b21d450d3bd9333c8a5efb4081f440607452820e295142168061b2216f3986c`  
		Last Modified: Wed, 01 Nov 2023 01:48:53 GMT  
		Size: 5.2 MB (5226554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c93767e1cbf8a0b2d24469dbe0f750b73d88204210f83f7faa87b8be37dfaa`  
		Last Modified: Wed, 01 Nov 2023 01:48:52 GMT  
		Size: 610.9 KB (610919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24dc783ed2d49dd34054350d1a680091886de94bd264352e835184065e394e64`  
		Last Modified: Wed, 01 Nov 2023 01:48:52 GMT  
		Size: 295.2 KB (295153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8597086eac85cffb9306a84cfa8414bcda5500cb8092b1ba307a38e9e56540f`  
		Last Modified: Wed, 01 Nov 2023 01:48:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4fefd748372d68972d6fb14014c7813ac7837a6380b957f3092da518331958`  
		Last Modified: Wed, 01 Nov 2023 01:48:55 GMT  
		Size: 52.7 MB (52687716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ff2441b3a4073bbf88542aaf2d970fd2eb11cc4bd01c846d1245dae6187068`  
		Last Modified: Wed, 01 Nov 2023 01:48:50 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c29c7241d3a11a9dcf62611e3563275d0b24d32fa9f65fb5be837b13ef1cfb4`  
		Last Modified: Wed, 01 Nov 2023 01:48:50 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cacd4b2ce1758697d4898b78068d98430738b73f2f0171222ea8fc970a567603`  
		Last Modified: Wed, 01 Nov 2023 01:48:50 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7254e813570e08d636b0b367fb2dfe8c25dfa8b3a07a24b4dcf9574a9e238270`  
		Last Modified: Wed, 01 Nov 2023 01:48:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:831daf394c7922970580685f1b22701050dd6a16e2f3a494a0cc21d59d232e8a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88692917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb7b80ab6c0be332c785fef11c78605df05520b29c166d4b8419e9ba11b4137d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:52:39 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 21 Nov 2023 07:52:39 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 21 Nov 2023 07:52:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:52:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 21 Nov 2023 07:52:48 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 21 Nov 2023 07:52:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:52:53 GMT
ENV COUCHDB_VERSION=3.3.2
# Tue, 21 Nov 2023 07:52:53 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 21 Nov 2023 07:53:04 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 21 Nov 2023 07:53:05 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 21 Nov 2023 07:53:05 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 21 Nov 2023 07:53:05 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 21 Nov 2023 07:53:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 21 Nov 2023 07:53:06 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 07:53:06 GMT
VOLUME [/opt/couchdb/data]
# Tue, 21 Nov 2023 07:53:06 GMT
EXPOSE 4369 5984 9100
# Tue, 21 Nov 2023 07:53:06 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a831f10e5df507c8f1e02bf16d8431aea07447742165f87bac8012c02082c5c1`  
		Last Modified: Tue, 21 Nov 2023 07:54:32 GMT  
		Size: 3.4 KB (3431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4f74c0ee547299d86d3b6de1a1b677264a77024288fe76a0459fe1596e94b0`  
		Last Modified: Tue, 21 Nov 2023 07:54:31 GMT  
		Size: 5.2 MB (5210800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a278347563aa0aac229a39ef7f2d07a6925c6a95f1eca2dc9335921b7b75f3`  
		Last Modified: Tue, 21 Nov 2023 07:54:31 GMT  
		Size: 567.0 KB (567042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:479409bd9ad96512a7ba2074dabd9869a645ffa5edcc2ed2838022c816bae08d`  
		Last Modified: Tue, 21 Nov 2023 07:54:30 GMT  
		Size: 295.0 KB (295025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb46e8fd7a961878d2567e65d067b58ff68156ff62061cc8a8eb83c963dec48`  
		Last Modified: Tue, 21 Nov 2023 07:54:30 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0693fcb978a2b25d973a958ba01b81f13a42056be06852f67b9267b84065469`  
		Last Modified: Tue, 21 Nov 2023 07:54:32 GMT  
		Size: 52.5 MB (52548491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb62433b69e69906e6e298abde0a0d51dd57cff56e397b5095cca42260b91396`  
		Last Modified: Tue, 21 Nov 2023 07:54:28 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429f575265d6dad0cc72071474dc91d355558fbb8878d15303208499c66db6ba`  
		Last Modified: Tue, 21 Nov 2023 07:54:28 GMT  
		Size: 999.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4dd6cdf208e02f406ff8afb4344c4bbeead85c1af4146cae59fd96374d2b04`  
		Last Modified: Tue, 21 Nov 2023 07:54:28 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759e8a99734a273cc774b1971af710af95d4adc3fbff7de0f6efa32f09aabb04`  
		Last Modified: Tue, 21 Nov 2023 07:54:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:ccf9e925a92c4e47c922173bb8a6541607469de85a3d23b8f709a5b2f9fa4571
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95968231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d5240fcc3525a7c996865649016d229a3b75d1447c7ade86132d7ede52ffe8`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Nov 2023 04:24:43 GMT
ADD file:b0d18f2d04821eb50d1faecc1a64916f5c63dd386ae71a3b2cb1d6c4aac6e1c4 in / 
# Tue, 21 Nov 2023 04:24:46 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:12:10 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 21 Nov 2023 07:12:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 21 Nov 2023 07:12:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:12:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 21 Nov 2023 07:12:37 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 21 Nov 2023 07:12:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:12:47 GMT
ENV COUCHDB_VERSION=3.3.2
# Tue, 21 Nov 2023 07:12:49 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 21 Nov 2023 07:13:13 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 21 Nov 2023 07:13:17 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 21 Nov 2023 07:13:17 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 21 Nov 2023 07:13:17 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 21 Nov 2023 07:13:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 21 Nov 2023 07:13:20 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 07:13:20 GMT
VOLUME [/opt/couchdb/data]
# Tue, 21 Nov 2023 07:13:20 GMT
EXPOSE 4369 5984 9100
# Tue, 21 Nov 2023 07:13:21 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:60239a74847cd7e9a928353188f3cf096ca8cf648e2b27c765058e169d568fd9`  
		Last Modified: Tue, 21 Nov 2023 04:29:47 GMT  
		Size: 35.3 MB (35293727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f63eed5db2c906b6108908d9dc6976c9a23f1bb19a0e617257decd133e7592d`  
		Last Modified: Tue, 21 Nov 2023 07:14:05 GMT  
		Size: 3.4 KB (3408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:941bb642de45bb343a873e9c819cd85bffe05a010a6da631d1723612f69c794c`  
		Last Modified: Tue, 21 Nov 2023 07:14:04 GMT  
		Size: 6.0 MB (6046203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f2659433b58c3235f1e9085447d55d5c442efc597e42f97dfce11b106d84c0`  
		Last Modified: Tue, 21 Nov 2023 07:14:04 GMT  
		Size: 662.9 KB (662883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d777a7fd59124bb1d1eed56bddee9639f6ea57c6eaf67610a97a4a8c833814e9`  
		Last Modified: Tue, 21 Nov 2023 07:14:03 GMT  
		Size: 295.1 KB (295091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef322b815f454b44be7fc5bbc3f2c179419841031a40a753c25cb71a704158f4`  
		Last Modified: Tue, 21 Nov 2023 07:14:03 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6180ccba02f37081c0d1523baa72b7df6183b2284a575cc84c8f245ed21624fc`  
		Last Modified: Tue, 21 Nov 2023 07:14:07 GMT  
		Size: 53.7 MB (53662909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991739364f41cbdef5c3adb115b1f41c51bbafbd6555e32316cad98f1cae7e54`  
		Last Modified: Tue, 21 Nov 2023 07:14:01 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f539c1a9af058023c294a0b078bb81ec732ba18d3e4c624af45c5e3a877c5dd`  
		Last Modified: Tue, 21 Nov 2023 07:14:01 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27abb88fb75707dd945625a5a2734aa790dcd4330e5d257d13fde86d69630c4`  
		Last Modified: Tue, 21 Nov 2023 07:14:01 GMT  
		Size: 2.2 KB (2232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7837c78696f2a9940c752105b06aeb98a48f8a6eacab80ba3a467f89fbe31ee5`  
		Last Modified: Tue, 21 Nov 2023 07:14:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; s390x

```console
$ docker pull couchdb@sha256:21965f0438b454449366375d4c6bfd319e83dec568e9907669ba2b6a1c077563
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (87002806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba071f2f075a8263e2e67f1fc0f844debd3e57242ac3165ff9adcfacf2338049`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Nov 2023 05:05:18 GMT
ADD file:a545f27075704ce13e33e539170d3f47007424d2cc2bea5aecfd2608a5194151 in / 
# Tue, 21 Nov 2023 05:05:22 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:20:22 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 21 Nov 2023 06:20:22 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 21 Nov 2023 06:20:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:20:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 21 Nov 2023 06:20:31 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 21 Nov 2023 06:20:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:20:36 GMT
ENV COUCHDB_VERSION=3.3.2
# Tue, 21 Nov 2023 06:20:36 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 21 Nov 2023 06:20:53 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 21 Nov 2023 06:20:55 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 21 Nov 2023 06:20:55 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 21 Nov 2023 06:20:55 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 21 Nov 2023 06:20:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 21 Nov 2023 06:20:56 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 06:20:56 GMT
VOLUME [/opt/couchdb/data]
# Tue, 21 Nov 2023 06:20:56 GMT
EXPOSE 4369 5984 9100
# Tue, 21 Nov 2023 06:20:56 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b114072f1cab66b7376d690985b12816aebab2e4e41fc170e32f111df27951dc`  
		Last Modified: Tue, 21 Nov 2023 05:10:48 GMT  
		Size: 29.7 MB (29656938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72dba253785a5e917fdd9064f61b676b4080ff3073424ff387308d70579c728b`  
		Last Modified: Tue, 21 Nov 2023 06:21:15 GMT  
		Size: 3.4 KB (3431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a299cd04ea14bbc3034e11001a1ec06dd4b5e1aaa78317dc803570f8a4c6437`  
		Last Modified: Tue, 21 Nov 2023 06:21:15 GMT  
		Size: 5.1 MB (5111719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c684e5bcbb93c8f0c9da5b81b4a1d19274f7ad0c7e3b17eb12cbe45cd2514989`  
		Last Modified: Tue, 21 Nov 2023 06:21:14 GMT  
		Size: 573.6 KB (573635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d916370cd04b7352346fee3edc1ac77bdb9393e24c5bc62c4cb0803a682836`  
		Last Modified: Tue, 21 Nov 2023 06:21:14 GMT  
		Size: 295.1 KB (295096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e602d723a112bfbe3ebaca9b99e2e9636dac8b07c69947311ceb07666d40ed`  
		Last Modified: Tue, 21 Nov 2023 06:21:14 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdbafbeffdc5d29b56e0ccf672e48ead551f49aa23534b4fd9aefcd339587dc5`  
		Last Modified: Tue, 21 Nov 2023 06:21:18 GMT  
		Size: 51.4 MB (51357976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f08f21ade417458e581ec8afdf835c5d165444c0e93fdc330cbd6146af1da3`  
		Last Modified: Tue, 21 Nov 2023 06:21:13 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a4bc9e282fe338ed74c99dbb5cb5777e0ba1a2d068de6e102a8adbb34acc14`  
		Last Modified: Tue, 21 Nov 2023 06:21:13 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c93f5a64665780dfb559adfed9587064e52e00c9c515834a97cf26e3529da9`  
		Last Modified: Tue, 21 Nov 2023 06:21:13 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f6f407505b71a14801c0c71da8d0ce2a85d8c65d58e7998784a75dcde3cfb6`  
		Last Modified: Tue, 21 Nov 2023 06:21:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:7dd549717e94af28eb0cbeacf10318f539a19ff5ff2930eb2bd427322851fbb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:d64439bcd931bfe3b2b48135529b514beab649fa0259881fd04c774f2c3d5422
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80075635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205e57c6f99f40a4d603140fe6501754b9f090f9630e35f08a02887e35b43e91`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:33 GMT
ADD file:29d3eb64d192a97184f2aa169407b58e969b06268c6372b49eefb72bcadb6e99 in / 
# Wed, 01 Nov 2023 00:21:34 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:47:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 01 Nov 2023 01:47:36 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 01 Nov 2023 01:47:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:47:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 01 Nov 2023 01:47:47 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 01 Nov 2023 01:47:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:47:53 GMT
ENV COUCHDB_VERSION=3.1.2
# Wed, 01 Nov 2023 01:47:54 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 01 Nov 2023 01:48:07 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 01 Nov 2023 01:48:08 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 01 Nov 2023 01:48:08 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 01 Nov 2023 01:48:08 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 01 Nov 2023 01:48:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 01 Nov 2023 01:48:09 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 01 Nov 2023 01:48:09 GMT
VOLUME [/opt/couchdb/data]
# Wed, 01 Nov 2023 01:48:09 GMT
EXPOSE 4369 5984 9100
# Wed, 01 Nov 2023 01:48:09 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:113c6ad4754853f4a2ae632cff7d90eba9145cca0bd6fa4d60aa432bd26be6c7`  
		Last Modified: Wed, 01 Nov 2023 00:26:56 GMT  
		Size: 27.2 MB (27187422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365ea17356912d8ab65ea5e3a1e839d36823f7303a6f99fec14eb169f5a4f2e1`  
		Last Modified: Wed, 01 Nov 2023 01:49:33 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2706b6ad14bfc13aa94a94269c8479e367a22ebbf64f230b4a133b8198b51523`  
		Last Modified: Wed, 01 Nov 2023 01:49:32 GMT  
		Size: 6.7 MB (6704557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3cbd037256b0218774d56e4d3151275a32733815758ef37784eae1b624c9831`  
		Last Modified: Wed, 01 Nov 2023 01:49:31 GMT  
		Size: 1.3 MB (1259891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7bc073931afdef902766bdbf4440108b63b7e7a8afc61c51d5132e2b366910`  
		Last Modified: Wed, 01 Nov 2023 01:49:31 GMT  
		Size: 294.5 KB (294533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4debe8d86185b55779861ac36695c6d3d6f33c7b19c8b4d6d8b1edf847264fc8`  
		Last Modified: Wed, 01 Nov 2023 01:49:30 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:771c29924f094333de4b98cd2e8acaa0f6bd0f0737f62f73c3ff771764790fb0`  
		Last Modified: Wed, 01 Nov 2023 01:49:33 GMT  
		Size: 44.6 MB (44622218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04407e3339446bef5cd7c3a5bdadbe859d94da08f9f3387a2c933c5c3a701289`  
		Last Modified: Wed, 01 Nov 2023 01:49:29 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4e74a59eb1bbbac0433a03c3df812810095d2f7d1e03133d6501fd8c29ba83`  
		Last Modified: Wed, 01 Nov 2023 01:49:29 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c433447043d6daa20d54cff95f75f0e1f42b9f8a3e91ae1f28e5964d2f7b08`  
		Last Modified: Wed, 01 Nov 2023 01:49:29 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74642c019385d2d0c4880e20c048b3e1ca10a9ac41ee087a3d2aa1472198bece`  
		Last Modified: Wed, 01 Nov 2023 01:49:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:37cc498008183d12dd4e01b804cefe36ebab637b48c806c1e209702798d42690
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75138387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c17b5985551eb87f31d003a31f350852ebca8ba78287ed3f55dd68678ec17ca`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:34 GMT
ADD file:475e94b9a8f65c7cd4d4156af31e83190240ff35d8038f3fa86ad124d4d5d299 in / 
# Tue, 21 Nov 2023 06:27:35 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:53:23 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 21 Nov 2023 07:53:24 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 21 Nov 2023 07:53:33 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:53:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 21 Nov 2023 07:53:37 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 21 Nov 2023 07:53:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:53:43 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 21 Nov 2023 07:53:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 21 Nov 2023 07:53:55 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 21 Nov 2023 07:53:55 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 21 Nov 2023 07:53:55 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 21 Nov 2023 07:53:56 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 21 Nov 2023 07:53:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 21 Nov 2023 07:53:56 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 07:53:56 GMT
VOLUME [/opt/couchdb/data]
# Tue, 21 Nov 2023 07:53:56 GMT
EXPOSE 4369 5984 9100
# Tue, 21 Nov 2023 07:53:56 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:78b429e3efdd9f2b163abf0bca6b1462a25b1c5eddc1dd47f5d3445c6413cfa1`  
		Last Modified: Tue, 21 Nov 2023 06:31:45 GMT  
		Size: 26.0 MB (25967796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3c5bfaccf97ef74c924764aca27d055d3cab8446f6ef59870cd544056d4cec`  
		Last Modified: Tue, 21 Nov 2023 07:54:50 GMT  
		Size: 3.4 KB (3434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff6bf33f9c2e30b4f1ce3f1bf6149231315457866fad15eedffdf007ad01f5e`  
		Last Modified: Tue, 21 Nov 2023 07:54:49 GMT  
		Size: 6.6 MB (6577624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0040bf5cab2106c8e662145f7f764673fdd1f2b1ea63a2f64a94333049636031`  
		Last Modified: Tue, 21 Nov 2023 07:54:48 GMT  
		Size: 1.2 MB (1164833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f6ff98dded5f418fecd217598fdeb4a722749c105e50a53dce349adc0872191`  
		Last Modified: Tue, 21 Nov 2023 07:54:48 GMT  
		Size: 294.4 KB (294403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b3cf58bd99b2965a4aa657d7191e0436efdee52829d14f4b0e7c830ed26296`  
		Last Modified: Tue, 21 Nov 2023 07:54:48 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50d22884607a48a62a9335825c3f44fe0065a733e89d1c09cdf41fa1f20421d`  
		Last Modified: Tue, 21 Nov 2023 07:54:49 GMT  
		Size: 41.1 MB (41126695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041cbf629fcf79f3a1ae7768c35b231256213eb7a6a245e48871a296ca1c5e1c`  
		Last Modified: Tue, 21 Nov 2023 07:54:46 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:092b48f8245b28b3573e94e1d5e6df3c5b930eee14f17cf005f4a43a2baf2ab8`  
		Last Modified: Tue, 21 Nov 2023 07:54:46 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e42c042eb9e348de2b88f5421f8526d33d89321080bf5cb2af402fff160e965`  
		Last Modified: Tue, 21 Nov 2023 07:54:46 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b2de15229ac86dc89469f80ca89c3565745f1a26b772a362d1e55c3d00c65b`  
		Last Modified: Tue, 21 Nov 2023 07:54:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1.2`

```console
$ docker pull couchdb@sha256:7dd549717e94af28eb0cbeacf10318f539a19ff5ff2930eb2bd427322851fbb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1.2` - linux; amd64

```console
$ docker pull couchdb@sha256:d64439bcd931bfe3b2b48135529b514beab649fa0259881fd04c774f2c3d5422
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80075635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205e57c6f99f40a4d603140fe6501754b9f090f9630e35f08a02887e35b43e91`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:33 GMT
ADD file:29d3eb64d192a97184f2aa169407b58e969b06268c6372b49eefb72bcadb6e99 in / 
# Wed, 01 Nov 2023 00:21:34 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:47:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 01 Nov 2023 01:47:36 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 01 Nov 2023 01:47:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:47:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 01 Nov 2023 01:47:47 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 01 Nov 2023 01:47:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:47:53 GMT
ENV COUCHDB_VERSION=3.1.2
# Wed, 01 Nov 2023 01:47:54 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 01 Nov 2023 01:48:07 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 01 Nov 2023 01:48:08 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 01 Nov 2023 01:48:08 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 01 Nov 2023 01:48:08 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 01 Nov 2023 01:48:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 01 Nov 2023 01:48:09 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 01 Nov 2023 01:48:09 GMT
VOLUME [/opt/couchdb/data]
# Wed, 01 Nov 2023 01:48:09 GMT
EXPOSE 4369 5984 9100
# Wed, 01 Nov 2023 01:48:09 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:113c6ad4754853f4a2ae632cff7d90eba9145cca0bd6fa4d60aa432bd26be6c7`  
		Last Modified: Wed, 01 Nov 2023 00:26:56 GMT  
		Size: 27.2 MB (27187422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365ea17356912d8ab65ea5e3a1e839d36823f7303a6f99fec14eb169f5a4f2e1`  
		Last Modified: Wed, 01 Nov 2023 01:49:33 GMT  
		Size: 3.4 KB (3412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2706b6ad14bfc13aa94a94269c8479e367a22ebbf64f230b4a133b8198b51523`  
		Last Modified: Wed, 01 Nov 2023 01:49:32 GMT  
		Size: 6.7 MB (6704557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3cbd037256b0218774d56e4d3151275a32733815758ef37784eae1b624c9831`  
		Last Modified: Wed, 01 Nov 2023 01:49:31 GMT  
		Size: 1.3 MB (1259891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7bc073931afdef902766bdbf4440108b63b7e7a8afc61c51d5132e2b366910`  
		Last Modified: Wed, 01 Nov 2023 01:49:31 GMT  
		Size: 294.5 KB (294533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4debe8d86185b55779861ac36695c6d3d6f33c7b19c8b4d6d8b1edf847264fc8`  
		Last Modified: Wed, 01 Nov 2023 01:49:30 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:771c29924f094333de4b98cd2e8acaa0f6bd0f0737f62f73c3ff771764790fb0`  
		Last Modified: Wed, 01 Nov 2023 01:49:33 GMT  
		Size: 44.6 MB (44622218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04407e3339446bef5cd7c3a5bdadbe859d94da08f9f3387a2c933c5c3a701289`  
		Last Modified: Wed, 01 Nov 2023 01:49:29 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4e74a59eb1bbbac0433a03c3df812810095d2f7d1e03133d6501fd8c29ba83`  
		Last Modified: Wed, 01 Nov 2023 01:49:29 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c433447043d6daa20d54cff95f75f0e1f42b9f8a3e91ae1f28e5964d2f7b08`  
		Last Modified: Wed, 01 Nov 2023 01:49:29 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74642c019385d2d0c4880e20c048b3e1ca10a9ac41ee087a3d2aa1472198bece`  
		Last Modified: Wed, 01 Nov 2023 01:49:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:37cc498008183d12dd4e01b804cefe36ebab637b48c806c1e209702798d42690
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75138387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c17b5985551eb87f31d003a31f350852ebca8ba78287ed3f55dd68678ec17ca`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:34 GMT
ADD file:475e94b9a8f65c7cd4d4156af31e83190240ff35d8038f3fa86ad124d4d5d299 in / 
# Tue, 21 Nov 2023 06:27:35 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:53:23 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 21 Nov 2023 07:53:24 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 21 Nov 2023 07:53:33 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:53:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 21 Nov 2023 07:53:37 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 21 Nov 2023 07:53:43 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:53:43 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 21 Nov 2023 07:53:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 21 Nov 2023 07:53:55 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 21 Nov 2023 07:53:55 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 21 Nov 2023 07:53:55 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 21 Nov 2023 07:53:56 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 21 Nov 2023 07:53:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 21 Nov 2023 07:53:56 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 07:53:56 GMT
VOLUME [/opt/couchdb/data]
# Tue, 21 Nov 2023 07:53:56 GMT
EXPOSE 4369 5984 9100
# Tue, 21 Nov 2023 07:53:56 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:78b429e3efdd9f2b163abf0bca6b1462a25b1c5eddc1dd47f5d3445c6413cfa1`  
		Last Modified: Tue, 21 Nov 2023 06:31:45 GMT  
		Size: 26.0 MB (25967796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3c5bfaccf97ef74c924764aca27d055d3cab8446f6ef59870cd544056d4cec`  
		Last Modified: Tue, 21 Nov 2023 07:54:50 GMT  
		Size: 3.4 KB (3434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff6bf33f9c2e30b4f1ce3f1bf6149231315457866fad15eedffdf007ad01f5e`  
		Last Modified: Tue, 21 Nov 2023 07:54:49 GMT  
		Size: 6.6 MB (6577624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0040bf5cab2106c8e662145f7f764673fdd1f2b1ea63a2f64a94333049636031`  
		Last Modified: Tue, 21 Nov 2023 07:54:48 GMT  
		Size: 1.2 MB (1164833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f6ff98dded5f418fecd217598fdeb4a722749c105e50a53dce349adc0872191`  
		Last Modified: Tue, 21 Nov 2023 07:54:48 GMT  
		Size: 294.4 KB (294403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b3cf58bd99b2965a4aa657d7191e0436efdee52829d14f4b0e7c830ed26296`  
		Last Modified: Tue, 21 Nov 2023 07:54:48 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50d22884607a48a62a9335825c3f44fe0065a733e89d1c09cdf41fa1f20421d`  
		Last Modified: Tue, 21 Nov 2023 07:54:49 GMT  
		Size: 41.1 MB (41126695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:041cbf629fcf79f3a1ae7768c35b231256213eb7a6a245e48871a296ca1c5e1c`  
		Last Modified: Tue, 21 Nov 2023 07:54:46 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:092b48f8245b28b3573e94e1d5e6df3c5b930eee14f17cf005f4a43a2baf2ab8`  
		Last Modified: Tue, 21 Nov 2023 07:54:46 GMT  
		Size: 766.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e42c042eb9e348de2b88f5421f8526d33d89321080bf5cb2af402fff160e965`  
		Last Modified: Tue, 21 Nov 2023 07:54:46 GMT  
		Size: 2.1 KB (2060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b2de15229ac86dc89469f80ca89c3565745f1a26b772a362d1e55c3d00c65b`  
		Last Modified: Tue, 21 Nov 2023 07:54:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2`

```console
$ docker pull couchdb@sha256:8a5147883071d0704020753781b7fbd7e24fbeb8c49d1004c2da3e78d484939e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:920faa468ec44afab004cc39e9768aa379a91eb2b08df506bcdc5aaa18765bff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89746808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e098381214be901b170999d456be51caf296a2a26345be64f33d40dd2421f30`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:46:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 01 Nov 2023 01:46:41 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 01 Nov 2023 01:46:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:46:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 01 Nov 2023 01:46:51 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 01 Nov 2023 01:46:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:47:15 GMT
ENV COUCHDB_VERSION=3.2.3
# Wed, 01 Nov 2023 01:47:15 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 01 Nov 2023 01:47:28 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 01 Nov 2023 01:47:29 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 01 Nov 2023 01:47:29 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 01 Nov 2023 01:47:29 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 01 Nov 2023 01:47:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 01 Nov 2023 01:47:30 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 01 Nov 2023 01:47:30 GMT
VOLUME [/opt/couchdb/data]
# Wed, 01 Nov 2023 01:47:30 GMT
EXPOSE 4369 5984 9100
# Wed, 01 Nov 2023 01:47:30 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbba1a29bfe2ee9664ccd0caa145b5aa7a5480c276f1c42fd77ac32ef2c440c1`  
		Last Modified: Wed, 01 Nov 2023 01:48:53 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b21d450d3bd9333c8a5efb4081f440607452820e295142168061b2216f3986c`  
		Last Modified: Wed, 01 Nov 2023 01:48:53 GMT  
		Size: 5.2 MB (5226554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c93767e1cbf8a0b2d24469dbe0f750b73d88204210f83f7faa87b8be37dfaa`  
		Last Modified: Wed, 01 Nov 2023 01:48:52 GMT  
		Size: 610.9 KB (610919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24dc783ed2d49dd34054350d1a680091886de94bd264352e835184065e394e64`  
		Last Modified: Wed, 01 Nov 2023 01:48:52 GMT  
		Size: 295.2 KB (295153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3095226c333171f329b0b302f35b809cee56c32b4129b1faa460f655ca1da73a`  
		Last Modified: Wed, 01 Nov 2023 01:49:17 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05b8c804244b1c762a3d12f9ce96d57339dbfd5e4f2f514e001c76114d90362`  
		Last Modified: Wed, 01 Nov 2023 01:49:20 GMT  
		Size: 52.2 MB (52188854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608652e0912931c13140293ddf5859b35e9dc3ec420a7b7cdb66335dd8d4aa25`  
		Last Modified: Wed, 01 Nov 2023 01:49:15 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0740499e7d320dbadd105454a7a5783a998c0cecb76d1db6794baade4e8e715`  
		Last Modified: Wed, 01 Nov 2023 01:49:15 GMT  
		Size: 997.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f15b969faacebc224c92b52534e1bf59e947e6c973aa304d8502a732331de84`  
		Last Modified: Wed, 01 Nov 2023 01:49:15 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bafbb4496c4b925498eea59607a6cd21da7da01a3d8e67d869a0558b1506c8a`  
		Last Modified: Wed, 01 Nov 2023 01:49:15 GMT  
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
$ docker pull couchdb@sha256:eac50b3e16c45fed8c14501e6fd3f157a3b662291de7997d9625e770589dbbea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchdb:3.2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:920faa468ec44afab004cc39e9768aa379a91eb2b08df506bcdc5aaa18765bff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89746808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e098381214be901b170999d456be51caf296a2a26345be64f33d40dd2421f30`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:46:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 01 Nov 2023 01:46:41 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 01 Nov 2023 01:46:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:46:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 01 Nov 2023 01:46:51 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 01 Nov 2023 01:46:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:47:15 GMT
ENV COUCHDB_VERSION=3.2.3
# Wed, 01 Nov 2023 01:47:15 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 01 Nov 2023 01:47:28 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 01 Nov 2023 01:47:29 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 01 Nov 2023 01:47:29 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 01 Nov 2023 01:47:29 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 01 Nov 2023 01:47:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 01 Nov 2023 01:47:30 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 01 Nov 2023 01:47:30 GMT
VOLUME [/opt/couchdb/data]
# Wed, 01 Nov 2023 01:47:30 GMT
EXPOSE 4369 5984 9100
# Wed, 01 Nov 2023 01:47:30 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbba1a29bfe2ee9664ccd0caa145b5aa7a5480c276f1c42fd77ac32ef2c440c1`  
		Last Modified: Wed, 01 Nov 2023 01:48:53 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b21d450d3bd9333c8a5efb4081f440607452820e295142168061b2216f3986c`  
		Last Modified: Wed, 01 Nov 2023 01:48:53 GMT  
		Size: 5.2 MB (5226554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c93767e1cbf8a0b2d24469dbe0f750b73d88204210f83f7faa87b8be37dfaa`  
		Last Modified: Wed, 01 Nov 2023 01:48:52 GMT  
		Size: 610.9 KB (610919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24dc783ed2d49dd34054350d1a680091886de94bd264352e835184065e394e64`  
		Last Modified: Wed, 01 Nov 2023 01:48:52 GMT  
		Size: 295.2 KB (295153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3095226c333171f329b0b302f35b809cee56c32b4129b1faa460f655ca1da73a`  
		Last Modified: Wed, 01 Nov 2023 01:49:17 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05b8c804244b1c762a3d12f9ce96d57339dbfd5e4f2f514e001c76114d90362`  
		Last Modified: Wed, 01 Nov 2023 01:49:20 GMT  
		Size: 52.2 MB (52188854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608652e0912931c13140293ddf5859b35e9dc3ec420a7b7cdb66335dd8d4aa25`  
		Last Modified: Wed, 01 Nov 2023 01:49:15 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0740499e7d320dbadd105454a7a5783a998c0cecb76d1db6794baade4e8e715`  
		Last Modified: Wed, 01 Nov 2023 01:49:15 GMT  
		Size: 997.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f15b969faacebc224c92b52534e1bf59e947e6c973aa304d8502a732331de84`  
		Last Modified: Wed, 01 Nov 2023 01:49:15 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bafbb4496c4b925498eea59607a6cd21da7da01a3d8e67d869a0558b1506c8a`  
		Last Modified: Wed, 01 Nov 2023 01:49:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.3`

```console
$ docker pull couchdb@sha256:dc6bcc8ef7381be4ff0975b27e4cddaafd45bba68c2d5c8f7524f260d62cef93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `couchdb:3.3` - linux; amd64

```console
$ docker pull couchdb@sha256:3c609bc33e472d4cb0a4ea0b117359bd0c9ed4f0628899131e8344fd13fbe01a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90245671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fff4b56666dbf396fc0b2eedb70c70b8990ccb6dc5d8447206f2243d21c1986c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:46:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 01 Nov 2023 01:46:41 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 01 Nov 2023 01:46:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:46:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 01 Nov 2023 01:46:51 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 01 Nov 2023 01:46:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:46:56 GMT
ENV COUCHDB_VERSION=3.3.2
# Wed, 01 Nov 2023 01:46:56 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 01 Nov 2023 01:47:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 01 Nov 2023 01:47:10 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 01 Nov 2023 01:47:10 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 01 Nov 2023 01:47:11 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 01 Nov 2023 01:47:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 01 Nov 2023 01:47:11 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 01 Nov 2023 01:47:11 GMT
VOLUME [/opt/couchdb/data]
# Wed, 01 Nov 2023 01:47:11 GMT
EXPOSE 4369 5984 9100
# Wed, 01 Nov 2023 01:47:11 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbba1a29bfe2ee9664ccd0caa145b5aa7a5480c276f1c42fd77ac32ef2c440c1`  
		Last Modified: Wed, 01 Nov 2023 01:48:53 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b21d450d3bd9333c8a5efb4081f440607452820e295142168061b2216f3986c`  
		Last Modified: Wed, 01 Nov 2023 01:48:53 GMT  
		Size: 5.2 MB (5226554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c93767e1cbf8a0b2d24469dbe0f750b73d88204210f83f7faa87b8be37dfaa`  
		Last Modified: Wed, 01 Nov 2023 01:48:52 GMT  
		Size: 610.9 KB (610919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24dc783ed2d49dd34054350d1a680091886de94bd264352e835184065e394e64`  
		Last Modified: Wed, 01 Nov 2023 01:48:52 GMT  
		Size: 295.2 KB (295153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8597086eac85cffb9306a84cfa8414bcda5500cb8092b1ba307a38e9e56540f`  
		Last Modified: Wed, 01 Nov 2023 01:48:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4fefd748372d68972d6fb14014c7813ac7837a6380b957f3092da518331958`  
		Last Modified: Wed, 01 Nov 2023 01:48:55 GMT  
		Size: 52.7 MB (52687716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ff2441b3a4073bbf88542aaf2d970fd2eb11cc4bd01c846d1245dae6187068`  
		Last Modified: Wed, 01 Nov 2023 01:48:50 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c29c7241d3a11a9dcf62611e3563275d0b24d32fa9f65fb5be837b13ef1cfb4`  
		Last Modified: Wed, 01 Nov 2023 01:48:50 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cacd4b2ce1758697d4898b78068d98430738b73f2f0171222ea8fc970a567603`  
		Last Modified: Wed, 01 Nov 2023 01:48:50 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7254e813570e08d636b0b367fb2dfe8c25dfa8b3a07a24b4dcf9574a9e238270`  
		Last Modified: Wed, 01 Nov 2023 01:48:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:831daf394c7922970580685f1b22701050dd6a16e2f3a494a0cc21d59d232e8a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88692917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb7b80ab6c0be332c785fef11c78605df05520b29c166d4b8419e9ba11b4137d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:52:39 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 21 Nov 2023 07:52:39 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 21 Nov 2023 07:52:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:52:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 21 Nov 2023 07:52:48 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 21 Nov 2023 07:52:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:52:53 GMT
ENV COUCHDB_VERSION=3.3.2
# Tue, 21 Nov 2023 07:52:53 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 21 Nov 2023 07:53:04 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 21 Nov 2023 07:53:05 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 21 Nov 2023 07:53:05 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 21 Nov 2023 07:53:05 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 21 Nov 2023 07:53:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 21 Nov 2023 07:53:06 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 07:53:06 GMT
VOLUME [/opt/couchdb/data]
# Tue, 21 Nov 2023 07:53:06 GMT
EXPOSE 4369 5984 9100
# Tue, 21 Nov 2023 07:53:06 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a831f10e5df507c8f1e02bf16d8431aea07447742165f87bac8012c02082c5c1`  
		Last Modified: Tue, 21 Nov 2023 07:54:32 GMT  
		Size: 3.4 KB (3431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4f74c0ee547299d86d3b6de1a1b677264a77024288fe76a0459fe1596e94b0`  
		Last Modified: Tue, 21 Nov 2023 07:54:31 GMT  
		Size: 5.2 MB (5210800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a278347563aa0aac229a39ef7f2d07a6925c6a95f1eca2dc9335921b7b75f3`  
		Last Modified: Tue, 21 Nov 2023 07:54:31 GMT  
		Size: 567.0 KB (567042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:479409bd9ad96512a7ba2074dabd9869a645ffa5edcc2ed2838022c816bae08d`  
		Last Modified: Tue, 21 Nov 2023 07:54:30 GMT  
		Size: 295.0 KB (295025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb46e8fd7a961878d2567e65d067b58ff68156ff62061cc8a8eb83c963dec48`  
		Last Modified: Tue, 21 Nov 2023 07:54:30 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0693fcb978a2b25d973a958ba01b81f13a42056be06852f67b9267b84065469`  
		Last Modified: Tue, 21 Nov 2023 07:54:32 GMT  
		Size: 52.5 MB (52548491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb62433b69e69906e6e298abde0a0d51dd57cff56e397b5095cca42260b91396`  
		Last Modified: Tue, 21 Nov 2023 07:54:28 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429f575265d6dad0cc72071474dc91d355558fbb8878d15303208499c66db6ba`  
		Last Modified: Tue, 21 Nov 2023 07:54:28 GMT  
		Size: 999.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4dd6cdf208e02f406ff8afb4344c4bbeead85c1af4146cae59fd96374d2b04`  
		Last Modified: Tue, 21 Nov 2023 07:54:28 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759e8a99734a273cc774b1971af710af95d4adc3fbff7de0f6efa32f09aabb04`  
		Last Modified: Tue, 21 Nov 2023 07:54:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:ccf9e925a92c4e47c922173bb8a6541607469de85a3d23b8f709a5b2f9fa4571
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95968231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d5240fcc3525a7c996865649016d229a3b75d1447c7ade86132d7ede52ffe8`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Nov 2023 04:24:43 GMT
ADD file:b0d18f2d04821eb50d1faecc1a64916f5c63dd386ae71a3b2cb1d6c4aac6e1c4 in / 
# Tue, 21 Nov 2023 04:24:46 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:12:10 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 21 Nov 2023 07:12:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 21 Nov 2023 07:12:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:12:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 21 Nov 2023 07:12:37 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 21 Nov 2023 07:12:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:12:47 GMT
ENV COUCHDB_VERSION=3.3.2
# Tue, 21 Nov 2023 07:12:49 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 21 Nov 2023 07:13:13 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 21 Nov 2023 07:13:17 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 21 Nov 2023 07:13:17 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 21 Nov 2023 07:13:17 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 21 Nov 2023 07:13:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 21 Nov 2023 07:13:20 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 07:13:20 GMT
VOLUME [/opt/couchdb/data]
# Tue, 21 Nov 2023 07:13:20 GMT
EXPOSE 4369 5984 9100
# Tue, 21 Nov 2023 07:13:21 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:60239a74847cd7e9a928353188f3cf096ca8cf648e2b27c765058e169d568fd9`  
		Last Modified: Tue, 21 Nov 2023 04:29:47 GMT  
		Size: 35.3 MB (35293727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f63eed5db2c906b6108908d9dc6976c9a23f1bb19a0e617257decd133e7592d`  
		Last Modified: Tue, 21 Nov 2023 07:14:05 GMT  
		Size: 3.4 KB (3408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:941bb642de45bb343a873e9c819cd85bffe05a010a6da631d1723612f69c794c`  
		Last Modified: Tue, 21 Nov 2023 07:14:04 GMT  
		Size: 6.0 MB (6046203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f2659433b58c3235f1e9085447d55d5c442efc597e42f97dfce11b106d84c0`  
		Last Modified: Tue, 21 Nov 2023 07:14:04 GMT  
		Size: 662.9 KB (662883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d777a7fd59124bb1d1eed56bddee9639f6ea57c6eaf67610a97a4a8c833814e9`  
		Last Modified: Tue, 21 Nov 2023 07:14:03 GMT  
		Size: 295.1 KB (295091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef322b815f454b44be7fc5bbc3f2c179419841031a40a753c25cb71a704158f4`  
		Last Modified: Tue, 21 Nov 2023 07:14:03 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6180ccba02f37081c0d1523baa72b7df6183b2284a575cc84c8f245ed21624fc`  
		Last Modified: Tue, 21 Nov 2023 07:14:07 GMT  
		Size: 53.7 MB (53662909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991739364f41cbdef5c3adb115b1f41c51bbafbd6555e32316cad98f1cae7e54`  
		Last Modified: Tue, 21 Nov 2023 07:14:01 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f539c1a9af058023c294a0b078bb81ec732ba18d3e4c624af45c5e3a877c5dd`  
		Last Modified: Tue, 21 Nov 2023 07:14:01 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27abb88fb75707dd945625a5a2734aa790dcd4330e5d257d13fde86d69630c4`  
		Last Modified: Tue, 21 Nov 2023 07:14:01 GMT  
		Size: 2.2 KB (2232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7837c78696f2a9940c752105b06aeb98a48f8a6eacab80ba3a467f89fbe31ee5`  
		Last Modified: Tue, 21 Nov 2023 07:14:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3` - linux; s390x

```console
$ docker pull couchdb@sha256:21965f0438b454449366375d4c6bfd319e83dec568e9907669ba2b6a1c077563
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (87002806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba071f2f075a8263e2e67f1fc0f844debd3e57242ac3165ff9adcfacf2338049`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Nov 2023 05:05:18 GMT
ADD file:a545f27075704ce13e33e539170d3f47007424d2cc2bea5aecfd2608a5194151 in / 
# Tue, 21 Nov 2023 05:05:22 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:20:22 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 21 Nov 2023 06:20:22 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 21 Nov 2023 06:20:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:20:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 21 Nov 2023 06:20:31 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 21 Nov 2023 06:20:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:20:36 GMT
ENV COUCHDB_VERSION=3.3.2
# Tue, 21 Nov 2023 06:20:36 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 21 Nov 2023 06:20:53 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 21 Nov 2023 06:20:55 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 21 Nov 2023 06:20:55 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 21 Nov 2023 06:20:55 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 21 Nov 2023 06:20:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 21 Nov 2023 06:20:56 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 06:20:56 GMT
VOLUME [/opt/couchdb/data]
# Tue, 21 Nov 2023 06:20:56 GMT
EXPOSE 4369 5984 9100
# Tue, 21 Nov 2023 06:20:56 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b114072f1cab66b7376d690985b12816aebab2e4e41fc170e32f111df27951dc`  
		Last Modified: Tue, 21 Nov 2023 05:10:48 GMT  
		Size: 29.7 MB (29656938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72dba253785a5e917fdd9064f61b676b4080ff3073424ff387308d70579c728b`  
		Last Modified: Tue, 21 Nov 2023 06:21:15 GMT  
		Size: 3.4 KB (3431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a299cd04ea14bbc3034e11001a1ec06dd4b5e1aaa78317dc803570f8a4c6437`  
		Last Modified: Tue, 21 Nov 2023 06:21:15 GMT  
		Size: 5.1 MB (5111719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c684e5bcbb93c8f0c9da5b81b4a1d19274f7ad0c7e3b17eb12cbe45cd2514989`  
		Last Modified: Tue, 21 Nov 2023 06:21:14 GMT  
		Size: 573.6 KB (573635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d916370cd04b7352346fee3edc1ac77bdb9393e24c5bc62c4cb0803a682836`  
		Last Modified: Tue, 21 Nov 2023 06:21:14 GMT  
		Size: 295.1 KB (295096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e602d723a112bfbe3ebaca9b99e2e9636dac8b07c69947311ceb07666d40ed`  
		Last Modified: Tue, 21 Nov 2023 06:21:14 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdbafbeffdc5d29b56e0ccf672e48ead551f49aa23534b4fd9aefcd339587dc5`  
		Last Modified: Tue, 21 Nov 2023 06:21:18 GMT  
		Size: 51.4 MB (51357976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f08f21ade417458e581ec8afdf835c5d165444c0e93fdc330cbd6146af1da3`  
		Last Modified: Tue, 21 Nov 2023 06:21:13 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a4bc9e282fe338ed74c99dbb5cb5777e0ba1a2d068de6e102a8adbb34acc14`  
		Last Modified: Tue, 21 Nov 2023 06:21:13 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c93f5a64665780dfb559adfed9587064e52e00c9c515834a97cf26e3529da9`  
		Last Modified: Tue, 21 Nov 2023 06:21:13 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f6f407505b71a14801c0c71da8d0ce2a85d8c65d58e7998784a75dcde3cfb6`  
		Last Modified: Tue, 21 Nov 2023 06:21:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.3.2`

```console
$ docker pull couchdb@sha256:dc6bcc8ef7381be4ff0975b27e4cddaafd45bba68c2d5c8f7524f260d62cef93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `couchdb:3.3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:3c609bc33e472d4cb0a4ea0b117359bd0c9ed4f0628899131e8344fd13fbe01a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90245671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fff4b56666dbf396fc0b2eedb70c70b8990ccb6dc5d8447206f2243d21c1986c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:46:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 01 Nov 2023 01:46:41 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 01 Nov 2023 01:46:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:46:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 01 Nov 2023 01:46:51 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 01 Nov 2023 01:46:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:46:56 GMT
ENV COUCHDB_VERSION=3.3.2
# Wed, 01 Nov 2023 01:46:56 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 01 Nov 2023 01:47:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 01 Nov 2023 01:47:10 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 01 Nov 2023 01:47:10 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 01 Nov 2023 01:47:11 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 01 Nov 2023 01:47:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 01 Nov 2023 01:47:11 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 01 Nov 2023 01:47:11 GMT
VOLUME [/opt/couchdb/data]
# Wed, 01 Nov 2023 01:47:11 GMT
EXPOSE 4369 5984 9100
# Wed, 01 Nov 2023 01:47:11 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbba1a29bfe2ee9664ccd0caa145b5aa7a5480c276f1c42fd77ac32ef2c440c1`  
		Last Modified: Wed, 01 Nov 2023 01:48:53 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b21d450d3bd9333c8a5efb4081f440607452820e295142168061b2216f3986c`  
		Last Modified: Wed, 01 Nov 2023 01:48:53 GMT  
		Size: 5.2 MB (5226554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c93767e1cbf8a0b2d24469dbe0f750b73d88204210f83f7faa87b8be37dfaa`  
		Last Modified: Wed, 01 Nov 2023 01:48:52 GMT  
		Size: 610.9 KB (610919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24dc783ed2d49dd34054350d1a680091886de94bd264352e835184065e394e64`  
		Last Modified: Wed, 01 Nov 2023 01:48:52 GMT  
		Size: 295.2 KB (295153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8597086eac85cffb9306a84cfa8414bcda5500cb8092b1ba307a38e9e56540f`  
		Last Modified: Wed, 01 Nov 2023 01:48:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4fefd748372d68972d6fb14014c7813ac7837a6380b957f3092da518331958`  
		Last Modified: Wed, 01 Nov 2023 01:48:55 GMT  
		Size: 52.7 MB (52687716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ff2441b3a4073bbf88542aaf2d970fd2eb11cc4bd01c846d1245dae6187068`  
		Last Modified: Wed, 01 Nov 2023 01:48:50 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c29c7241d3a11a9dcf62611e3563275d0b24d32fa9f65fb5be837b13ef1cfb4`  
		Last Modified: Wed, 01 Nov 2023 01:48:50 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cacd4b2ce1758697d4898b78068d98430738b73f2f0171222ea8fc970a567603`  
		Last Modified: Wed, 01 Nov 2023 01:48:50 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7254e813570e08d636b0b367fb2dfe8c25dfa8b3a07a24b4dcf9574a9e238270`  
		Last Modified: Wed, 01 Nov 2023 01:48:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:831daf394c7922970580685f1b22701050dd6a16e2f3a494a0cc21d59d232e8a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88692917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb7b80ab6c0be332c785fef11c78605df05520b29c166d4b8419e9ba11b4137d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:52:39 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 21 Nov 2023 07:52:39 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 21 Nov 2023 07:52:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:52:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 21 Nov 2023 07:52:48 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 21 Nov 2023 07:52:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:52:53 GMT
ENV COUCHDB_VERSION=3.3.2
# Tue, 21 Nov 2023 07:52:53 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 21 Nov 2023 07:53:04 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 21 Nov 2023 07:53:05 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 21 Nov 2023 07:53:05 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 21 Nov 2023 07:53:05 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 21 Nov 2023 07:53:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 21 Nov 2023 07:53:06 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 07:53:06 GMT
VOLUME [/opt/couchdb/data]
# Tue, 21 Nov 2023 07:53:06 GMT
EXPOSE 4369 5984 9100
# Tue, 21 Nov 2023 07:53:06 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a831f10e5df507c8f1e02bf16d8431aea07447742165f87bac8012c02082c5c1`  
		Last Modified: Tue, 21 Nov 2023 07:54:32 GMT  
		Size: 3.4 KB (3431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4f74c0ee547299d86d3b6de1a1b677264a77024288fe76a0459fe1596e94b0`  
		Last Modified: Tue, 21 Nov 2023 07:54:31 GMT  
		Size: 5.2 MB (5210800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a278347563aa0aac229a39ef7f2d07a6925c6a95f1eca2dc9335921b7b75f3`  
		Last Modified: Tue, 21 Nov 2023 07:54:31 GMT  
		Size: 567.0 KB (567042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:479409bd9ad96512a7ba2074dabd9869a645ffa5edcc2ed2838022c816bae08d`  
		Last Modified: Tue, 21 Nov 2023 07:54:30 GMT  
		Size: 295.0 KB (295025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb46e8fd7a961878d2567e65d067b58ff68156ff62061cc8a8eb83c963dec48`  
		Last Modified: Tue, 21 Nov 2023 07:54:30 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0693fcb978a2b25d973a958ba01b81f13a42056be06852f67b9267b84065469`  
		Last Modified: Tue, 21 Nov 2023 07:54:32 GMT  
		Size: 52.5 MB (52548491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb62433b69e69906e6e298abde0a0d51dd57cff56e397b5095cca42260b91396`  
		Last Modified: Tue, 21 Nov 2023 07:54:28 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429f575265d6dad0cc72071474dc91d355558fbb8878d15303208499c66db6ba`  
		Last Modified: Tue, 21 Nov 2023 07:54:28 GMT  
		Size: 999.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4dd6cdf208e02f406ff8afb4344c4bbeead85c1af4146cae59fd96374d2b04`  
		Last Modified: Tue, 21 Nov 2023 07:54:28 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759e8a99734a273cc774b1971af710af95d4adc3fbff7de0f6efa32f09aabb04`  
		Last Modified: Tue, 21 Nov 2023 07:54:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3.2` - linux; ppc64le

```console
$ docker pull couchdb@sha256:ccf9e925a92c4e47c922173bb8a6541607469de85a3d23b8f709a5b2f9fa4571
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95968231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d5240fcc3525a7c996865649016d229a3b75d1447c7ade86132d7ede52ffe8`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Nov 2023 04:24:43 GMT
ADD file:b0d18f2d04821eb50d1faecc1a64916f5c63dd386ae71a3b2cb1d6c4aac6e1c4 in / 
# Tue, 21 Nov 2023 04:24:46 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:12:10 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 21 Nov 2023 07:12:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 21 Nov 2023 07:12:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:12:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 21 Nov 2023 07:12:37 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 21 Nov 2023 07:12:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:12:47 GMT
ENV COUCHDB_VERSION=3.3.2
# Tue, 21 Nov 2023 07:12:49 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 21 Nov 2023 07:13:13 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 21 Nov 2023 07:13:17 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 21 Nov 2023 07:13:17 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 21 Nov 2023 07:13:17 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 21 Nov 2023 07:13:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 21 Nov 2023 07:13:20 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 07:13:20 GMT
VOLUME [/opt/couchdb/data]
# Tue, 21 Nov 2023 07:13:20 GMT
EXPOSE 4369 5984 9100
# Tue, 21 Nov 2023 07:13:21 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:60239a74847cd7e9a928353188f3cf096ca8cf648e2b27c765058e169d568fd9`  
		Last Modified: Tue, 21 Nov 2023 04:29:47 GMT  
		Size: 35.3 MB (35293727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f63eed5db2c906b6108908d9dc6976c9a23f1bb19a0e617257decd133e7592d`  
		Last Modified: Tue, 21 Nov 2023 07:14:05 GMT  
		Size: 3.4 KB (3408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:941bb642de45bb343a873e9c819cd85bffe05a010a6da631d1723612f69c794c`  
		Last Modified: Tue, 21 Nov 2023 07:14:04 GMT  
		Size: 6.0 MB (6046203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f2659433b58c3235f1e9085447d55d5c442efc597e42f97dfce11b106d84c0`  
		Last Modified: Tue, 21 Nov 2023 07:14:04 GMT  
		Size: 662.9 KB (662883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d777a7fd59124bb1d1eed56bddee9639f6ea57c6eaf67610a97a4a8c833814e9`  
		Last Modified: Tue, 21 Nov 2023 07:14:03 GMT  
		Size: 295.1 KB (295091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef322b815f454b44be7fc5bbc3f2c179419841031a40a753c25cb71a704158f4`  
		Last Modified: Tue, 21 Nov 2023 07:14:03 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6180ccba02f37081c0d1523baa72b7df6183b2284a575cc84c8f245ed21624fc`  
		Last Modified: Tue, 21 Nov 2023 07:14:07 GMT  
		Size: 53.7 MB (53662909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991739364f41cbdef5c3adb115b1f41c51bbafbd6555e32316cad98f1cae7e54`  
		Last Modified: Tue, 21 Nov 2023 07:14:01 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f539c1a9af058023c294a0b078bb81ec732ba18d3e4c624af45c5e3a877c5dd`  
		Last Modified: Tue, 21 Nov 2023 07:14:01 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27abb88fb75707dd945625a5a2734aa790dcd4330e5d257d13fde86d69630c4`  
		Last Modified: Tue, 21 Nov 2023 07:14:01 GMT  
		Size: 2.2 KB (2232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7837c78696f2a9940c752105b06aeb98a48f8a6eacab80ba3a467f89fbe31ee5`  
		Last Modified: Tue, 21 Nov 2023 07:14:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3.2` - linux; s390x

```console
$ docker pull couchdb@sha256:21965f0438b454449366375d4c6bfd319e83dec568e9907669ba2b6a1c077563
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (87002806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba071f2f075a8263e2e67f1fc0f844debd3e57242ac3165ff9adcfacf2338049`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Nov 2023 05:05:18 GMT
ADD file:a545f27075704ce13e33e539170d3f47007424d2cc2bea5aecfd2608a5194151 in / 
# Tue, 21 Nov 2023 05:05:22 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:20:22 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 21 Nov 2023 06:20:22 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 21 Nov 2023 06:20:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:20:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 21 Nov 2023 06:20:31 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 21 Nov 2023 06:20:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:20:36 GMT
ENV COUCHDB_VERSION=3.3.2
# Tue, 21 Nov 2023 06:20:36 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 21 Nov 2023 06:20:53 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 21 Nov 2023 06:20:55 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 21 Nov 2023 06:20:55 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 21 Nov 2023 06:20:55 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 21 Nov 2023 06:20:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 21 Nov 2023 06:20:56 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 06:20:56 GMT
VOLUME [/opt/couchdb/data]
# Tue, 21 Nov 2023 06:20:56 GMT
EXPOSE 4369 5984 9100
# Tue, 21 Nov 2023 06:20:56 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b114072f1cab66b7376d690985b12816aebab2e4e41fc170e32f111df27951dc`  
		Last Modified: Tue, 21 Nov 2023 05:10:48 GMT  
		Size: 29.7 MB (29656938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72dba253785a5e917fdd9064f61b676b4080ff3073424ff387308d70579c728b`  
		Last Modified: Tue, 21 Nov 2023 06:21:15 GMT  
		Size: 3.4 KB (3431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a299cd04ea14bbc3034e11001a1ec06dd4b5e1aaa78317dc803570f8a4c6437`  
		Last Modified: Tue, 21 Nov 2023 06:21:15 GMT  
		Size: 5.1 MB (5111719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c684e5bcbb93c8f0c9da5b81b4a1d19274f7ad0c7e3b17eb12cbe45cd2514989`  
		Last Modified: Tue, 21 Nov 2023 06:21:14 GMT  
		Size: 573.6 KB (573635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d916370cd04b7352346fee3edc1ac77bdb9393e24c5bc62c4cb0803a682836`  
		Last Modified: Tue, 21 Nov 2023 06:21:14 GMT  
		Size: 295.1 KB (295096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e602d723a112bfbe3ebaca9b99e2e9636dac8b07c69947311ceb07666d40ed`  
		Last Modified: Tue, 21 Nov 2023 06:21:14 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdbafbeffdc5d29b56e0ccf672e48ead551f49aa23534b4fd9aefcd339587dc5`  
		Last Modified: Tue, 21 Nov 2023 06:21:18 GMT  
		Size: 51.4 MB (51357976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f08f21ade417458e581ec8afdf835c5d165444c0e93fdc330cbd6146af1da3`  
		Last Modified: Tue, 21 Nov 2023 06:21:13 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a4bc9e282fe338ed74c99dbb5cb5777e0ba1a2d068de6e102a8adbb34acc14`  
		Last Modified: Tue, 21 Nov 2023 06:21:13 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c93f5a64665780dfb559adfed9587064e52e00c9c515834a97cf26e3529da9`  
		Last Modified: Tue, 21 Nov 2023 06:21:13 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f6f407505b71a14801c0c71da8d0ce2a85d8c65d58e7998784a75dcde3cfb6`  
		Last Modified: Tue, 21 Nov 2023 06:21:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:dc6bcc8ef7381be4ff0975b27e4cddaafd45bba68c2d5c8f7524f260d62cef93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:3c609bc33e472d4cb0a4ea0b117359bd0c9ed4f0628899131e8344fd13fbe01a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90245671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fff4b56666dbf396fc0b2eedb70c70b8990ccb6dc5d8447206f2243d21c1986c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:46:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 01 Nov 2023 01:46:41 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 01 Nov 2023 01:46:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:46:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 01 Nov 2023 01:46:51 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 01 Nov 2023 01:46:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:46:56 GMT
ENV COUCHDB_VERSION=3.3.2
# Wed, 01 Nov 2023 01:46:56 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 01 Nov 2023 01:47:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 01 Nov 2023 01:47:10 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 01 Nov 2023 01:47:10 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 01 Nov 2023 01:47:11 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 01 Nov 2023 01:47:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 01 Nov 2023 01:47:11 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 01 Nov 2023 01:47:11 GMT
VOLUME [/opt/couchdb/data]
# Wed, 01 Nov 2023 01:47:11 GMT
EXPOSE 4369 5984 9100
# Wed, 01 Nov 2023 01:47:11 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbba1a29bfe2ee9664ccd0caa145b5aa7a5480c276f1c42fd77ac32ef2c440c1`  
		Last Modified: Wed, 01 Nov 2023 01:48:53 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b21d450d3bd9333c8a5efb4081f440607452820e295142168061b2216f3986c`  
		Last Modified: Wed, 01 Nov 2023 01:48:53 GMT  
		Size: 5.2 MB (5226554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c93767e1cbf8a0b2d24469dbe0f750b73d88204210f83f7faa87b8be37dfaa`  
		Last Modified: Wed, 01 Nov 2023 01:48:52 GMT  
		Size: 610.9 KB (610919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24dc783ed2d49dd34054350d1a680091886de94bd264352e835184065e394e64`  
		Last Modified: Wed, 01 Nov 2023 01:48:52 GMT  
		Size: 295.2 KB (295153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8597086eac85cffb9306a84cfa8414bcda5500cb8092b1ba307a38e9e56540f`  
		Last Modified: Wed, 01 Nov 2023 01:48:52 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4fefd748372d68972d6fb14014c7813ac7837a6380b957f3092da518331958`  
		Last Modified: Wed, 01 Nov 2023 01:48:55 GMT  
		Size: 52.7 MB (52687716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ff2441b3a4073bbf88542aaf2d970fd2eb11cc4bd01c846d1245dae6187068`  
		Last Modified: Wed, 01 Nov 2023 01:48:50 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c29c7241d3a11a9dcf62611e3563275d0b24d32fa9f65fb5be837b13ef1cfb4`  
		Last Modified: Wed, 01 Nov 2023 01:48:50 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cacd4b2ce1758697d4898b78068d98430738b73f2f0171222ea8fc970a567603`  
		Last Modified: Wed, 01 Nov 2023 01:48:50 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7254e813570e08d636b0b367fb2dfe8c25dfa8b3a07a24b4dcf9574a9e238270`  
		Last Modified: Wed, 01 Nov 2023 01:48:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:831daf394c7922970580685f1b22701050dd6a16e2f3a494a0cc21d59d232e8a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88692917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb7b80ab6c0be332c785fef11c78605df05520b29c166d4b8419e9ba11b4137d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:52:39 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 21 Nov 2023 07:52:39 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 21 Nov 2023 07:52:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:52:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 21 Nov 2023 07:52:48 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 21 Nov 2023 07:52:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:52:53 GMT
ENV COUCHDB_VERSION=3.3.2
# Tue, 21 Nov 2023 07:52:53 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 21 Nov 2023 07:53:04 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 21 Nov 2023 07:53:05 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 21 Nov 2023 07:53:05 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 21 Nov 2023 07:53:05 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 21 Nov 2023 07:53:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 21 Nov 2023 07:53:06 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 07:53:06 GMT
VOLUME [/opt/couchdb/data]
# Tue, 21 Nov 2023 07:53:06 GMT
EXPOSE 4369 5984 9100
# Tue, 21 Nov 2023 07:53:06 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a831f10e5df507c8f1e02bf16d8431aea07447742165f87bac8012c02082c5c1`  
		Last Modified: Tue, 21 Nov 2023 07:54:32 GMT  
		Size: 3.4 KB (3431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4f74c0ee547299d86d3b6de1a1b677264a77024288fe76a0459fe1596e94b0`  
		Last Modified: Tue, 21 Nov 2023 07:54:31 GMT  
		Size: 5.2 MB (5210800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a278347563aa0aac229a39ef7f2d07a6925c6a95f1eca2dc9335921b7b75f3`  
		Last Modified: Tue, 21 Nov 2023 07:54:31 GMT  
		Size: 567.0 KB (567042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:479409bd9ad96512a7ba2074dabd9869a645ffa5edcc2ed2838022c816bae08d`  
		Last Modified: Tue, 21 Nov 2023 07:54:30 GMT  
		Size: 295.0 KB (295025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb46e8fd7a961878d2567e65d067b58ff68156ff62061cc8a8eb83c963dec48`  
		Last Modified: Tue, 21 Nov 2023 07:54:30 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0693fcb978a2b25d973a958ba01b81f13a42056be06852f67b9267b84065469`  
		Last Modified: Tue, 21 Nov 2023 07:54:32 GMT  
		Size: 52.5 MB (52548491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb62433b69e69906e6e298abde0a0d51dd57cff56e397b5095cca42260b91396`  
		Last Modified: Tue, 21 Nov 2023 07:54:28 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429f575265d6dad0cc72071474dc91d355558fbb8878d15303208499c66db6ba`  
		Last Modified: Tue, 21 Nov 2023 07:54:28 GMT  
		Size: 999.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4dd6cdf208e02f406ff8afb4344c4bbeead85c1af4146cae59fd96374d2b04`  
		Last Modified: Tue, 21 Nov 2023 07:54:28 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759e8a99734a273cc774b1971af710af95d4adc3fbff7de0f6efa32f09aabb04`  
		Last Modified: Tue, 21 Nov 2023 07:54:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:ccf9e925a92c4e47c922173bb8a6541607469de85a3d23b8f709a5b2f9fa4571
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95968231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0d5240fcc3525a7c996865649016d229a3b75d1447c7ade86132d7ede52ffe8`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Nov 2023 04:24:43 GMT
ADD file:b0d18f2d04821eb50d1faecc1a64916f5c63dd386ae71a3b2cb1d6c4aac6e1c4 in / 
# Tue, 21 Nov 2023 04:24:46 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:12:10 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 21 Nov 2023 07:12:12 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 21 Nov 2023 07:12:31 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:12:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 21 Nov 2023 07:12:37 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 21 Nov 2023 07:12:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 07:12:47 GMT
ENV COUCHDB_VERSION=3.3.2
# Tue, 21 Nov 2023 07:12:49 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 21 Nov 2023 07:13:13 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 21 Nov 2023 07:13:17 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 21 Nov 2023 07:13:17 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 21 Nov 2023 07:13:17 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 21 Nov 2023 07:13:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 21 Nov 2023 07:13:20 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 07:13:20 GMT
VOLUME [/opt/couchdb/data]
# Tue, 21 Nov 2023 07:13:20 GMT
EXPOSE 4369 5984 9100
# Tue, 21 Nov 2023 07:13:21 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:60239a74847cd7e9a928353188f3cf096ca8cf648e2b27c765058e169d568fd9`  
		Last Modified: Tue, 21 Nov 2023 04:29:47 GMT  
		Size: 35.3 MB (35293727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f63eed5db2c906b6108908d9dc6976c9a23f1bb19a0e617257decd133e7592d`  
		Last Modified: Tue, 21 Nov 2023 07:14:05 GMT  
		Size: 3.4 KB (3408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:941bb642de45bb343a873e9c819cd85bffe05a010a6da631d1723612f69c794c`  
		Last Modified: Tue, 21 Nov 2023 07:14:04 GMT  
		Size: 6.0 MB (6046203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f2659433b58c3235f1e9085447d55d5c442efc597e42f97dfce11b106d84c0`  
		Last Modified: Tue, 21 Nov 2023 07:14:04 GMT  
		Size: 662.9 KB (662883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d777a7fd59124bb1d1eed56bddee9639f6ea57c6eaf67610a97a4a8c833814e9`  
		Last Modified: Tue, 21 Nov 2023 07:14:03 GMT  
		Size: 295.1 KB (295091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef322b815f454b44be7fc5bbc3f2c179419841031a40a753c25cb71a704158f4`  
		Last Modified: Tue, 21 Nov 2023 07:14:03 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6180ccba02f37081c0d1523baa72b7df6183b2284a575cc84c8f245ed21624fc`  
		Last Modified: Tue, 21 Nov 2023 07:14:07 GMT  
		Size: 53.7 MB (53662909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991739364f41cbdef5c3adb115b1f41c51bbafbd6555e32316cad98f1cae7e54`  
		Last Modified: Tue, 21 Nov 2023 07:14:01 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f539c1a9af058023c294a0b078bb81ec732ba18d3e4c624af45c5e3a877c5dd`  
		Last Modified: Tue, 21 Nov 2023 07:14:01 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27abb88fb75707dd945625a5a2734aa790dcd4330e5d257d13fde86d69630c4`  
		Last Modified: Tue, 21 Nov 2023 07:14:01 GMT  
		Size: 2.2 KB (2232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7837c78696f2a9940c752105b06aeb98a48f8a6eacab80ba3a467f89fbe31ee5`  
		Last Modified: Tue, 21 Nov 2023 07:14:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:21965f0438b454449366375d4c6bfd319e83dec568e9907669ba2b6a1c077563
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (87002806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba071f2f075a8263e2e67f1fc0f844debd3e57242ac3165ff9adcfacf2338049`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 21 Nov 2023 05:05:18 GMT
ADD file:a545f27075704ce13e33e539170d3f47007424d2cc2bea5aecfd2608a5194151 in / 
# Tue, 21 Nov 2023 05:05:22 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:20:22 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 21 Nov 2023 06:20:22 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 21 Nov 2023 06:20:28 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:20:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 21 Nov 2023 06:20:31 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 21 Nov 2023 06:20:36 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:20:36 GMT
ENV COUCHDB_VERSION=3.3.2
# Tue, 21 Nov 2023 06:20:36 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 21 Nov 2023 06:20:53 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 21 Nov 2023 06:20:55 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 21 Nov 2023 06:20:55 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 21 Nov 2023 06:20:55 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 21 Nov 2023 06:20:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 21 Nov 2023 06:20:56 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 06:20:56 GMT
VOLUME [/opt/couchdb/data]
# Tue, 21 Nov 2023 06:20:56 GMT
EXPOSE 4369 5984 9100
# Tue, 21 Nov 2023 06:20:56 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b114072f1cab66b7376d690985b12816aebab2e4e41fc170e32f111df27951dc`  
		Last Modified: Tue, 21 Nov 2023 05:10:48 GMT  
		Size: 29.7 MB (29656938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72dba253785a5e917fdd9064f61b676b4080ff3073424ff387308d70579c728b`  
		Last Modified: Tue, 21 Nov 2023 06:21:15 GMT  
		Size: 3.4 KB (3431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a299cd04ea14bbc3034e11001a1ec06dd4b5e1aaa78317dc803570f8a4c6437`  
		Last Modified: Tue, 21 Nov 2023 06:21:15 GMT  
		Size: 5.1 MB (5111719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c684e5bcbb93c8f0c9da5b81b4a1d19274f7ad0c7e3b17eb12cbe45cd2514989`  
		Last Modified: Tue, 21 Nov 2023 06:21:14 GMT  
		Size: 573.6 KB (573635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d916370cd04b7352346fee3edc1ac77bdb9393e24c5bc62c4cb0803a682836`  
		Last Modified: Tue, 21 Nov 2023 06:21:14 GMT  
		Size: 295.1 KB (295096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e602d723a112bfbe3ebaca9b99e2e9636dac8b07c69947311ceb07666d40ed`  
		Last Modified: Tue, 21 Nov 2023 06:21:14 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdbafbeffdc5d29b56e0ccf672e48ead551f49aa23534b4fd9aefcd339587dc5`  
		Last Modified: Tue, 21 Nov 2023 06:21:18 GMT  
		Size: 51.4 MB (51357976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f08f21ade417458e581ec8afdf835c5d165444c0e93fdc330cbd6146af1da3`  
		Last Modified: Tue, 21 Nov 2023 06:21:13 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a4bc9e282fe338ed74c99dbb5cb5777e0ba1a2d068de6e102a8adbb34acc14`  
		Last Modified: Tue, 21 Nov 2023 06:21:13 GMT  
		Size: 1.0 KB (1001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c93f5a64665780dfb559adfed9587064e52e00c9c515834a97cf26e3529da9`  
		Last Modified: Tue, 21 Nov 2023 06:21:13 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f6f407505b71a14801c0c71da8d0ce2a85d8c65d58e7998784a75dcde3cfb6`  
		Last Modified: Tue, 21 Nov 2023 06:21:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
