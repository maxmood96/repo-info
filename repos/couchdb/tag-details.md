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
$ docker pull couchdb@sha256:5e859acb7b984d2a4cfd4b76544871694e6fabc1574ebe0b9b67638b56905ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:09f0f5ee98dab4f14dfa0948e7959a182f73a5fb28462c0550ede691f518957b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84603754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba66eb6710e44595d821b1c799bcf4d5d092bc6dd3fa42386457618eb2a7434`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 19 Dec 2023 01:21:12 GMT
ADD file:ae5c65eea20f7ddcf93a0aa255b6a08a906ac1a1a65cd2c4b5d1529bf9f6eaf8 in / 
# Tue, 19 Dec 2023 01:21:13 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:48:09 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 Dec 2023 06:48:09 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 19 Dec 2023 06:48:18 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 06:48:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 19 Dec 2023 06:48:22 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 Dec 2023 06:48:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 06:48:50 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 19 Dec 2023 06:48:50 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 19 Dec 2023 06:49:09 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 19 Dec 2023 06:49:10 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 19 Dec 2023 06:49:10 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 19 Dec 2023 06:49:10 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 19 Dec 2023 06:49:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 19 Dec 2023 06:49:10 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 06:49:11 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 Dec 2023 06:49:11 GMT
EXPOSE 4369 5984 9100
# Tue, 19 Dec 2023 06:49:11 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:faac0b3889808c27af96e662a1082eef35772c35dcee1c7334f5f5a22b4149d7`  
		Last Modified: Tue, 19 Dec 2023 01:26:21 GMT  
		Size: 27.2 MB (27188221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7166d4cfe5df555a7729929a6d911ba456e010fabf8a64909232e00ead121bc`  
		Last Modified: Tue, 19 Dec 2023 06:49:59 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4b104d263a43ff5771a1387a20124227ad1f5673c6e0db8dc73314fb604c36`  
		Last Modified: Tue, 19 Dec 2023 06:49:58 GMT  
		Size: 6.7 MB (6704570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d9bda983dd893f88c5ac99cfecbd7008f925b865f7d0684189a6224b0c6de8`  
		Last Modified: Tue, 19 Dec 2023 06:49:57 GMT  
		Size: 1.3 MB (1259894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab85e8861aa6e17e21bcde34afc7866fecfbb5fae39616bcaf635fc5ef14fb24`  
		Last Modified: Tue, 19 Dec 2023 06:49:57 GMT  
		Size: 294.6 KB (294555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89d6563e8c3b10aff1a57fa8336cd27e627cd802ad4080a165dd18fe76bf2ea`  
		Last Modified: Tue, 19 Dec 2023 06:50:11 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d577c04040648c253601c8988f5ce21fd1e69b05720ecc993886b8ce7e92af`  
		Last Modified: Tue, 19 Dec 2023 06:50:15 GMT  
		Size: 49.1 MB (49149495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4bbe2da817b6638fd544411743245fcc3026c70514b44c7f734d25f62b504ed`  
		Last Modified: Tue, 19 Dec 2023 06:50:09 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1cd4ed0cc7ca429112deb3a9c807f11a2716fbeef17f10fdc6061e1153ef19`  
		Last Modified: Tue, 19 Dec 2023 06:50:09 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c48e0c302b1fa8a286b4011d3f6e249602f32f99ec2184ae7eea9d1921e581f`  
		Last Modified: Tue, 19 Dec 2023 06:50:09 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1127283dd5b4a3c263aa5a7ed2b4b10fa99a8b61de96e789daec4a40b8c4da5d`  
		Last Modified: Tue, 19 Dec 2023 06:50:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:87f65845abb0e5646c5810e5a174f781118d75a9ccd77d474781a080424438a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73044917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:297e871e0920e9977f6dbbc4c42b1bc8e5a90b2d12865d3bf99ee2d1a9a35a00`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:39 GMT
ADD file:f60673c303a98b4e4c676e3403bc1b7cb316335aba1202205188176810494c07 in / 
# Tue, 19 Dec 2023 01:41:40 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 07:28:06 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 Dec 2023 07:28:07 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 19 Dec 2023 07:28:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:28:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 19 Dec 2023 07:28:17 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 Dec 2023 07:28:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:28:40 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 19 Dec 2023 07:28:40 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 19 Dec 2023 07:28:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 19 Dec 2023 07:28:52 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 19 Dec 2023 07:28:52 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 19 Dec 2023 07:28:52 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 19 Dec 2023 07:28:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 19 Dec 2023 07:28:53 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 07:28:53 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 Dec 2023 07:28:53 GMT
EXPOSE 4369 5984 9100
# Tue, 19 Dec 2023 07:28:53 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c0b0171eefd1c6d7f85c54d4a609269c9b5e19a0fd8cd787a49c808c6b73cf74`  
		Last Modified: Tue, 19 Dec 2023 01:46:01 GMT  
		Size: 26.0 MB (25969827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ecfca8170b3d9ea74e8fc0136b48f4aa7728fe2b12f8f33ddee284b2de4e3d9`  
		Last Modified: Tue, 19 Dec 2023 07:29:27 GMT  
		Size: 3.4 KB (3442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d096c04d2ea1dd5eb814d6b9b2b4395de466eff95bd757fe014e0c53a5e2f119`  
		Last Modified: Tue, 19 Dec 2023 07:29:26 GMT  
		Size: 6.6 MB (6577654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8acabcd31cbd2c0fe5824dbdac2ed0369915f01859a7125f0d7cdb0fac1bd060`  
		Last Modified: Tue, 19 Dec 2023 07:29:25 GMT  
		Size: 1.2 MB (1164807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac71f5ef55891682bfe632a363760b305012b19c9bd1d92df2481360ed714d9`  
		Last Modified: Tue, 19 Dec 2023 07:29:25 GMT  
		Size: 294.4 KB (294410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497922475afba19882940cd1b1789dc75ecf7d18987e1b3efb5bc2738c3482cb`  
		Last Modified: Tue, 19 Dec 2023 07:29:37 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0482da1b9c7ce2202ce34920dd59f825659df0068a08495b87f2d5cf881eb5d`  
		Last Modified: Tue, 19 Dec 2023 07:29:39 GMT  
		Size: 39.0 MB (39031178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9c9d4aed740283c709a57ac42725fcbb91995e6159ef67fe802bda45ab6192`  
		Last Modified: Tue, 19 Dec 2023 07:29:36 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e052b312ebd40db334457ebd6f6aa49cc2ff029fa7b8e6d0ca0a054c1c21c63`  
		Last Modified: Tue, 19 Dec 2023 07:29:36 GMT  
		Size: 762.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7882a34fe19cc2353cbbe89b9cac530c7f7237a279451fbf70bfc1da5110245d`  
		Last Modified: Tue, 19 Dec 2023 07:29:36 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a79ca1c1c99843fa16adc363a3440fc20dc2b1ed33220c91c5036acd574f0c`  
		Last Modified: Tue, 19 Dec 2023 07:29:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:5e859acb7b984d2a4cfd4b76544871694e6fabc1574ebe0b9b67638b56905ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:09f0f5ee98dab4f14dfa0948e7959a182f73a5fb28462c0550ede691f518957b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84603754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba66eb6710e44595d821b1c799bcf4d5d092bc6dd3fa42386457618eb2a7434`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 19 Dec 2023 01:21:12 GMT
ADD file:ae5c65eea20f7ddcf93a0aa255b6a08a906ac1a1a65cd2c4b5d1529bf9f6eaf8 in / 
# Tue, 19 Dec 2023 01:21:13 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:48:09 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 Dec 2023 06:48:09 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 19 Dec 2023 06:48:18 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 06:48:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 19 Dec 2023 06:48:22 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 Dec 2023 06:48:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 06:48:50 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 19 Dec 2023 06:48:50 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 19 Dec 2023 06:49:09 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 19 Dec 2023 06:49:10 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 19 Dec 2023 06:49:10 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 19 Dec 2023 06:49:10 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 19 Dec 2023 06:49:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 19 Dec 2023 06:49:10 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 06:49:11 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 Dec 2023 06:49:11 GMT
EXPOSE 4369 5984 9100
# Tue, 19 Dec 2023 06:49:11 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:faac0b3889808c27af96e662a1082eef35772c35dcee1c7334f5f5a22b4149d7`  
		Last Modified: Tue, 19 Dec 2023 01:26:21 GMT  
		Size: 27.2 MB (27188221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7166d4cfe5df555a7729929a6d911ba456e010fabf8a64909232e00ead121bc`  
		Last Modified: Tue, 19 Dec 2023 06:49:59 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4b104d263a43ff5771a1387a20124227ad1f5673c6e0db8dc73314fb604c36`  
		Last Modified: Tue, 19 Dec 2023 06:49:58 GMT  
		Size: 6.7 MB (6704570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d9bda983dd893f88c5ac99cfecbd7008f925b865f7d0684189a6224b0c6de8`  
		Last Modified: Tue, 19 Dec 2023 06:49:57 GMT  
		Size: 1.3 MB (1259894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab85e8861aa6e17e21bcde34afc7866fecfbb5fae39616bcaf635fc5ef14fb24`  
		Last Modified: Tue, 19 Dec 2023 06:49:57 GMT  
		Size: 294.6 KB (294555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89d6563e8c3b10aff1a57fa8336cd27e627cd802ad4080a165dd18fe76bf2ea`  
		Last Modified: Tue, 19 Dec 2023 06:50:11 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d577c04040648c253601c8988f5ce21fd1e69b05720ecc993886b8ce7e92af`  
		Last Modified: Tue, 19 Dec 2023 06:50:15 GMT  
		Size: 49.1 MB (49149495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4bbe2da817b6638fd544411743245fcc3026c70514b44c7f734d25f62b504ed`  
		Last Modified: Tue, 19 Dec 2023 06:50:09 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1cd4ed0cc7ca429112deb3a9c807f11a2716fbeef17f10fdc6061e1153ef19`  
		Last Modified: Tue, 19 Dec 2023 06:50:09 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c48e0c302b1fa8a286b4011d3f6e249602f32f99ec2184ae7eea9d1921e581f`  
		Last Modified: Tue, 19 Dec 2023 06:50:09 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1127283dd5b4a3c263aa5a7ed2b4b10fa99a8b61de96e789daec4a40b8c4da5d`  
		Last Modified: Tue, 19 Dec 2023 06:50:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:87f65845abb0e5646c5810e5a174f781118d75a9ccd77d474781a080424438a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73044917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:297e871e0920e9977f6dbbc4c42b1bc8e5a90b2d12865d3bf99ee2d1a9a35a00`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:39 GMT
ADD file:f60673c303a98b4e4c676e3403bc1b7cb316335aba1202205188176810494c07 in / 
# Tue, 19 Dec 2023 01:41:40 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 07:28:06 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 Dec 2023 07:28:07 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 19 Dec 2023 07:28:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:28:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 19 Dec 2023 07:28:17 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 Dec 2023 07:28:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:28:40 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 19 Dec 2023 07:28:40 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 19 Dec 2023 07:28:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 19 Dec 2023 07:28:52 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 19 Dec 2023 07:28:52 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 19 Dec 2023 07:28:52 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 19 Dec 2023 07:28:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 19 Dec 2023 07:28:53 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 07:28:53 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 Dec 2023 07:28:53 GMT
EXPOSE 4369 5984 9100
# Tue, 19 Dec 2023 07:28:53 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c0b0171eefd1c6d7f85c54d4a609269c9b5e19a0fd8cd787a49c808c6b73cf74`  
		Last Modified: Tue, 19 Dec 2023 01:46:01 GMT  
		Size: 26.0 MB (25969827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ecfca8170b3d9ea74e8fc0136b48f4aa7728fe2b12f8f33ddee284b2de4e3d9`  
		Last Modified: Tue, 19 Dec 2023 07:29:27 GMT  
		Size: 3.4 KB (3442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d096c04d2ea1dd5eb814d6b9b2b4395de466eff95bd757fe014e0c53a5e2f119`  
		Last Modified: Tue, 19 Dec 2023 07:29:26 GMT  
		Size: 6.6 MB (6577654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8acabcd31cbd2c0fe5824dbdac2ed0369915f01859a7125f0d7cdb0fac1bd060`  
		Last Modified: Tue, 19 Dec 2023 07:29:25 GMT  
		Size: 1.2 MB (1164807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac71f5ef55891682bfe632a363760b305012b19c9bd1d92df2481360ed714d9`  
		Last Modified: Tue, 19 Dec 2023 07:29:25 GMT  
		Size: 294.4 KB (294410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497922475afba19882940cd1b1789dc75ecf7d18987e1b3efb5bc2738c3482cb`  
		Last Modified: Tue, 19 Dec 2023 07:29:37 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0482da1b9c7ce2202ce34920dd59f825659df0068a08495b87f2d5cf881eb5d`  
		Last Modified: Tue, 19 Dec 2023 07:29:39 GMT  
		Size: 39.0 MB (39031178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9c9d4aed740283c709a57ac42725fcbb91995e6159ef67fe802bda45ab6192`  
		Last Modified: Tue, 19 Dec 2023 07:29:36 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e052b312ebd40db334457ebd6f6aa49cc2ff029fa7b8e6d0ca0a054c1c21c63`  
		Last Modified: Tue, 19 Dec 2023 07:29:36 GMT  
		Size: 762.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7882a34fe19cc2353cbbe89b9cac530c7f7237a279451fbf70bfc1da5110245d`  
		Last Modified: Tue, 19 Dec 2023 07:29:36 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a79ca1c1c99843fa16adc363a3440fc20dc2b1ed33220c91c5036acd574f0c`  
		Last Modified: Tue, 19 Dec 2023 07:29:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:5e859acb7b984d2a4cfd4b76544871694e6fabc1574ebe0b9b67638b56905ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:09f0f5ee98dab4f14dfa0948e7959a182f73a5fb28462c0550ede691f518957b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84603754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba66eb6710e44595d821b1c799bcf4d5d092bc6dd3fa42386457618eb2a7434`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 19 Dec 2023 01:21:12 GMT
ADD file:ae5c65eea20f7ddcf93a0aa255b6a08a906ac1a1a65cd2c4b5d1529bf9f6eaf8 in / 
# Tue, 19 Dec 2023 01:21:13 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:48:09 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 Dec 2023 06:48:09 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 19 Dec 2023 06:48:18 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 06:48:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 19 Dec 2023 06:48:22 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 Dec 2023 06:48:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 06:48:50 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 19 Dec 2023 06:48:50 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 19 Dec 2023 06:49:09 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 19 Dec 2023 06:49:10 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 19 Dec 2023 06:49:10 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 19 Dec 2023 06:49:10 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 19 Dec 2023 06:49:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 19 Dec 2023 06:49:10 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 06:49:11 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 Dec 2023 06:49:11 GMT
EXPOSE 4369 5984 9100
# Tue, 19 Dec 2023 06:49:11 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:faac0b3889808c27af96e662a1082eef35772c35dcee1c7334f5f5a22b4149d7`  
		Last Modified: Tue, 19 Dec 2023 01:26:21 GMT  
		Size: 27.2 MB (27188221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7166d4cfe5df555a7729929a6d911ba456e010fabf8a64909232e00ead121bc`  
		Last Modified: Tue, 19 Dec 2023 06:49:59 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4b104d263a43ff5771a1387a20124227ad1f5673c6e0db8dc73314fb604c36`  
		Last Modified: Tue, 19 Dec 2023 06:49:58 GMT  
		Size: 6.7 MB (6704570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d9bda983dd893f88c5ac99cfecbd7008f925b865f7d0684189a6224b0c6de8`  
		Last Modified: Tue, 19 Dec 2023 06:49:57 GMT  
		Size: 1.3 MB (1259894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab85e8861aa6e17e21bcde34afc7866fecfbb5fae39616bcaf635fc5ef14fb24`  
		Last Modified: Tue, 19 Dec 2023 06:49:57 GMT  
		Size: 294.6 KB (294555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89d6563e8c3b10aff1a57fa8336cd27e627cd802ad4080a165dd18fe76bf2ea`  
		Last Modified: Tue, 19 Dec 2023 06:50:11 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d577c04040648c253601c8988f5ce21fd1e69b05720ecc993886b8ce7e92af`  
		Last Modified: Tue, 19 Dec 2023 06:50:15 GMT  
		Size: 49.1 MB (49149495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4bbe2da817b6638fd544411743245fcc3026c70514b44c7f734d25f62b504ed`  
		Last Modified: Tue, 19 Dec 2023 06:50:09 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1cd4ed0cc7ca429112deb3a9c807f11a2716fbeef17f10fdc6061e1153ef19`  
		Last Modified: Tue, 19 Dec 2023 06:50:09 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c48e0c302b1fa8a286b4011d3f6e249602f32f99ec2184ae7eea9d1921e581f`  
		Last Modified: Tue, 19 Dec 2023 06:50:09 GMT  
		Size: 2.1 KB (2058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1127283dd5b4a3c263aa5a7ed2b4b10fa99a8b61de96e789daec4a40b8c4da5d`  
		Last Modified: Tue, 19 Dec 2023 06:50:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:87f65845abb0e5646c5810e5a174f781118d75a9ccd77d474781a080424438a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73044917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:297e871e0920e9977f6dbbc4c42b1bc8e5a90b2d12865d3bf99ee2d1a9a35a00`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:39 GMT
ADD file:f60673c303a98b4e4c676e3403bc1b7cb316335aba1202205188176810494c07 in / 
# Tue, 19 Dec 2023 01:41:40 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 07:28:06 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 Dec 2023 07:28:07 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 19 Dec 2023 07:28:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:28:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 19 Dec 2023 07:28:17 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 Dec 2023 07:28:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:28:40 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Tue, 19 Dec 2023 07:28:40 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 19 Dec 2023 07:28:52 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 19 Dec 2023 07:28:52 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Tue, 19 Dec 2023 07:28:52 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 19 Dec 2023 07:28:52 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Tue, 19 Dec 2023 07:28:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 19 Dec 2023 07:28:53 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 07:28:53 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 Dec 2023 07:28:53 GMT
EXPOSE 4369 5984 9100
# Tue, 19 Dec 2023 07:28:53 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c0b0171eefd1c6d7f85c54d4a609269c9b5e19a0fd8cd787a49c808c6b73cf74`  
		Last Modified: Tue, 19 Dec 2023 01:46:01 GMT  
		Size: 26.0 MB (25969827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ecfca8170b3d9ea74e8fc0136b48f4aa7728fe2b12f8f33ddee284b2de4e3d9`  
		Last Modified: Tue, 19 Dec 2023 07:29:27 GMT  
		Size: 3.4 KB (3442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d096c04d2ea1dd5eb814d6b9b2b4395de466eff95bd757fe014e0c53a5e2f119`  
		Last Modified: Tue, 19 Dec 2023 07:29:26 GMT  
		Size: 6.6 MB (6577654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8acabcd31cbd2c0fe5824dbdac2ed0369915f01859a7125f0d7cdb0fac1bd060`  
		Last Modified: Tue, 19 Dec 2023 07:29:25 GMT  
		Size: 1.2 MB (1164807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac71f5ef55891682bfe632a363760b305012b19c9bd1d92df2481360ed714d9`  
		Last Modified: Tue, 19 Dec 2023 07:29:25 GMT  
		Size: 294.4 KB (294410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497922475afba19882940cd1b1789dc75ecf7d18987e1b3efb5bc2738c3482cb`  
		Last Modified: Tue, 19 Dec 2023 07:29:37 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0482da1b9c7ce2202ce34920dd59f825659df0068a08495b87f2d5cf881eb5d`  
		Last Modified: Tue, 19 Dec 2023 07:29:39 GMT  
		Size: 39.0 MB (39031178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9c9d4aed740283c709a57ac42725fcbb91995e6159ef67fe802bda45ab6192`  
		Last Modified: Tue, 19 Dec 2023 07:29:36 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e052b312ebd40db334457ebd6f6aa49cc2ff029fa7b8e6d0ca0a054c1c21c63`  
		Last Modified: Tue, 19 Dec 2023 07:29:36 GMT  
		Size: 762.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7882a34fe19cc2353cbbe89b9cac530c7f7237a279451fbf70bfc1da5110245d`  
		Last Modified: Tue, 19 Dec 2023 07:29:36 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a79ca1c1c99843fa16adc363a3440fc20dc2b1ed33220c91c5036acd574f0c`  
		Last Modified: Tue, 19 Dec 2023 07:29:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3`

```console
$ docker pull couchdb@sha256:333505c46793653fe32b009775176678e21af28ef4c73a524d3c5ea73869bdbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:84cc1a070b6ed5057c2539ce9ac0729140211317bfd4c3f8c6af6a972f866fec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.3 MB (90281758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f410d452fcd2d0f4feb71f132b5e4571b9097692fa5ee7bfe55846fffb1b7e3`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:50 GMT
ADD file:bb44d67b03db8efaeb0c4171474f441d14ff35f328f13add32b289fca062fa2f in / 
# Tue, 19 Dec 2023 01:20:50 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:47:07 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 Dec 2023 06:47:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 19 Dec 2023 06:47:16 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 06:47:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 19 Dec 2023 06:47:20 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 Dec 2023 06:47:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 06:47:25 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 19 Dec 2023 06:47:26 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 19 Dec 2023 06:47:39 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 19 Dec 2023 06:47:39 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 19 Dec 2023 06:47:39 GMT
COPY --chown=couchdb:couchdbfile:e5db3ae8229456931b3901d8737d15bbebc21bae345eb60dc63b3edc7a03cfbc in /opt/couchdb/etc/ 
# Tue, 19 Dec 2023 06:47:40 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 19 Dec 2023 06:47:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 19 Dec 2023 06:47:40 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 06:47:40 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 Dec 2023 06:47:40 GMT
EXPOSE 4369 5984 9100
# Tue, 19 Dec 2023 06:47:40 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b5a0d5c14ba9ece1eecd5137c468d9a123372b0af2ed2c8c4446137730c90e5b`  
		Last Modified: Tue, 19 Dec 2023 01:25:40 GMT  
		Size: 31.4 MB (31417873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23f4f070a8876f3b9f2d6536e694e3c435dd993aa89811b93afe3bacdd39de9`  
		Last Modified: Tue, 19 Dec 2023 06:49:26 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e164d5f405aaa07b15f82f3f61b6dbd1cbdc900af32846793054982af6bebe8`  
		Last Modified: Tue, 19 Dec 2023 06:49:25 GMT  
		Size: 5.2 MB (5226586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1dfb4acdebdde82699f2071917a04403c86391036145bbe0ed6d0088656a5c`  
		Last Modified: Tue, 19 Dec 2023 06:49:24 GMT  
		Size: 610.9 KB (610876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1881a771df37f7280e9f36e60d2bf31e1aa682bc897cc46f6048ac2968810ba`  
		Last Modified: Tue, 19 Dec 2023 06:49:24 GMT  
		Size: 295.1 KB (295141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43749cff0c55900c892efc75594212cdfa3d8250f5e733ad3d7992578c888a53`  
		Last Modified: Tue, 19 Dec 2023 06:49:24 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e73826e46a52089a5eb9572f0c4af2e15b3acdb046351f947055ebcf4a9738e8`  
		Last Modified: Tue, 19 Dec 2023 06:49:27 GMT  
		Size: 52.7 MB (52723616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d947e97cc2e724ae946a0a9c7d7acb1c2d25392cadd8502765bf22263aeb7c`  
		Last Modified: Tue, 19 Dec 2023 06:49:22 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7faf03e411f35a5287f56dfccb92efe76a20e4c74a82b7a72829c26175f8213f`  
		Last Modified: Tue, 19 Dec 2023 06:49:22 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0ad2880bdae49be7450333cca29ee638cc9391120e38cc468595f5860297d4`  
		Last Modified: Tue, 19 Dec 2023 06:49:22 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b3dcd02b547118831d71c582730baa714d3fa17b91ec09f7e73ad145fff73d`  
		Last Modified: Tue, 19 Dec 2023 06:49:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:4f81ca5bba0603020a90e870f1bf6d0b3a4ffb76a9f646245025ed216b8a25cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88720261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a042cb3315f4ccd7707c7caba4c1222c0df9996186e17d09d7b7edfd7cf44bd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 07:27:22 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 Dec 2023 07:27:22 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 19 Dec 2023 07:27:29 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:27:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 19 Dec 2023 07:27:31 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 Dec 2023 07:27:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:27:36 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 19 Dec 2023 07:27:36 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 19 Dec 2023 07:27:48 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 19 Dec 2023 07:27:48 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 19 Dec 2023 07:27:48 GMT
COPY --chown=couchdb:couchdbfile:e5db3ae8229456931b3901d8737d15bbebc21bae345eb60dc63b3edc7a03cfbc in /opt/couchdb/etc/ 
# Tue, 19 Dec 2023 07:27:48 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 19 Dec 2023 07:27:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 19 Dec 2023 07:27:49 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 07:27:49 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 Dec 2023 07:27:49 GMT
EXPOSE 4369 5984 9100
# Tue, 19 Dec 2023 07:27:49 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0394d793892daa65ee0bc1540172df5a2856d2c8c1bc13ee7d2a4dff27ef6241`  
		Last Modified: Tue, 19 Dec 2023 07:29:09 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658582a72baaa765a6488cdd18203abba2afbc4eb8d8ca6e1999853a37a888a0`  
		Last Modified: Tue, 19 Dec 2023 07:29:07 GMT  
		Size: 5.2 MB (5210803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d4ac2e2a33e9f495f8acb32a937d4f5429fe8e5e1841de81c9af1393f963468`  
		Last Modified: Tue, 19 Dec 2023 07:29:07 GMT  
		Size: 567.1 KB (567068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2014dad1dedfaca02420d239e0dc675ebda086ff260dcad37b8e054b0e34a1`  
		Last Modified: Tue, 19 Dec 2023 07:29:07 GMT  
		Size: 295.0 KB (295003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d1cb38cb33f9beab7a400eaae36c0b5174c745bfee2a8a5459eb0b5a1fdf85`  
		Last Modified: Tue, 19 Dec 2023 07:29:07 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eecb23deed554222330dc99e93d196bd26b2e922d8d1e7134c9ffc44cf5caeb`  
		Last Modified: Tue, 19 Dec 2023 07:29:09 GMT  
		Size: 52.6 MB (52575650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54b2cb98d9cc8d7f5221c7261be15f031f3adb67fdd3d081ce71fd6a8810a00`  
		Last Modified: Tue, 19 Dec 2023 07:29:05 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8820ac202d74508dc47813bf522d34390023e8814a6667280d08b3863f6ea21`  
		Last Modified: Tue, 19 Dec 2023 07:29:05 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164bc544c6f56c0c1432f03896e396571e3860a597977fca0890d95aae3c7b0c`  
		Last Modified: Tue, 19 Dec 2023 07:29:05 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbc071fea4af87720aa2e669b72e48b40ed5ef900a6064f868aff87a69b3d31`  
		Last Modified: Tue, 19 Dec 2023 07:29:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:753b8176a7aef04da37381fd019c1b2fa6681010e801fc9036e3024e18715ca5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (96006838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d353bf91590bd557c4b0d1b956dfe7e1e6fa4e21024715d5368e4a2c0d40cb23`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 19 Dec 2023 01:22:19 GMT
ADD file:1cb772a6ad8ca6301624db3141029490564de7673bc0f2d4bedb5a1578ea85bd in / 
# Tue, 19 Dec 2023 01:22:21 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:11:17 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 Dec 2023 06:11:20 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 19 Dec 2023 06:11:35 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 06:11:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 19 Dec 2023 06:11:40 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 Dec 2023 06:11:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 06:11:50 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 19 Dec 2023 06:11:51 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 19 Dec 2023 06:12:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 19 Dec 2023 06:12:14 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 19 Dec 2023 06:12:15 GMT
COPY --chown=couchdb:couchdbfile:e5db3ae8229456931b3901d8737d15bbebc21bae345eb60dc63b3edc7a03cfbc in /opt/couchdb/etc/ 
# Tue, 19 Dec 2023 06:12:15 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 19 Dec 2023 06:12:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 19 Dec 2023 06:12:16 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 06:12:17 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 Dec 2023 06:12:17 GMT
EXPOSE 4369 5984 9100
# Tue, 19 Dec 2023 06:12:18 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c9f6fac7f65cfc65b7f8de8bc377b135ca95e45a3246cf2bd1bb90922679553e`  
		Last Modified: Tue, 19 Dec 2023 01:27:11 GMT  
		Size: 35.3 MB (35293807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7577d3224ba65ea8b4b80082d021e485704e429a94e948187c117ef600a0bef`  
		Last Modified: Tue, 19 Dec 2023 06:12:58 GMT  
		Size: 3.4 KB (3417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf8166072b100e13640179c785cd4218b6a2e957ec0e129d0bde7e3834b4dfd`  
		Last Modified: Tue, 19 Dec 2023 06:12:57 GMT  
		Size: 6.0 MB (6046157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c850ad28a78cd961b2a762a88d0451864228709b98ab4b853b228ab4c0800ff7`  
		Last Modified: Tue, 19 Dec 2023 06:12:56 GMT  
		Size: 662.9 KB (662861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95514ebca6987967313a81e9311e31cd8685e3e37bbae279e5d699953a929caf`  
		Last Modified: Tue, 19 Dec 2023 06:12:56 GMT  
		Size: 295.0 KB (295041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c19fb87d01555598a6d01afad8ee27bbe66f165aba43c2b7371a8992104b49`  
		Last Modified: Tue, 19 Dec 2023 06:12:56 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f88c0665db50b85ec902075ad54db3b289b00cc710d7e4392ad1a54d2b30b67`  
		Last Modified: Tue, 19 Dec 2023 06:13:00 GMT  
		Size: 53.7 MB (53701301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4418e5805fb7f6139789891c3e29e2e88f5edc1316d9ba290f5b787f7875b4b4`  
		Last Modified: Tue, 19 Dec 2023 06:12:54 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1d3278e0d5e4065ead7e595ecf8e930b3d840461de896a6764408ca3c217f3`  
		Last Modified: Tue, 19 Dec 2023 06:12:54 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7656c58286888136b4d0eeadba3ffe94124aea9339b8f188674a7d9f08e23bb8`  
		Last Modified: Tue, 19 Dec 2023 06:12:54 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00ff0e342ac6c64e01a93d5a7e5b8141b7afc11273eaf4e03414f7cea7ea31f`  
		Last Modified: Tue, 19 Dec 2023 06:12:54 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; s390x

```console
$ docker pull couchdb@sha256:16a8fda74a542dc4618a4386e0af7bcb801fe40e836bee5719e848484c43a27b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (87021688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eeed791965b3cd821a4d47cf82857981320070fe855468cf1e755d638a106da`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 19 Dec 2023 01:43:11 GMT
ADD file:36a070457acddafcd6cdda22a3c41efcbd4e2b1694831eb74c8143520ebf1cf2 in / 
# Tue, 19 Dec 2023 01:43:14 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 07:57:36 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 Dec 2023 07:57:37 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 19 Dec 2023 07:57:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:57:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 19 Dec 2023 07:57:46 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 Dec 2023 07:57:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:57:51 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 19 Dec 2023 07:57:51 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 19 Dec 2023 07:58:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 19 Dec 2023 07:58:11 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 19 Dec 2023 07:58:11 GMT
COPY --chown=couchdb:couchdbfile:e5db3ae8229456931b3901d8737d15bbebc21bae345eb60dc63b3edc7a03cfbc in /opt/couchdb/etc/ 
# Tue, 19 Dec 2023 07:58:11 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 19 Dec 2023 07:58:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 19 Dec 2023 07:58:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 07:58:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 Dec 2023 07:58:12 GMT
EXPOSE 4369 5984 9100
# Tue, 19 Dec 2023 07:58:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:eff2a4367cf88d5103011eba9299da2b4d173b0bde5dc0455020febf72b9b1c4`  
		Last Modified: Tue, 19 Dec 2023 01:48:08 GMT  
		Size: 29.7 MB (29657006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f975e1c9e4483ac4db84d1e169aa04cc6a63245fa728ee551dfefa22379da07`  
		Last Modified: Tue, 19 Dec 2023 07:58:29 GMT  
		Size: 3.4 KB (3433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b20a5f5aec4009b77b60ee76eddcc4b31e4da278a67ae508d20da5fdfee806`  
		Last Modified: Tue, 19 Dec 2023 07:58:29 GMT  
		Size: 5.1 MB (5111753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c363ab0e5c30a848c591e547cec797a2bb7e09547a9a7352df92046cc6f8d70`  
		Last Modified: Tue, 19 Dec 2023 07:58:28 GMT  
		Size: 573.6 KB (573629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85342303b4df5a705ade33d0371e3942e3bd60e38b82cac5fa98895e162dd171`  
		Last Modified: Tue, 19 Dec 2023 07:58:28 GMT  
		Size: 295.0 KB (295047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc25d72bfae6b4e82f6beed698a54a28df0e716ab54a4348dd8b9d4cee015a7`  
		Last Modified: Tue, 19 Dec 2023 07:58:28 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb3505471c15f489f2d9ebf576e6cdf453fb38a1e33efdeb0377a786468446f`  
		Last Modified: Tue, 19 Dec 2023 07:58:32 GMT  
		Size: 51.4 MB (51376568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4feb6044bfe7237ce49f60f350f83816e95d1a45ab1f1fb7e698c1ac6a4293`  
		Last Modified: Tue, 19 Dec 2023 07:58:27 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db627cf99bb6ab8588279df4502444dfc4cad89ecaf89ea849abb87dcb8ac8e`  
		Last Modified: Tue, 19 Dec 2023 07:58:27 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69209650939b42537987eac0111ad5f1509436e67d7ed206dded4bc862f772d`  
		Last Modified: Tue, 19 Dec 2023 07:58:27 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d40c7bd17dd059fee66b38b642c02a84e7fdd42b26b5b46defd98afb1c41c3f`  
		Last Modified: Tue, 19 Dec 2023 07:58:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:5ba36432c66ede56124f68b9d69cef11114e7444dbb13e0eb2560e9ab292631b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:fc5b9fb424a1f29932290b6fe9534d56d25da640f90af8325cfeccf225225569
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80076408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8751799358a2a661a1cc51181313a85f37683a6bf99209b131e54ec5dba0c26`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 19 Dec 2023 01:21:12 GMT
ADD file:ae5c65eea20f7ddcf93a0aa255b6a08a906ac1a1a65cd2c4b5d1529bf9f6eaf8 in / 
# Tue, 19 Dec 2023 01:21:13 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:48:09 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 Dec 2023 06:48:09 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 19 Dec 2023 06:48:18 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 06:48:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 19 Dec 2023 06:48:22 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 Dec 2023 06:48:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 06:48:29 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 19 Dec 2023 06:48:30 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 19 Dec 2023 06:48:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 19 Dec 2023 06:48:43 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 19 Dec 2023 06:48:44 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 19 Dec 2023 06:48:44 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 19 Dec 2023 06:48:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 19 Dec 2023 06:48:44 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 06:48:44 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 Dec 2023 06:48:44 GMT
EXPOSE 4369 5984 9100
# Tue, 19 Dec 2023 06:48:45 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:faac0b3889808c27af96e662a1082eef35772c35dcee1c7334f5f5a22b4149d7`  
		Last Modified: Tue, 19 Dec 2023 01:26:21 GMT  
		Size: 27.2 MB (27188221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7166d4cfe5df555a7729929a6d911ba456e010fabf8a64909232e00ead121bc`  
		Last Modified: Tue, 19 Dec 2023 06:49:59 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4b104d263a43ff5771a1387a20124227ad1f5673c6e0db8dc73314fb604c36`  
		Last Modified: Tue, 19 Dec 2023 06:49:58 GMT  
		Size: 6.7 MB (6704570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d9bda983dd893f88c5ac99cfecbd7008f925b865f7d0684189a6224b0c6de8`  
		Last Modified: Tue, 19 Dec 2023 06:49:57 GMT  
		Size: 1.3 MB (1259894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab85e8861aa6e17e21bcde34afc7866fecfbb5fae39616bcaf635fc5ef14fb24`  
		Last Modified: Tue, 19 Dec 2023 06:49:57 GMT  
		Size: 294.6 KB (294555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97240f92ce4de6aaad4479bd8c3587c9d99063a2f926fa499931ce4fac4e4275`  
		Last Modified: Tue, 19 Dec 2023 06:49:57 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75ff7bb5081af19002ea75058891e555644d534a6aad9086d653c2190c15aaf`  
		Last Modified: Tue, 19 Dec 2023 06:50:00 GMT  
		Size: 44.6 MB (44622151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc2dc812cf3929e712fb0aef7b198002b614224c04593709dd30335709edec6`  
		Last Modified: Tue, 19 Dec 2023 06:49:55 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25848513c50e1ddbdfbbd7a52c5ac15ef29db26ec37d2aa18bb659fb70e94618`  
		Last Modified: Tue, 19 Dec 2023 06:49:55 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2305e3f1b72672ec9dc4491426e34bc4891ed116d39359e9b4352f7b701b72a5`  
		Last Modified: Tue, 19 Dec 2023 06:49:55 GMT  
		Size: 2.1 KB (2061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0101d064fe5a27e07e1294fe7d8ea2ce5e4a635da0db0ee5caf3a52fcba907c5`  
		Last Modified: Tue, 19 Dec 2023 06:49:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:97de9156908ebef26f452803f1f612b7a5cd37f11095e886f83f55eec242705a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75141341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17a450a8c8c0dcb2cd0f7291c29f6f0b92f273836fbcc79b851874a26de210d1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:39 GMT
ADD file:f60673c303a98b4e4c676e3403bc1b7cb316335aba1202205188176810494c07 in / 
# Tue, 19 Dec 2023 01:41:40 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 07:28:06 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 Dec 2023 07:28:07 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 19 Dec 2023 07:28:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:28:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 19 Dec 2023 07:28:17 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 Dec 2023 07:28:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:28:24 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 19 Dec 2023 07:28:24 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 19 Dec 2023 07:28:36 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 19 Dec 2023 07:28:37 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 19 Dec 2023 07:28:37 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 19 Dec 2023 07:28:37 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 19 Dec 2023 07:28:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 19 Dec 2023 07:28:37 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 07:28:37 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 Dec 2023 07:28:37 GMT
EXPOSE 4369 5984 9100
# Tue, 19 Dec 2023 07:28:37 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c0b0171eefd1c6d7f85c54d4a609269c9b5e19a0fd8cd787a49c808c6b73cf74`  
		Last Modified: Tue, 19 Dec 2023 01:46:01 GMT  
		Size: 26.0 MB (25969827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ecfca8170b3d9ea74e8fc0136b48f4aa7728fe2b12f8f33ddee284b2de4e3d9`  
		Last Modified: Tue, 19 Dec 2023 07:29:27 GMT  
		Size: 3.4 KB (3442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d096c04d2ea1dd5eb814d6b9b2b4395de466eff95bd757fe014e0c53a5e2f119`  
		Last Modified: Tue, 19 Dec 2023 07:29:26 GMT  
		Size: 6.6 MB (6577654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8acabcd31cbd2c0fe5824dbdac2ed0369915f01859a7125f0d7cdb0fac1bd060`  
		Last Modified: Tue, 19 Dec 2023 07:29:25 GMT  
		Size: 1.2 MB (1164807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac71f5ef55891682bfe632a363760b305012b19c9bd1d92df2481360ed714d9`  
		Last Modified: Tue, 19 Dec 2023 07:29:25 GMT  
		Size: 294.4 KB (294410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ca9efb5361e8fea34ab91065f677eb7a29273caac75cdb53c92077b8e30068`  
		Last Modified: Tue, 19 Dec 2023 07:29:25 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9a8234361d499a7ecf3924980f46c835d5ed9c1bc3c6cc5aec816b3ad16f22`  
		Last Modified: Tue, 19 Dec 2023 07:29:26 GMT  
		Size: 41.1 MB (41127603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87a75aa12389f4cf5f7d2d7546d8145114a2b070ff60a7c31abdd7a7079a081`  
		Last Modified: Tue, 19 Dec 2023 07:29:23 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb146e308d234f50254b8b39f7a6d27c661268ef851be0242d1214950115220`  
		Last Modified: Tue, 19 Dec 2023 07:29:23 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a9248c9017e6436518886519e0ecd908915671e480438b58a71db7cce9864a`  
		Last Modified: Tue, 19 Dec 2023 07:29:23 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419495cbe50d01faa265ec5e63a4d3b0ea5489c2a4b877cbb973d0038e6cdf41`  
		Last Modified: Tue, 19 Dec 2023 07:29:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1.2`

```console
$ docker pull couchdb@sha256:5ba36432c66ede56124f68b9d69cef11114e7444dbb13e0eb2560e9ab292631b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1.2` - linux; amd64

```console
$ docker pull couchdb@sha256:fc5b9fb424a1f29932290b6fe9534d56d25da640f90af8325cfeccf225225569
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80076408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8751799358a2a661a1cc51181313a85f37683a6bf99209b131e54ec5dba0c26`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 19 Dec 2023 01:21:12 GMT
ADD file:ae5c65eea20f7ddcf93a0aa255b6a08a906ac1a1a65cd2c4b5d1529bf9f6eaf8 in / 
# Tue, 19 Dec 2023 01:21:13 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:48:09 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 Dec 2023 06:48:09 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 19 Dec 2023 06:48:18 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 06:48:22 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 19 Dec 2023 06:48:22 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 Dec 2023 06:48:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 06:48:29 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 19 Dec 2023 06:48:30 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 19 Dec 2023 06:48:43 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 19 Dec 2023 06:48:43 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 19 Dec 2023 06:48:44 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 19 Dec 2023 06:48:44 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 19 Dec 2023 06:48:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 19 Dec 2023 06:48:44 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 06:48:44 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 Dec 2023 06:48:44 GMT
EXPOSE 4369 5984 9100
# Tue, 19 Dec 2023 06:48:45 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:faac0b3889808c27af96e662a1082eef35772c35dcee1c7334f5f5a22b4149d7`  
		Last Modified: Tue, 19 Dec 2023 01:26:21 GMT  
		Size: 27.2 MB (27188221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7166d4cfe5df555a7729929a6d911ba456e010fabf8a64909232e00ead121bc`  
		Last Modified: Tue, 19 Dec 2023 06:49:59 GMT  
		Size: 3.4 KB (3414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4b104d263a43ff5771a1387a20124227ad1f5673c6e0db8dc73314fb604c36`  
		Last Modified: Tue, 19 Dec 2023 06:49:58 GMT  
		Size: 6.7 MB (6704570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d9bda983dd893f88c5ac99cfecbd7008f925b865f7d0684189a6224b0c6de8`  
		Last Modified: Tue, 19 Dec 2023 06:49:57 GMT  
		Size: 1.3 MB (1259894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab85e8861aa6e17e21bcde34afc7866fecfbb5fae39616bcaf635fc5ef14fb24`  
		Last Modified: Tue, 19 Dec 2023 06:49:57 GMT  
		Size: 294.6 KB (294555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97240f92ce4de6aaad4479bd8c3587c9d99063a2f926fa499931ce4fac4e4275`  
		Last Modified: Tue, 19 Dec 2023 06:49:57 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75ff7bb5081af19002ea75058891e555644d534a6aad9086d653c2190c15aaf`  
		Last Modified: Tue, 19 Dec 2023 06:50:00 GMT  
		Size: 44.6 MB (44622151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc2dc812cf3929e712fb0aef7b198002b614224c04593709dd30335709edec6`  
		Last Modified: Tue, 19 Dec 2023 06:49:55 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25848513c50e1ddbdfbbd7a52c5ac15ef29db26ec37d2aa18bb659fb70e94618`  
		Last Modified: Tue, 19 Dec 2023 06:49:55 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2305e3f1b72672ec9dc4491426e34bc4891ed116d39359e9b4352f7b701b72a5`  
		Last Modified: Tue, 19 Dec 2023 06:49:55 GMT  
		Size: 2.1 KB (2061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0101d064fe5a27e07e1294fe7d8ea2ce5e4a635da0db0ee5caf3a52fcba907c5`  
		Last Modified: Tue, 19 Dec 2023 06:49:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:97de9156908ebef26f452803f1f612b7a5cd37f11095e886f83f55eec242705a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75141341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17a450a8c8c0dcb2cd0f7291c29f6f0b92f273836fbcc79b851874a26de210d1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:39 GMT
ADD file:f60673c303a98b4e4c676e3403bc1b7cb316335aba1202205188176810494c07 in / 
# Tue, 19 Dec 2023 01:41:40 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 07:28:06 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 Dec 2023 07:28:07 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 19 Dec 2023 07:28:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:28:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Tue, 19 Dec 2023 07:28:17 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 Dec 2023 07:28:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:28:24 GMT
ENV COUCHDB_VERSION=3.1.2
# Tue, 19 Dec 2023 07:28:24 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 19 Dec 2023 07:28:36 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 19 Dec 2023 07:28:37 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 19 Dec 2023 07:28:37 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Tue, 19 Dec 2023 07:28:37 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Tue, 19 Dec 2023 07:28:37 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 19 Dec 2023 07:28:37 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 07:28:37 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 Dec 2023 07:28:37 GMT
EXPOSE 4369 5984 9100
# Tue, 19 Dec 2023 07:28:37 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c0b0171eefd1c6d7f85c54d4a609269c9b5e19a0fd8cd787a49c808c6b73cf74`  
		Last Modified: Tue, 19 Dec 2023 01:46:01 GMT  
		Size: 26.0 MB (25969827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ecfca8170b3d9ea74e8fc0136b48f4aa7728fe2b12f8f33ddee284b2de4e3d9`  
		Last Modified: Tue, 19 Dec 2023 07:29:27 GMT  
		Size: 3.4 KB (3442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d096c04d2ea1dd5eb814d6b9b2b4395de466eff95bd757fe014e0c53a5e2f119`  
		Last Modified: Tue, 19 Dec 2023 07:29:26 GMT  
		Size: 6.6 MB (6577654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8acabcd31cbd2c0fe5824dbdac2ed0369915f01859a7125f0d7cdb0fac1bd060`  
		Last Modified: Tue, 19 Dec 2023 07:29:25 GMT  
		Size: 1.2 MB (1164807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac71f5ef55891682bfe632a363760b305012b19c9bd1d92df2481360ed714d9`  
		Last Modified: Tue, 19 Dec 2023 07:29:25 GMT  
		Size: 294.4 KB (294410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ca9efb5361e8fea34ab91065f677eb7a29273caac75cdb53c92077b8e30068`  
		Last Modified: Tue, 19 Dec 2023 07:29:25 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9a8234361d499a7ecf3924980f46c835d5ed9c1bc3c6cc5aec816b3ad16f22`  
		Last Modified: Tue, 19 Dec 2023 07:29:26 GMT  
		Size: 41.1 MB (41127603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87a75aa12389f4cf5f7d2d7546d8145114a2b070ff60a7c31abdd7a7079a081`  
		Last Modified: Tue, 19 Dec 2023 07:29:23 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb146e308d234f50254b8b39f7a6d27c661268ef851be0242d1214950115220`  
		Last Modified: Tue, 19 Dec 2023 07:29:23 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a9248c9017e6436518886519e0ecd908915671e480438b58a71db7cce9864a`  
		Last Modified: Tue, 19 Dec 2023 07:29:23 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419495cbe50d01faa265ec5e63a4d3b0ea5489c2a4b877cbb973d0038e6cdf41`  
		Last Modified: Tue, 19 Dec 2023 07:29:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2`

```console
$ docker pull couchdb@sha256:b6fed2756895c2a121867640a043206eb216653175d711eeaf64d4fd234fc794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:97a8510522e914d2a89b62553f12eb05d78facba87aca42c8c7ad7f217c9cc3e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89747360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7867d5f717af65fbeb432fa0300039806f58bc1c8585c1660fe22fb78a166d8`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:50 GMT
ADD file:bb44d67b03db8efaeb0c4171474f441d14ff35f328f13add32b289fca062fa2f in / 
# Tue, 19 Dec 2023 01:20:50 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:47:07 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 Dec 2023 06:47:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 19 Dec 2023 06:47:16 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 06:47:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 19 Dec 2023 06:47:20 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 Dec 2023 06:47:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 06:47:48 GMT
ENV COUCHDB_VERSION=3.2.3
# Tue, 19 Dec 2023 06:47:49 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 19 Dec 2023 06:48:02 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 19 Dec 2023 06:48:02 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 19 Dec 2023 06:48:03 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 19 Dec 2023 06:48:03 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 19 Dec 2023 06:48:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 19 Dec 2023 06:48:03 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 06:48:03 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 Dec 2023 06:48:03 GMT
EXPOSE 4369 5984 9100
# Tue, 19 Dec 2023 06:48:04 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b5a0d5c14ba9ece1eecd5137c468d9a123372b0af2ed2c8c4446137730c90e5b`  
		Last Modified: Tue, 19 Dec 2023 01:25:40 GMT  
		Size: 31.4 MB (31417873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23f4f070a8876f3b9f2d6536e694e3c435dd993aa89811b93afe3bacdd39de9`  
		Last Modified: Tue, 19 Dec 2023 06:49:26 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e164d5f405aaa07b15f82f3f61b6dbd1cbdc900af32846793054982af6bebe8`  
		Last Modified: Tue, 19 Dec 2023 06:49:25 GMT  
		Size: 5.2 MB (5226586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1dfb4acdebdde82699f2071917a04403c86391036145bbe0ed6d0088656a5c`  
		Last Modified: Tue, 19 Dec 2023 06:49:24 GMT  
		Size: 610.9 KB (610876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1881a771df37f7280e9f36e60d2bf31e1aa682bc897cc46f6048ac2968810ba`  
		Last Modified: Tue, 19 Dec 2023 06:49:24 GMT  
		Size: 295.1 KB (295141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a5f772a9a428e77320db7958f9bec8de6e19d7439a1daecf6a6e370a0dfd71`  
		Last Modified: Tue, 19 Dec 2023 06:49:43 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8503e53b380d12f249eed7e899655ab7f8a3ac7e0f336c80c2f1a6c29cddd85`  
		Last Modified: Tue, 19 Dec 2023 06:49:46 GMT  
		Size: 52.2 MB (52189462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a68e6f5c21ad4eb62ee1bf2db65655af57173cf5db06b8e072f08302a21522a`  
		Last Modified: Tue, 19 Dec 2023 06:49:41 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d51023e201b1f0f0838c8ad3578ea0ea1ce092fef87c23ff52c1880bb44b1fb`  
		Last Modified: Tue, 19 Dec 2023 06:49:41 GMT  
		Size: 999.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2dc6bf45c477ac7473d9b8716ba020b5dbef88ee2843274a50404cd108acdf6`  
		Last Modified: Tue, 19 Dec 2023 06:49:41 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83fe7b8ff6b4bb08b244a8f4414c8e51089ae9f313086a4e953db6f2df395477`  
		Last Modified: Tue, 19 Dec 2023 06:49:41 GMT  
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
$ docker pull couchdb@sha256:1a2d0ec478dd3c43ac8f9ce2bb58ca379844a12826080d4787687b585a2560d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchdb:3.2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:97a8510522e914d2a89b62553f12eb05d78facba87aca42c8c7ad7f217c9cc3e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89747360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7867d5f717af65fbeb432fa0300039806f58bc1c8585c1660fe22fb78a166d8`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:50 GMT
ADD file:bb44d67b03db8efaeb0c4171474f441d14ff35f328f13add32b289fca062fa2f in / 
# Tue, 19 Dec 2023 01:20:50 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:47:07 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 Dec 2023 06:47:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 19 Dec 2023 06:47:16 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 06:47:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 19 Dec 2023 06:47:20 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 Dec 2023 06:47:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 06:47:48 GMT
ENV COUCHDB_VERSION=3.2.3
# Tue, 19 Dec 2023 06:47:49 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 19 Dec 2023 06:48:02 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 19 Dec 2023 06:48:02 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 19 Dec 2023 06:48:03 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 19 Dec 2023 06:48:03 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 19 Dec 2023 06:48:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 19 Dec 2023 06:48:03 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 06:48:03 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 Dec 2023 06:48:03 GMT
EXPOSE 4369 5984 9100
# Tue, 19 Dec 2023 06:48:04 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b5a0d5c14ba9ece1eecd5137c468d9a123372b0af2ed2c8c4446137730c90e5b`  
		Last Modified: Tue, 19 Dec 2023 01:25:40 GMT  
		Size: 31.4 MB (31417873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23f4f070a8876f3b9f2d6536e694e3c435dd993aa89811b93afe3bacdd39de9`  
		Last Modified: Tue, 19 Dec 2023 06:49:26 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e164d5f405aaa07b15f82f3f61b6dbd1cbdc900af32846793054982af6bebe8`  
		Last Modified: Tue, 19 Dec 2023 06:49:25 GMT  
		Size: 5.2 MB (5226586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1dfb4acdebdde82699f2071917a04403c86391036145bbe0ed6d0088656a5c`  
		Last Modified: Tue, 19 Dec 2023 06:49:24 GMT  
		Size: 610.9 KB (610876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1881a771df37f7280e9f36e60d2bf31e1aa682bc897cc46f6048ac2968810ba`  
		Last Modified: Tue, 19 Dec 2023 06:49:24 GMT  
		Size: 295.1 KB (295141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a5f772a9a428e77320db7958f9bec8de6e19d7439a1daecf6a6e370a0dfd71`  
		Last Modified: Tue, 19 Dec 2023 06:49:43 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8503e53b380d12f249eed7e899655ab7f8a3ac7e0f336c80c2f1a6c29cddd85`  
		Last Modified: Tue, 19 Dec 2023 06:49:46 GMT  
		Size: 52.2 MB (52189462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a68e6f5c21ad4eb62ee1bf2db65655af57173cf5db06b8e072f08302a21522a`  
		Last Modified: Tue, 19 Dec 2023 06:49:41 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d51023e201b1f0f0838c8ad3578ea0ea1ce092fef87c23ff52c1880bb44b1fb`  
		Last Modified: Tue, 19 Dec 2023 06:49:41 GMT  
		Size: 999.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2dc6bf45c477ac7473d9b8716ba020b5dbef88ee2843274a50404cd108acdf6`  
		Last Modified: Tue, 19 Dec 2023 06:49:41 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83fe7b8ff6b4bb08b244a8f4414c8e51089ae9f313086a4e953db6f2df395477`  
		Last Modified: Tue, 19 Dec 2023 06:49:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.3`

```console
$ docker pull couchdb@sha256:333505c46793653fe32b009775176678e21af28ef4c73a524d3c5ea73869bdbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `couchdb:3.3` - linux; amd64

```console
$ docker pull couchdb@sha256:84cc1a070b6ed5057c2539ce9ac0729140211317bfd4c3f8c6af6a972f866fec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.3 MB (90281758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f410d452fcd2d0f4feb71f132b5e4571b9097692fa5ee7bfe55846fffb1b7e3`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:50 GMT
ADD file:bb44d67b03db8efaeb0c4171474f441d14ff35f328f13add32b289fca062fa2f in / 
# Tue, 19 Dec 2023 01:20:50 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:47:07 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 Dec 2023 06:47:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 19 Dec 2023 06:47:16 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 06:47:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 19 Dec 2023 06:47:20 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 Dec 2023 06:47:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 06:47:25 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 19 Dec 2023 06:47:26 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 19 Dec 2023 06:47:39 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 19 Dec 2023 06:47:39 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 19 Dec 2023 06:47:39 GMT
COPY --chown=couchdb:couchdbfile:e5db3ae8229456931b3901d8737d15bbebc21bae345eb60dc63b3edc7a03cfbc in /opt/couchdb/etc/ 
# Tue, 19 Dec 2023 06:47:40 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 19 Dec 2023 06:47:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 19 Dec 2023 06:47:40 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 06:47:40 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 Dec 2023 06:47:40 GMT
EXPOSE 4369 5984 9100
# Tue, 19 Dec 2023 06:47:40 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b5a0d5c14ba9ece1eecd5137c468d9a123372b0af2ed2c8c4446137730c90e5b`  
		Last Modified: Tue, 19 Dec 2023 01:25:40 GMT  
		Size: 31.4 MB (31417873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23f4f070a8876f3b9f2d6536e694e3c435dd993aa89811b93afe3bacdd39de9`  
		Last Modified: Tue, 19 Dec 2023 06:49:26 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e164d5f405aaa07b15f82f3f61b6dbd1cbdc900af32846793054982af6bebe8`  
		Last Modified: Tue, 19 Dec 2023 06:49:25 GMT  
		Size: 5.2 MB (5226586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1dfb4acdebdde82699f2071917a04403c86391036145bbe0ed6d0088656a5c`  
		Last Modified: Tue, 19 Dec 2023 06:49:24 GMT  
		Size: 610.9 KB (610876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1881a771df37f7280e9f36e60d2bf31e1aa682bc897cc46f6048ac2968810ba`  
		Last Modified: Tue, 19 Dec 2023 06:49:24 GMT  
		Size: 295.1 KB (295141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43749cff0c55900c892efc75594212cdfa3d8250f5e733ad3d7992578c888a53`  
		Last Modified: Tue, 19 Dec 2023 06:49:24 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e73826e46a52089a5eb9572f0c4af2e15b3acdb046351f947055ebcf4a9738e8`  
		Last Modified: Tue, 19 Dec 2023 06:49:27 GMT  
		Size: 52.7 MB (52723616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d947e97cc2e724ae946a0a9c7d7acb1c2d25392cadd8502765bf22263aeb7c`  
		Last Modified: Tue, 19 Dec 2023 06:49:22 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7faf03e411f35a5287f56dfccb92efe76a20e4c74a82b7a72829c26175f8213f`  
		Last Modified: Tue, 19 Dec 2023 06:49:22 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0ad2880bdae49be7450333cca29ee638cc9391120e38cc468595f5860297d4`  
		Last Modified: Tue, 19 Dec 2023 06:49:22 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b3dcd02b547118831d71c582730baa714d3fa17b91ec09f7e73ad145fff73d`  
		Last Modified: Tue, 19 Dec 2023 06:49:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:4f81ca5bba0603020a90e870f1bf6d0b3a4ffb76a9f646245025ed216b8a25cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88720261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a042cb3315f4ccd7707c7caba4c1222c0df9996186e17d09d7b7edfd7cf44bd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 07:27:22 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 Dec 2023 07:27:22 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 19 Dec 2023 07:27:29 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:27:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 19 Dec 2023 07:27:31 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 Dec 2023 07:27:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:27:36 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 19 Dec 2023 07:27:36 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 19 Dec 2023 07:27:48 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 19 Dec 2023 07:27:48 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 19 Dec 2023 07:27:48 GMT
COPY --chown=couchdb:couchdbfile:e5db3ae8229456931b3901d8737d15bbebc21bae345eb60dc63b3edc7a03cfbc in /opt/couchdb/etc/ 
# Tue, 19 Dec 2023 07:27:48 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 19 Dec 2023 07:27:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 19 Dec 2023 07:27:49 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 07:27:49 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 Dec 2023 07:27:49 GMT
EXPOSE 4369 5984 9100
# Tue, 19 Dec 2023 07:27:49 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0394d793892daa65ee0bc1540172df5a2856d2c8c1bc13ee7d2a4dff27ef6241`  
		Last Modified: Tue, 19 Dec 2023 07:29:09 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658582a72baaa765a6488cdd18203abba2afbc4eb8d8ca6e1999853a37a888a0`  
		Last Modified: Tue, 19 Dec 2023 07:29:07 GMT  
		Size: 5.2 MB (5210803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d4ac2e2a33e9f495f8acb32a937d4f5429fe8e5e1841de81c9af1393f963468`  
		Last Modified: Tue, 19 Dec 2023 07:29:07 GMT  
		Size: 567.1 KB (567068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2014dad1dedfaca02420d239e0dc675ebda086ff260dcad37b8e054b0e34a1`  
		Last Modified: Tue, 19 Dec 2023 07:29:07 GMT  
		Size: 295.0 KB (295003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d1cb38cb33f9beab7a400eaae36c0b5174c745bfee2a8a5459eb0b5a1fdf85`  
		Last Modified: Tue, 19 Dec 2023 07:29:07 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eecb23deed554222330dc99e93d196bd26b2e922d8d1e7134c9ffc44cf5caeb`  
		Last Modified: Tue, 19 Dec 2023 07:29:09 GMT  
		Size: 52.6 MB (52575650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54b2cb98d9cc8d7f5221c7261be15f031f3adb67fdd3d081ce71fd6a8810a00`  
		Last Modified: Tue, 19 Dec 2023 07:29:05 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8820ac202d74508dc47813bf522d34390023e8814a6667280d08b3863f6ea21`  
		Last Modified: Tue, 19 Dec 2023 07:29:05 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164bc544c6f56c0c1432f03896e396571e3860a597977fca0890d95aae3c7b0c`  
		Last Modified: Tue, 19 Dec 2023 07:29:05 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbc071fea4af87720aa2e669b72e48b40ed5ef900a6064f868aff87a69b3d31`  
		Last Modified: Tue, 19 Dec 2023 07:29:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:753b8176a7aef04da37381fd019c1b2fa6681010e801fc9036e3024e18715ca5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (96006838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d353bf91590bd557c4b0d1b956dfe7e1e6fa4e21024715d5368e4a2c0d40cb23`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 19 Dec 2023 01:22:19 GMT
ADD file:1cb772a6ad8ca6301624db3141029490564de7673bc0f2d4bedb5a1578ea85bd in / 
# Tue, 19 Dec 2023 01:22:21 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:11:17 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 Dec 2023 06:11:20 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 19 Dec 2023 06:11:35 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 06:11:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 19 Dec 2023 06:11:40 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 Dec 2023 06:11:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 06:11:50 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 19 Dec 2023 06:11:51 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 19 Dec 2023 06:12:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 19 Dec 2023 06:12:14 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 19 Dec 2023 06:12:15 GMT
COPY --chown=couchdb:couchdbfile:e5db3ae8229456931b3901d8737d15bbebc21bae345eb60dc63b3edc7a03cfbc in /opt/couchdb/etc/ 
# Tue, 19 Dec 2023 06:12:15 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 19 Dec 2023 06:12:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 19 Dec 2023 06:12:16 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 06:12:17 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 Dec 2023 06:12:17 GMT
EXPOSE 4369 5984 9100
# Tue, 19 Dec 2023 06:12:18 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c9f6fac7f65cfc65b7f8de8bc377b135ca95e45a3246cf2bd1bb90922679553e`  
		Last Modified: Tue, 19 Dec 2023 01:27:11 GMT  
		Size: 35.3 MB (35293807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7577d3224ba65ea8b4b80082d021e485704e429a94e948187c117ef600a0bef`  
		Last Modified: Tue, 19 Dec 2023 06:12:58 GMT  
		Size: 3.4 KB (3417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf8166072b100e13640179c785cd4218b6a2e957ec0e129d0bde7e3834b4dfd`  
		Last Modified: Tue, 19 Dec 2023 06:12:57 GMT  
		Size: 6.0 MB (6046157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c850ad28a78cd961b2a762a88d0451864228709b98ab4b853b228ab4c0800ff7`  
		Last Modified: Tue, 19 Dec 2023 06:12:56 GMT  
		Size: 662.9 KB (662861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95514ebca6987967313a81e9311e31cd8685e3e37bbae279e5d699953a929caf`  
		Last Modified: Tue, 19 Dec 2023 06:12:56 GMT  
		Size: 295.0 KB (295041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c19fb87d01555598a6d01afad8ee27bbe66f165aba43c2b7371a8992104b49`  
		Last Modified: Tue, 19 Dec 2023 06:12:56 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f88c0665db50b85ec902075ad54db3b289b00cc710d7e4392ad1a54d2b30b67`  
		Last Modified: Tue, 19 Dec 2023 06:13:00 GMT  
		Size: 53.7 MB (53701301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4418e5805fb7f6139789891c3e29e2e88f5edc1316d9ba290f5b787f7875b4b4`  
		Last Modified: Tue, 19 Dec 2023 06:12:54 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1d3278e0d5e4065ead7e595ecf8e930b3d840461de896a6764408ca3c217f3`  
		Last Modified: Tue, 19 Dec 2023 06:12:54 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7656c58286888136b4d0eeadba3ffe94124aea9339b8f188674a7d9f08e23bb8`  
		Last Modified: Tue, 19 Dec 2023 06:12:54 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00ff0e342ac6c64e01a93d5a7e5b8141b7afc11273eaf4e03414f7cea7ea31f`  
		Last Modified: Tue, 19 Dec 2023 06:12:54 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3` - linux; s390x

```console
$ docker pull couchdb@sha256:16a8fda74a542dc4618a4386e0af7bcb801fe40e836bee5719e848484c43a27b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (87021688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eeed791965b3cd821a4d47cf82857981320070fe855468cf1e755d638a106da`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 19 Dec 2023 01:43:11 GMT
ADD file:36a070457acddafcd6cdda22a3c41efcbd4e2b1694831eb74c8143520ebf1cf2 in / 
# Tue, 19 Dec 2023 01:43:14 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 07:57:36 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 Dec 2023 07:57:37 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 19 Dec 2023 07:57:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:57:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 19 Dec 2023 07:57:46 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 Dec 2023 07:57:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:57:51 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 19 Dec 2023 07:57:51 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 19 Dec 2023 07:58:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 19 Dec 2023 07:58:11 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 19 Dec 2023 07:58:11 GMT
COPY --chown=couchdb:couchdbfile:e5db3ae8229456931b3901d8737d15bbebc21bae345eb60dc63b3edc7a03cfbc in /opt/couchdb/etc/ 
# Tue, 19 Dec 2023 07:58:11 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 19 Dec 2023 07:58:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 19 Dec 2023 07:58:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 07:58:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 Dec 2023 07:58:12 GMT
EXPOSE 4369 5984 9100
# Tue, 19 Dec 2023 07:58:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:eff2a4367cf88d5103011eba9299da2b4d173b0bde5dc0455020febf72b9b1c4`  
		Last Modified: Tue, 19 Dec 2023 01:48:08 GMT  
		Size: 29.7 MB (29657006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f975e1c9e4483ac4db84d1e169aa04cc6a63245fa728ee551dfefa22379da07`  
		Last Modified: Tue, 19 Dec 2023 07:58:29 GMT  
		Size: 3.4 KB (3433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b20a5f5aec4009b77b60ee76eddcc4b31e4da278a67ae508d20da5fdfee806`  
		Last Modified: Tue, 19 Dec 2023 07:58:29 GMT  
		Size: 5.1 MB (5111753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c363ab0e5c30a848c591e547cec797a2bb7e09547a9a7352df92046cc6f8d70`  
		Last Modified: Tue, 19 Dec 2023 07:58:28 GMT  
		Size: 573.6 KB (573629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85342303b4df5a705ade33d0371e3942e3bd60e38b82cac5fa98895e162dd171`  
		Last Modified: Tue, 19 Dec 2023 07:58:28 GMT  
		Size: 295.0 KB (295047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc25d72bfae6b4e82f6beed698a54a28df0e716ab54a4348dd8b9d4cee015a7`  
		Last Modified: Tue, 19 Dec 2023 07:58:28 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb3505471c15f489f2d9ebf576e6cdf453fb38a1e33efdeb0377a786468446f`  
		Last Modified: Tue, 19 Dec 2023 07:58:32 GMT  
		Size: 51.4 MB (51376568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4feb6044bfe7237ce49f60f350f83816e95d1a45ab1f1fb7e698c1ac6a4293`  
		Last Modified: Tue, 19 Dec 2023 07:58:27 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db627cf99bb6ab8588279df4502444dfc4cad89ecaf89ea849abb87dcb8ac8e`  
		Last Modified: Tue, 19 Dec 2023 07:58:27 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69209650939b42537987eac0111ad5f1509436e67d7ed206dded4bc862f772d`  
		Last Modified: Tue, 19 Dec 2023 07:58:27 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d40c7bd17dd059fee66b38b642c02a84e7fdd42b26b5b46defd98afb1c41c3f`  
		Last Modified: Tue, 19 Dec 2023 07:58:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.3.3`

```console
$ docker pull couchdb@sha256:333505c46793653fe32b009775176678e21af28ef4c73a524d3c5ea73869bdbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `couchdb:3.3.3` - linux; amd64

```console
$ docker pull couchdb@sha256:84cc1a070b6ed5057c2539ce9ac0729140211317bfd4c3f8c6af6a972f866fec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.3 MB (90281758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f410d452fcd2d0f4feb71f132b5e4571b9097692fa5ee7bfe55846fffb1b7e3`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:50 GMT
ADD file:bb44d67b03db8efaeb0c4171474f441d14ff35f328f13add32b289fca062fa2f in / 
# Tue, 19 Dec 2023 01:20:50 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:47:07 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 Dec 2023 06:47:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 19 Dec 2023 06:47:16 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 06:47:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 19 Dec 2023 06:47:20 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 Dec 2023 06:47:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 06:47:25 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 19 Dec 2023 06:47:26 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 19 Dec 2023 06:47:39 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 19 Dec 2023 06:47:39 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 19 Dec 2023 06:47:39 GMT
COPY --chown=couchdb:couchdbfile:e5db3ae8229456931b3901d8737d15bbebc21bae345eb60dc63b3edc7a03cfbc in /opt/couchdb/etc/ 
# Tue, 19 Dec 2023 06:47:40 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 19 Dec 2023 06:47:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 19 Dec 2023 06:47:40 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 06:47:40 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 Dec 2023 06:47:40 GMT
EXPOSE 4369 5984 9100
# Tue, 19 Dec 2023 06:47:40 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b5a0d5c14ba9ece1eecd5137c468d9a123372b0af2ed2c8c4446137730c90e5b`  
		Last Modified: Tue, 19 Dec 2023 01:25:40 GMT  
		Size: 31.4 MB (31417873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23f4f070a8876f3b9f2d6536e694e3c435dd993aa89811b93afe3bacdd39de9`  
		Last Modified: Tue, 19 Dec 2023 06:49:26 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e164d5f405aaa07b15f82f3f61b6dbd1cbdc900af32846793054982af6bebe8`  
		Last Modified: Tue, 19 Dec 2023 06:49:25 GMT  
		Size: 5.2 MB (5226586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1dfb4acdebdde82699f2071917a04403c86391036145bbe0ed6d0088656a5c`  
		Last Modified: Tue, 19 Dec 2023 06:49:24 GMT  
		Size: 610.9 KB (610876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1881a771df37f7280e9f36e60d2bf31e1aa682bc897cc46f6048ac2968810ba`  
		Last Modified: Tue, 19 Dec 2023 06:49:24 GMT  
		Size: 295.1 KB (295141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43749cff0c55900c892efc75594212cdfa3d8250f5e733ad3d7992578c888a53`  
		Last Modified: Tue, 19 Dec 2023 06:49:24 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e73826e46a52089a5eb9572f0c4af2e15b3acdb046351f947055ebcf4a9738e8`  
		Last Modified: Tue, 19 Dec 2023 06:49:27 GMT  
		Size: 52.7 MB (52723616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d947e97cc2e724ae946a0a9c7d7acb1c2d25392cadd8502765bf22263aeb7c`  
		Last Modified: Tue, 19 Dec 2023 06:49:22 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7faf03e411f35a5287f56dfccb92efe76a20e4c74a82b7a72829c26175f8213f`  
		Last Modified: Tue, 19 Dec 2023 06:49:22 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0ad2880bdae49be7450333cca29ee638cc9391120e38cc468595f5860297d4`  
		Last Modified: Tue, 19 Dec 2023 06:49:22 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b3dcd02b547118831d71c582730baa714d3fa17b91ec09f7e73ad145fff73d`  
		Last Modified: Tue, 19 Dec 2023 06:49:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:4f81ca5bba0603020a90e870f1bf6d0b3a4ffb76a9f646245025ed216b8a25cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88720261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a042cb3315f4ccd7707c7caba4c1222c0df9996186e17d09d7b7edfd7cf44bd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 07:27:22 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 Dec 2023 07:27:22 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 19 Dec 2023 07:27:29 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:27:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 19 Dec 2023 07:27:31 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 Dec 2023 07:27:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:27:36 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 19 Dec 2023 07:27:36 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 19 Dec 2023 07:27:48 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 19 Dec 2023 07:27:48 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 19 Dec 2023 07:27:48 GMT
COPY --chown=couchdb:couchdbfile:e5db3ae8229456931b3901d8737d15bbebc21bae345eb60dc63b3edc7a03cfbc in /opt/couchdb/etc/ 
# Tue, 19 Dec 2023 07:27:48 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 19 Dec 2023 07:27:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 19 Dec 2023 07:27:49 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 07:27:49 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 Dec 2023 07:27:49 GMT
EXPOSE 4369 5984 9100
# Tue, 19 Dec 2023 07:27:49 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0394d793892daa65ee0bc1540172df5a2856d2c8c1bc13ee7d2a4dff27ef6241`  
		Last Modified: Tue, 19 Dec 2023 07:29:09 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658582a72baaa765a6488cdd18203abba2afbc4eb8d8ca6e1999853a37a888a0`  
		Last Modified: Tue, 19 Dec 2023 07:29:07 GMT  
		Size: 5.2 MB (5210803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d4ac2e2a33e9f495f8acb32a937d4f5429fe8e5e1841de81c9af1393f963468`  
		Last Modified: Tue, 19 Dec 2023 07:29:07 GMT  
		Size: 567.1 KB (567068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2014dad1dedfaca02420d239e0dc675ebda086ff260dcad37b8e054b0e34a1`  
		Last Modified: Tue, 19 Dec 2023 07:29:07 GMT  
		Size: 295.0 KB (295003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d1cb38cb33f9beab7a400eaae36c0b5174c745bfee2a8a5459eb0b5a1fdf85`  
		Last Modified: Tue, 19 Dec 2023 07:29:07 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eecb23deed554222330dc99e93d196bd26b2e922d8d1e7134c9ffc44cf5caeb`  
		Last Modified: Tue, 19 Dec 2023 07:29:09 GMT  
		Size: 52.6 MB (52575650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54b2cb98d9cc8d7f5221c7261be15f031f3adb67fdd3d081ce71fd6a8810a00`  
		Last Modified: Tue, 19 Dec 2023 07:29:05 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8820ac202d74508dc47813bf522d34390023e8814a6667280d08b3863f6ea21`  
		Last Modified: Tue, 19 Dec 2023 07:29:05 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164bc544c6f56c0c1432f03896e396571e3860a597977fca0890d95aae3c7b0c`  
		Last Modified: Tue, 19 Dec 2023 07:29:05 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbc071fea4af87720aa2e669b72e48b40ed5ef900a6064f868aff87a69b3d31`  
		Last Modified: Tue, 19 Dec 2023 07:29:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:753b8176a7aef04da37381fd019c1b2fa6681010e801fc9036e3024e18715ca5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (96006838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d353bf91590bd557c4b0d1b956dfe7e1e6fa4e21024715d5368e4a2c0d40cb23`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 19 Dec 2023 01:22:19 GMT
ADD file:1cb772a6ad8ca6301624db3141029490564de7673bc0f2d4bedb5a1578ea85bd in / 
# Tue, 19 Dec 2023 01:22:21 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:11:17 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 Dec 2023 06:11:20 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 19 Dec 2023 06:11:35 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 06:11:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 19 Dec 2023 06:11:40 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 Dec 2023 06:11:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 06:11:50 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 19 Dec 2023 06:11:51 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 19 Dec 2023 06:12:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 19 Dec 2023 06:12:14 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 19 Dec 2023 06:12:15 GMT
COPY --chown=couchdb:couchdbfile:e5db3ae8229456931b3901d8737d15bbebc21bae345eb60dc63b3edc7a03cfbc in /opt/couchdb/etc/ 
# Tue, 19 Dec 2023 06:12:15 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 19 Dec 2023 06:12:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 19 Dec 2023 06:12:16 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 06:12:17 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 Dec 2023 06:12:17 GMT
EXPOSE 4369 5984 9100
# Tue, 19 Dec 2023 06:12:18 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c9f6fac7f65cfc65b7f8de8bc377b135ca95e45a3246cf2bd1bb90922679553e`  
		Last Modified: Tue, 19 Dec 2023 01:27:11 GMT  
		Size: 35.3 MB (35293807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7577d3224ba65ea8b4b80082d021e485704e429a94e948187c117ef600a0bef`  
		Last Modified: Tue, 19 Dec 2023 06:12:58 GMT  
		Size: 3.4 KB (3417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf8166072b100e13640179c785cd4218b6a2e957ec0e129d0bde7e3834b4dfd`  
		Last Modified: Tue, 19 Dec 2023 06:12:57 GMT  
		Size: 6.0 MB (6046157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c850ad28a78cd961b2a762a88d0451864228709b98ab4b853b228ab4c0800ff7`  
		Last Modified: Tue, 19 Dec 2023 06:12:56 GMT  
		Size: 662.9 KB (662861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95514ebca6987967313a81e9311e31cd8685e3e37bbae279e5d699953a929caf`  
		Last Modified: Tue, 19 Dec 2023 06:12:56 GMT  
		Size: 295.0 KB (295041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c19fb87d01555598a6d01afad8ee27bbe66f165aba43c2b7371a8992104b49`  
		Last Modified: Tue, 19 Dec 2023 06:12:56 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f88c0665db50b85ec902075ad54db3b289b00cc710d7e4392ad1a54d2b30b67`  
		Last Modified: Tue, 19 Dec 2023 06:13:00 GMT  
		Size: 53.7 MB (53701301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4418e5805fb7f6139789891c3e29e2e88f5edc1316d9ba290f5b787f7875b4b4`  
		Last Modified: Tue, 19 Dec 2023 06:12:54 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1d3278e0d5e4065ead7e595ecf8e930b3d840461de896a6764408ca3c217f3`  
		Last Modified: Tue, 19 Dec 2023 06:12:54 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7656c58286888136b4d0eeadba3ffe94124aea9339b8f188674a7d9f08e23bb8`  
		Last Modified: Tue, 19 Dec 2023 06:12:54 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00ff0e342ac6c64e01a93d5a7e5b8141b7afc11273eaf4e03414f7cea7ea31f`  
		Last Modified: Tue, 19 Dec 2023 06:12:54 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3.3` - linux; s390x

```console
$ docker pull couchdb@sha256:16a8fda74a542dc4618a4386e0af7bcb801fe40e836bee5719e848484c43a27b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (87021688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eeed791965b3cd821a4d47cf82857981320070fe855468cf1e755d638a106da`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 19 Dec 2023 01:43:11 GMT
ADD file:36a070457acddafcd6cdda22a3c41efcbd4e2b1694831eb74c8143520ebf1cf2 in / 
# Tue, 19 Dec 2023 01:43:14 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 07:57:36 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 Dec 2023 07:57:37 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 19 Dec 2023 07:57:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:57:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 19 Dec 2023 07:57:46 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 Dec 2023 07:57:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:57:51 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 19 Dec 2023 07:57:51 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 19 Dec 2023 07:58:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 19 Dec 2023 07:58:11 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 19 Dec 2023 07:58:11 GMT
COPY --chown=couchdb:couchdbfile:e5db3ae8229456931b3901d8737d15bbebc21bae345eb60dc63b3edc7a03cfbc in /opt/couchdb/etc/ 
# Tue, 19 Dec 2023 07:58:11 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 19 Dec 2023 07:58:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 19 Dec 2023 07:58:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 07:58:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 Dec 2023 07:58:12 GMT
EXPOSE 4369 5984 9100
# Tue, 19 Dec 2023 07:58:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:eff2a4367cf88d5103011eba9299da2b4d173b0bde5dc0455020febf72b9b1c4`  
		Last Modified: Tue, 19 Dec 2023 01:48:08 GMT  
		Size: 29.7 MB (29657006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f975e1c9e4483ac4db84d1e169aa04cc6a63245fa728ee551dfefa22379da07`  
		Last Modified: Tue, 19 Dec 2023 07:58:29 GMT  
		Size: 3.4 KB (3433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b20a5f5aec4009b77b60ee76eddcc4b31e4da278a67ae508d20da5fdfee806`  
		Last Modified: Tue, 19 Dec 2023 07:58:29 GMT  
		Size: 5.1 MB (5111753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c363ab0e5c30a848c591e547cec797a2bb7e09547a9a7352df92046cc6f8d70`  
		Last Modified: Tue, 19 Dec 2023 07:58:28 GMT  
		Size: 573.6 KB (573629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85342303b4df5a705ade33d0371e3942e3bd60e38b82cac5fa98895e162dd171`  
		Last Modified: Tue, 19 Dec 2023 07:58:28 GMT  
		Size: 295.0 KB (295047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc25d72bfae6b4e82f6beed698a54a28df0e716ab54a4348dd8b9d4cee015a7`  
		Last Modified: Tue, 19 Dec 2023 07:58:28 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb3505471c15f489f2d9ebf576e6cdf453fb38a1e33efdeb0377a786468446f`  
		Last Modified: Tue, 19 Dec 2023 07:58:32 GMT  
		Size: 51.4 MB (51376568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4feb6044bfe7237ce49f60f350f83816e95d1a45ab1f1fb7e698c1ac6a4293`  
		Last Modified: Tue, 19 Dec 2023 07:58:27 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db627cf99bb6ab8588279df4502444dfc4cad89ecaf89ea849abb87dcb8ac8e`  
		Last Modified: Tue, 19 Dec 2023 07:58:27 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69209650939b42537987eac0111ad5f1509436e67d7ed206dded4bc862f772d`  
		Last Modified: Tue, 19 Dec 2023 07:58:27 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d40c7bd17dd059fee66b38b642c02a84e7fdd42b26b5b46defd98afb1c41c3f`  
		Last Modified: Tue, 19 Dec 2023 07:58:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:333505c46793653fe32b009775176678e21af28ef4c73a524d3c5ea73869bdbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:84cc1a070b6ed5057c2539ce9ac0729140211317bfd4c3f8c6af6a972f866fec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.3 MB (90281758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f410d452fcd2d0f4feb71f132b5e4571b9097692fa5ee7bfe55846fffb1b7e3`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:50 GMT
ADD file:bb44d67b03db8efaeb0c4171474f441d14ff35f328f13add32b289fca062fa2f in / 
# Tue, 19 Dec 2023 01:20:50 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:47:07 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 Dec 2023 06:47:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 19 Dec 2023 06:47:16 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 06:47:19 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 19 Dec 2023 06:47:20 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 Dec 2023 06:47:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 06:47:25 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 19 Dec 2023 06:47:26 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 19 Dec 2023 06:47:39 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 19 Dec 2023 06:47:39 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 19 Dec 2023 06:47:39 GMT
COPY --chown=couchdb:couchdbfile:e5db3ae8229456931b3901d8737d15bbebc21bae345eb60dc63b3edc7a03cfbc in /opt/couchdb/etc/ 
# Tue, 19 Dec 2023 06:47:40 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 19 Dec 2023 06:47:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 19 Dec 2023 06:47:40 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 06:47:40 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 Dec 2023 06:47:40 GMT
EXPOSE 4369 5984 9100
# Tue, 19 Dec 2023 06:47:40 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b5a0d5c14ba9ece1eecd5137c468d9a123372b0af2ed2c8c4446137730c90e5b`  
		Last Modified: Tue, 19 Dec 2023 01:25:40 GMT  
		Size: 31.4 MB (31417873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23f4f070a8876f3b9f2d6536e694e3c435dd993aa89811b93afe3bacdd39de9`  
		Last Modified: Tue, 19 Dec 2023 06:49:26 GMT  
		Size: 3.4 KB (3409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e164d5f405aaa07b15f82f3f61b6dbd1cbdc900af32846793054982af6bebe8`  
		Last Modified: Tue, 19 Dec 2023 06:49:25 GMT  
		Size: 5.2 MB (5226586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1dfb4acdebdde82699f2071917a04403c86391036145bbe0ed6d0088656a5c`  
		Last Modified: Tue, 19 Dec 2023 06:49:24 GMT  
		Size: 610.9 KB (610876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1881a771df37f7280e9f36e60d2bf31e1aa682bc897cc46f6048ac2968810ba`  
		Last Modified: Tue, 19 Dec 2023 06:49:24 GMT  
		Size: 295.1 KB (295141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43749cff0c55900c892efc75594212cdfa3d8250f5e733ad3d7992578c888a53`  
		Last Modified: Tue, 19 Dec 2023 06:49:24 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e73826e46a52089a5eb9572f0c4af2e15b3acdb046351f947055ebcf4a9738e8`  
		Last Modified: Tue, 19 Dec 2023 06:49:27 GMT  
		Size: 52.7 MB (52723616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d947e97cc2e724ae946a0a9c7d7acb1c2d25392cadd8502765bf22263aeb7c`  
		Last Modified: Tue, 19 Dec 2023 06:49:22 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7faf03e411f35a5287f56dfccb92efe76a20e4c74a82b7a72829c26175f8213f`  
		Last Modified: Tue, 19 Dec 2023 06:49:22 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0ad2880bdae49be7450333cca29ee638cc9391120e38cc468595f5860297d4`  
		Last Modified: Tue, 19 Dec 2023 06:49:22 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b3dcd02b547118831d71c582730baa714d3fa17b91ec09f7e73ad145fff73d`  
		Last Modified: Tue, 19 Dec 2023 06:49:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:4f81ca5bba0603020a90e870f1bf6d0b3a4ffb76a9f646245025ed216b8a25cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88720261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a042cb3315f4ccd7707c7caba4c1222c0df9996186e17d09d7b7edfd7cf44bd`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 07:27:22 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 Dec 2023 07:27:22 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 19 Dec 2023 07:27:29 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:27:31 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 19 Dec 2023 07:27:31 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 Dec 2023 07:27:35 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:27:36 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 19 Dec 2023 07:27:36 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 19 Dec 2023 07:27:48 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 19 Dec 2023 07:27:48 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 19 Dec 2023 07:27:48 GMT
COPY --chown=couchdb:couchdbfile:e5db3ae8229456931b3901d8737d15bbebc21bae345eb60dc63b3edc7a03cfbc in /opt/couchdb/etc/ 
# Tue, 19 Dec 2023 07:27:48 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 19 Dec 2023 07:27:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 19 Dec 2023 07:27:49 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 07:27:49 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 Dec 2023 07:27:49 GMT
EXPOSE 4369 5984 9100
# Tue, 19 Dec 2023 07:27:49 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0394d793892daa65ee0bc1540172df5a2856d2c8c1bc13ee7d2a4dff27ef6241`  
		Last Modified: Tue, 19 Dec 2023 07:29:09 GMT  
		Size: 3.4 KB (3438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658582a72baaa765a6488cdd18203abba2afbc4eb8d8ca6e1999853a37a888a0`  
		Last Modified: Tue, 19 Dec 2023 07:29:07 GMT  
		Size: 5.2 MB (5210803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d4ac2e2a33e9f495f8acb32a937d4f5429fe8e5e1841de81c9af1393f963468`  
		Last Modified: Tue, 19 Dec 2023 07:29:07 GMT  
		Size: 567.1 KB (567068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c2014dad1dedfaca02420d239e0dc675ebda086ff260dcad37b8e054b0e34a1`  
		Last Modified: Tue, 19 Dec 2023 07:29:07 GMT  
		Size: 295.0 KB (295003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d1cb38cb33f9beab7a400eaae36c0b5174c745bfee2a8a5459eb0b5a1fdf85`  
		Last Modified: Tue, 19 Dec 2023 07:29:07 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eecb23deed554222330dc99e93d196bd26b2e922d8d1e7134c9ffc44cf5caeb`  
		Last Modified: Tue, 19 Dec 2023 07:29:09 GMT  
		Size: 52.6 MB (52575650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54b2cb98d9cc8d7f5221c7261be15f031f3adb67fdd3d081ce71fd6a8810a00`  
		Last Modified: Tue, 19 Dec 2023 07:29:05 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8820ac202d74508dc47813bf522d34390023e8814a6667280d08b3863f6ea21`  
		Last Modified: Tue, 19 Dec 2023 07:29:05 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164bc544c6f56c0c1432f03896e396571e3860a597977fca0890d95aae3c7b0c`  
		Last Modified: Tue, 19 Dec 2023 07:29:05 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbc071fea4af87720aa2e669b72e48b40ed5ef900a6064f868aff87a69b3d31`  
		Last Modified: Tue, 19 Dec 2023 07:29:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:753b8176a7aef04da37381fd019c1b2fa6681010e801fc9036e3024e18715ca5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (96006838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d353bf91590bd557c4b0d1b956dfe7e1e6fa4e21024715d5368e4a2c0d40cb23`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 19 Dec 2023 01:22:19 GMT
ADD file:1cb772a6ad8ca6301624db3141029490564de7673bc0f2d4bedb5a1578ea85bd in / 
# Tue, 19 Dec 2023 01:22:21 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:11:17 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 Dec 2023 06:11:20 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 19 Dec 2023 06:11:35 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 06:11:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 19 Dec 2023 06:11:40 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 Dec 2023 06:11:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 06:11:50 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 19 Dec 2023 06:11:51 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 19 Dec 2023 06:12:12 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 19 Dec 2023 06:12:14 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 19 Dec 2023 06:12:15 GMT
COPY --chown=couchdb:couchdbfile:e5db3ae8229456931b3901d8737d15bbebc21bae345eb60dc63b3edc7a03cfbc in /opt/couchdb/etc/ 
# Tue, 19 Dec 2023 06:12:15 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 19 Dec 2023 06:12:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 19 Dec 2023 06:12:16 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 06:12:17 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 Dec 2023 06:12:17 GMT
EXPOSE 4369 5984 9100
# Tue, 19 Dec 2023 06:12:18 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:c9f6fac7f65cfc65b7f8de8bc377b135ca95e45a3246cf2bd1bb90922679553e`  
		Last Modified: Tue, 19 Dec 2023 01:27:11 GMT  
		Size: 35.3 MB (35293807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7577d3224ba65ea8b4b80082d021e485704e429a94e948187c117ef600a0bef`  
		Last Modified: Tue, 19 Dec 2023 06:12:58 GMT  
		Size: 3.4 KB (3417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf8166072b100e13640179c785cd4218b6a2e957ec0e129d0bde7e3834b4dfd`  
		Last Modified: Tue, 19 Dec 2023 06:12:57 GMT  
		Size: 6.0 MB (6046157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c850ad28a78cd961b2a762a88d0451864228709b98ab4b853b228ab4c0800ff7`  
		Last Modified: Tue, 19 Dec 2023 06:12:56 GMT  
		Size: 662.9 KB (662861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95514ebca6987967313a81e9311e31cd8685e3e37bbae279e5d699953a929caf`  
		Last Modified: Tue, 19 Dec 2023 06:12:56 GMT  
		Size: 295.0 KB (295041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c19fb87d01555598a6d01afad8ee27bbe66f165aba43c2b7371a8992104b49`  
		Last Modified: Tue, 19 Dec 2023 06:12:56 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f88c0665db50b85ec902075ad54db3b289b00cc710d7e4392ad1a54d2b30b67`  
		Last Modified: Tue, 19 Dec 2023 06:13:00 GMT  
		Size: 53.7 MB (53701301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4418e5805fb7f6139789891c3e29e2e88f5edc1316d9ba290f5b787f7875b4b4`  
		Last Modified: Tue, 19 Dec 2023 06:12:54 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1d3278e0d5e4065ead7e595ecf8e930b3d840461de896a6764408ca3c217f3`  
		Last Modified: Tue, 19 Dec 2023 06:12:54 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7656c58286888136b4d0eeadba3ffe94124aea9339b8f188674a7d9f08e23bb8`  
		Last Modified: Tue, 19 Dec 2023 06:12:54 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00ff0e342ac6c64e01a93d5a7e5b8141b7afc11273eaf4e03414f7cea7ea31f`  
		Last Modified: Tue, 19 Dec 2023 06:12:54 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:16a8fda74a542dc4618a4386e0af7bcb801fe40e836bee5719e848484c43a27b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (87021688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eeed791965b3cd821a4d47cf82857981320070fe855468cf1e755d638a106da`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 19 Dec 2023 01:43:11 GMT
ADD file:36a070457acddafcd6cdda22a3c41efcbd4e2b1694831eb74c8143520ebf1cf2 in / 
# Tue, 19 Dec 2023 01:43:14 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 07:57:36 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 19 Dec 2023 07:57:37 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Tue, 19 Dec 2023 07:57:43 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:57:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Tue, 19 Dec 2023 07:57:46 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 19 Dec 2023 07:57:51 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:57:51 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 19 Dec 2023 07:57:51 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 19 Dec 2023 07:58:08 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 19 Dec 2023 07:58:11 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 19 Dec 2023 07:58:11 GMT
COPY --chown=couchdb:couchdbfile:e5db3ae8229456931b3901d8737d15bbebc21bae345eb60dc63b3edc7a03cfbc in /opt/couchdb/etc/ 
# Tue, 19 Dec 2023 07:58:11 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 19 Dec 2023 07:58:12 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 19 Dec 2023 07:58:12 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 07:58:12 GMT
VOLUME [/opt/couchdb/data]
# Tue, 19 Dec 2023 07:58:12 GMT
EXPOSE 4369 5984 9100
# Tue, 19 Dec 2023 07:58:12 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:eff2a4367cf88d5103011eba9299da2b4d173b0bde5dc0455020febf72b9b1c4`  
		Last Modified: Tue, 19 Dec 2023 01:48:08 GMT  
		Size: 29.7 MB (29657006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f975e1c9e4483ac4db84d1e169aa04cc6a63245fa728ee551dfefa22379da07`  
		Last Modified: Tue, 19 Dec 2023 07:58:29 GMT  
		Size: 3.4 KB (3433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b20a5f5aec4009b77b60ee76eddcc4b31e4da278a67ae508d20da5fdfee806`  
		Last Modified: Tue, 19 Dec 2023 07:58:29 GMT  
		Size: 5.1 MB (5111753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c363ab0e5c30a848c591e547cec797a2bb7e09547a9a7352df92046cc6f8d70`  
		Last Modified: Tue, 19 Dec 2023 07:58:28 GMT  
		Size: 573.6 KB (573629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85342303b4df5a705ade33d0371e3942e3bd60e38b82cac5fa98895e162dd171`  
		Last Modified: Tue, 19 Dec 2023 07:58:28 GMT  
		Size: 295.0 KB (295047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc25d72bfae6b4e82f6beed698a54a28df0e716ab54a4348dd8b9d4cee015a7`  
		Last Modified: Tue, 19 Dec 2023 07:58:28 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb3505471c15f489f2d9ebf576e6cdf453fb38a1e33efdeb0377a786468446f`  
		Last Modified: Tue, 19 Dec 2023 07:58:32 GMT  
		Size: 51.4 MB (51376568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4feb6044bfe7237ce49f60f350f83816e95d1a45ab1f1fb7e698c1ac6a4293`  
		Last Modified: Tue, 19 Dec 2023 07:58:27 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db627cf99bb6ab8588279df4502444dfc4cad89ecaf89ea849abb87dcb8ac8e`  
		Last Modified: Tue, 19 Dec 2023 07:58:27 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69209650939b42537987eac0111ad5f1509436e67d7ed206dded4bc862f772d`  
		Last Modified: Tue, 19 Dec 2023 07:58:27 GMT  
		Size: 2.2 KB (2230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d40c7bd17dd059fee66b38b642c02a84e7fdd42b26b5b46defd98afb1c41c3f`  
		Last Modified: Tue, 19 Dec 2023 07:58:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
