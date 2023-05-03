## `couchdb:latest`

```console
$ docker pull couchdb@sha256:9760ef202c43ddfbdc3d8e220353ddef84ba50d1d757508a81e6ca7a6e62eb5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:a78ecf1912d5046be84252e42c87b4ab88898be235ad23388b590870933d9c59
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90226076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4894334bb0e847a86583bb98c2678f2ef00343fe485b0e7a77da57bf72386d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:20:41 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 03 May 2023 20:20:41 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 03 May 2023 20:20:48 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:20:52 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 03 May 2023 20:20:52 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 03 May 2023 20:20:57 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:20:57 GMT
ENV COUCHDB_VERSION=3.3.2
# Wed, 03 May 2023 20:20:57 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 03 May 2023 20:21:10 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 03 May 2023 20:21:10 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 03 May 2023 20:21:10 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 03 May 2023 20:21:10 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 03 May 2023 20:21:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 03 May 2023 20:21:11 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 03 May 2023 20:21:11 GMT
VOLUME [/opt/couchdb/data]
# Wed, 03 May 2023 20:21:11 GMT
EXPOSE 4369 5984 9100
# Wed, 03 May 2023 20:21:11 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22aae57dfaa0a56d12e531052d943db83aef0440c156d6fd9d192f6a1085a270`  
		Last Modified: Wed, 03 May 2023 20:22:47 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b93caf13d63dac0c40ecd2e72ababf04b8014086e33b50ed00159c1332a5ae9`  
		Last Modified: Wed, 03 May 2023 20:22:46 GMT  
		Size: 5.2 MB (5224504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1357c913bae06fc471b1ba29963a41023b367169a33df605c24f688ca19fba6`  
		Last Modified: Wed, 03 May 2023 20:22:46 GMT  
		Size: 610.3 KB (610274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdeea262d51fa2fd0a20a1c0067906a28611ed6d893bbfc07b305a2ad12872bf`  
		Last Modified: Wed, 03 May 2023 20:22:45 GMT  
		Size: 294.4 KB (294388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d29c2f2da0eb28da20c5b6155cda5fe564867522531a0d737f4d5d38d70482`  
		Last Modified: Wed, 03 May 2023 20:22:45 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432ec4176080d53ddfca242d4a6ece47afb37dd56154f2f8d110a611220d81ce`  
		Last Modified: Wed, 03 May 2023 20:22:48 GMT  
		Size: 52.7 MB (52685980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aab316a2c3ce230eb78543d590746289488ab2411ce32ab4a4fff829964f8d6`  
		Last Modified: Wed, 03 May 2023 20:22:43 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9611ebaa996ba274a749a684e1eab5da6f2da79e516eddf4e7aefb4ad17340`  
		Last Modified: Wed, 03 May 2023 20:22:43 GMT  
		Size: 999.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5433ac64532fa5d3c3168cc608f497b8e5988cfe6db3506e072c6954d4fb4e6`  
		Last Modified: Wed, 03 May 2023 20:22:43 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96a1658cb7854650683f232eb1898ae52498d5838b2cdb433e66184970ca793`  
		Last Modified: Wed, 03 May 2023 20:22:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:9744d377ea8891887eb5854020c3a4545c7ef19e8986ee58d32b3cf4040b73b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88673594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fdf7920dfd53b2df52213aee261dd4e41c0549d72f9e343c14cd2b9fcbd5f4f`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:59:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 03 May 2023 17:59:08 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 03 May 2023 17:59:14 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:59:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 03 May 2023 17:59:17 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 03 May 2023 17:59:21 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:59:21 GMT
ENV COUCHDB_VERSION=3.3.2
# Wed, 03 May 2023 17:59:22 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 03 May 2023 17:59:34 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 03 May 2023 17:59:34 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 03 May 2023 17:59:35 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 03 May 2023 17:59:35 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 03 May 2023 17:59:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 03 May 2023 17:59:35 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 03 May 2023 17:59:35 GMT
VOLUME [/opt/couchdb/data]
# Wed, 03 May 2023 17:59:35 GMT
EXPOSE 4369 5984 9100
# Wed, 03 May 2023 17:59:35 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc49e0f227abecd65ff6b6795c3f880303494db817c7e1e18ecda59fc7152e8e`  
		Last Modified: Wed, 03 May 2023 18:00:52 GMT  
		Size: 3.4 KB (3436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0194f60c08f3777da4f834e63630710e50ad01aba6984abe85826ebc49af6a79`  
		Last Modified: Wed, 03 May 2023 18:00:51 GMT  
		Size: 5.2 MB (5209527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63900b96976ba15b59992aaf3958e1823702187a944ded17b4e7e574e5303602`  
		Last Modified: Wed, 03 May 2023 18:00:50 GMT  
		Size: 566.3 KB (566271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baaa51d00fbb637175fe6cd98964622811feb4a21e8ab226b746d44415e72e5f`  
		Last Modified: Wed, 03 May 2023 18:00:50 GMT  
		Size: 294.3 KB (294281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa220909c065252e8254c4d40d57f803dad4012af471289e13ffd7fa688c7eb`  
		Last Modified: Wed, 03 May 2023 18:00:50 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb46de8d7de131610fcf1b61d5a577b86afa7c4840ff37ccec2b17e8498225d2`  
		Last Modified: Wed, 03 May 2023 18:00:52 GMT  
		Size: 52.5 MB (52543335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f937d96179866f5702ff575f8c8f95bbb804136340edde11989b41f079e045d0`  
		Last Modified: Wed, 03 May 2023 18:00:48 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90137057d1382e2128147af431662186fb94c170fd949f3648719510367dcff`  
		Last Modified: Wed, 03 May 2023 18:00:48 GMT  
		Size: 1.0 KB (1002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e79d5751c60bf65d33ec9b49e331aaa0b00505dd7e2dce70dab7d08b91a847b`  
		Last Modified: Wed, 03 May 2023 18:00:48 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4add3ef4c8cc00343e2616e6ac05f104c708b83a23ff11f519c1ccc110d16a17`  
		Last Modified: Wed, 03 May 2023 18:00:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:13c66352ec28fb818402ea6a162b1d26ab57afc84b0959c08626072202a864fd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95962567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e4a23d81c45d81d19aed05a650b92a338f047fdbeff466ec274cce2ce6e48d4`
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
# Tue, 25 Apr 2023 22:16:20 GMT
ENV COUCHDB_VERSION=3.3.2
# Tue, 25 Apr 2023 22:16:21 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Tue, 25 Apr 2023 22:16:47 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Tue, 25 Apr 2023 22:16:49 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Tue, 25 Apr 2023 22:16:49 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Tue, 25 Apr 2023 22:16:49 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Tue, 25 Apr 2023 22:16:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Tue, 25 Apr 2023 22:16:51 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 25 Apr 2023 22:16:51 GMT
VOLUME [/opt/couchdb/data]
# Tue, 25 Apr 2023 22:16:52 GMT
EXPOSE 4369 5984 9100
# Tue, 25 Apr 2023 22:16:52 GMT
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
	-	`sha256:b4a005d1ac9dd4beafe87fd0d6df08fa72f0631b6ab8e23223294f78a242f748`  
		Last Modified: Tue, 25 Apr 2023 22:17:35 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab032b77afd1546e2bf51f362edad19e7661fb6470925250236ef4b8192eed99`  
		Last Modified: Tue, 25 Apr 2023 22:17:42 GMT  
		Size: 53.7 MB (53662597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14465f77288ec304103ebf17b65c6630abe30166373f91e89939385535147e4`  
		Last Modified: Tue, 25 Apr 2023 22:17:33 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5effe25ef84c827ba988a853ea59f8afff941940d15ca66ad41ccba621b99829`  
		Last Modified: Tue, 25 Apr 2023 22:17:33 GMT  
		Size: 1000.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6745b0a9c210274967bf202717f0026edd9102ecab6c433b4164ec8642f72e95`  
		Last Modified: Tue, 25 Apr 2023 22:17:33 GMT  
		Size: 2.2 KB (2233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d7963f0595ab31b467b4da324625d275d24dd8d46f18e3ac2504b8d64ed7c6`  
		Last Modified: Tue, 25 Apr 2023 22:17:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
