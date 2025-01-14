<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchdb`

-	[`couchdb:3`](#couchdb3)
-	[`couchdb:3-nouveau`](#couchdb3-nouveau)
-	[`couchdb:3.3`](#couchdb33)
-	[`couchdb:3.3.3`](#couchdb333)
-	[`couchdb:3.4`](#couchdb34)
-	[`couchdb:3.4-nouveau`](#couchdb34-nouveau)
-	[`couchdb:3.4.2`](#couchdb342)
-	[`couchdb:3.4.2-nouveau`](#couchdb342-nouveau)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:3`

```console
$ docker pull couchdb@sha256:ad6f63289f291bde103fd0d0f23504d5fd12a5de8f75a60317a5e228de64b46f
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
$ docker pull couchdb@sha256:a95224da3fe652bc5231bce9255d8eaeb589827d0f72d3af63b451a977d5f4c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133224084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfac4c6643a4b3f7ad19474bfe23a351fb2ef7912423a2d8df18b64bb62b06e4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94cfb7a0aadd073c09d48219fb9b682a517b3624d3f5d3d8f8a9fc1a29e8009c`  
		Last Modified: Tue, 14 Jan 2025 02:33:57 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f930d3e6857541e62b119727c90cd88062bd426dad1a2d97d3be3076f8e3b67`  
		Last Modified: Tue, 14 Jan 2025 02:33:57 GMT  
		Size: 7.9 MB (7874877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a17f12a2a50718f9ad85af6b6723e44d6a192e1ff473f4732a522ec8bd98938`  
		Last Modified: Tue, 14 Jan 2025 02:33:57 GMT  
		Size: 392.1 KB (392121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed0827d85352c811f94e2f36a99f0aca2954c1916ed3cbe059ddf88f0b45eaf`  
		Last Modified: Tue, 14 Jan 2025 02:33:57 GMT  
		Size: 76.3 KB (76255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa19dc7b250209e550ba9b11bc9680d9410a6a9c0e2c13adea5665d884edd9c5`  
		Last Modified: Tue, 14 Jan 2025 02:33:58 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc18312dcc63d53dded55cf2cea496f3449067e99317cb4a89522ca1cc9a7450`  
		Last Modified: Tue, 14 Jan 2025 02:33:59 GMT  
		Size: 96.7 MB (96662990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f883cb58292b7ed9110ffc0433e5b0c1545f164c765c031c7be05e154b863e4d`  
		Last Modified: Tue, 14 Jan 2025 02:33:58 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526420ad699c75c6d9f69f5926025f00ab7100ece6c2dc37f273a1684f3b4b71`  
		Last Modified: Tue, 14 Jan 2025 02:33:58 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18de8b09dd22f62475825a280b055d48deb17fe98b6e0cf3ffbb5291c66fe9c0`  
		Last Modified: Tue, 14 Jan 2025 02:33:58 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518a54d8eb18501bef8d2fe210909f87531c9ffa7b22cba9a32a19c253fbacf3`  
		Last Modified: Tue, 14 Jan 2025 02:33:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:6c7ac18b8bcad378884fa77920ec07987f7b8e7c139b2330af775618db4b18b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aac88a74b4468832ebae2de5148a13f5bcbea9a5049b4aff2914c15c8cbee3e7`

```dockerfile
```

-	Layers:
	-	`sha256:5fea47f279cfc6471eb29a3494dafe55bd603778641c6f55bf3557117ac8fa23`  
		Last Modified: Tue, 14 Jan 2025 02:33:57 GMT  
		Size: 3.9 MB (3933559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:098120b0ea4b9d34982ad821cf9ad78042b1755faffdc830b6568986b516d119`  
		Last Modified: Tue, 14 Jan 2025 02:33:57 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:33ad9d3878354339233afe53bb87df412283410b29708a7ca796f9ac07f8b621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132524949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414f1bc82926f249cbb136cfcfc223d28a194d2a83571874ab475e0fd4e4bbf1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a53b506eb957ed2ca989730c18ca42f6e0128157e3b16e04b417d5e3f6a46f`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0784cd6960fabd09529a3b70371d1a31ff9aec79c20d3905d9fbc1a2691c796`  
		Last Modified: Tue, 14 Jan 2025 07:04:10 GMT  
		Size: 7.7 MB (7654466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79f2c1109f6989057dfe173d7350181a4d2c6c3094af18ca942f929b5893b99`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 348.9 KB (348911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d118af51ca1a98ff6c7e8640d57cc57f54bf619a7beef5cfe3f06f5d8299b7`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 76.2 KB (76219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3f6188d465363a65faca581e7a29deff62119c7229c06b69dee041e921beff`  
		Last Modified: Tue, 14 Jan 2025 07:04:10 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4080fca21b251df01a293a38872fbe036647cd75dc3dc3d41eeacdcdc9f11e6`  
		Last Modified: Tue, 14 Jan 2025 07:04:13 GMT  
		Size: 96.4 MB (96398891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7570c55d2fc3d036f3606315986bce629111b93b08d0c34f0d640c69858cf107`  
		Last Modified: Tue, 14 Jan 2025 07:04:10 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93840e26080be7ccca7b1d4b3b6eb7444f77b3ce0c1dc501a7758bd2dddd794`  
		Last Modified: Tue, 14 Jan 2025 07:04:11 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349e54346d5fb87fe0546b92feeb3c137da315280a58ed267d31248215cee47c`  
		Last Modified: Tue, 14 Jan 2025 07:04:11 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0da7757a845ae5fd2495cc47db1219d3f9fa2fe4ce5b77dc66d72978d710e60`  
		Last Modified: Tue, 14 Jan 2025 07:04:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:81d65dd5d6ce19f884c69e8e6f10a4bdeee710be6407fc88a62f4599fdd5733a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544e391940d4445a1238cc81cff3eb9c691a770fc7915e710bf9f5799eefb829`

```dockerfile
```

-	Layers:
	-	`sha256:2faae1cf4e6c027422c66213a29885c6bea7c0675ebb0d7bc08679fc799cd5b4`  
		Last Modified: Tue, 14 Jan 2025 07:04:10 GMT  
		Size: 3.9 MB (3933852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e1b443faafdd6eb68584662f9aa0484863d3df8417e5bcb83deb538bcc5d8a2`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 32.0 KB (31970 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; s390x

```console
$ docker pull couchdb@sha256:c7e8d9e60dd0b23c1056e442f4e77c5781760cbea38e8fce29a80d5b907de056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129974576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0363ee9a1846275ab27cddc8292a5a6b0f512431ff9fa5318572c97040e8489`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796a06006ae38898ecb1581ebb6cb4522846078d5d7e8f8a2e300f972b51c50e`  
		Last Modified: Tue, 14 Jan 2025 05:03:14 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b027cea55a6bf96e67067e29306356b85485b1a314f72e2e2b84021d74d438f5`  
		Last Modified: Tue, 14 Jan 2025 05:03:14 GMT  
		Size: 7.4 MB (7388033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0735d11a8ad97f7a3f4b5cd4a2e5151328a005823fc219dd215c12aedeeb40f0`  
		Last Modified: Tue, 14 Jan 2025 05:03:14 GMT  
		Size: 355.7 KB (355663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6798c4ab25b5da5c70c4676230299a997c8fd1bfdcc8016b59d003a893466ab6`  
		Last Modified: Tue, 14 Jan 2025 05:03:14 GMT  
		Size: 76.4 KB (76363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f29ed5c6190b78c2ed8c0b5c8743ee9f67379bbed44eb54bd315e81a4d9aa21`  
		Last Modified: Tue, 14 Jan 2025 05:03:14 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6727b45b83dbfd16f7e25fabdd0c2dd979f1cd06056f045e211feec7f92c2eb2`  
		Last Modified: Tue, 14 Jan 2025 05:03:17 GMT  
		Size: 95.3 MB (95290347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa97288a42496b175156cccac188a3d05f71ef0442314740580d1da3404d5c9d`  
		Last Modified: Tue, 14 Jan 2025 05:03:15 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a531d6bae6d742f8280a170293a174fe348a43b08458c657c84520debf3a2b70`  
		Last Modified: Tue, 14 Jan 2025 05:03:15 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9ca4d8382089804dbaaa44ab24ea6b942fb920923799edc9c648305a60b10c`  
		Last Modified: Tue, 14 Jan 2025 05:03:15 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427c2f29f12e371e9f4bd0aa897ee7095a446affae5f5b5689ed1360429ffed8`  
		Last Modified: Tue, 14 Jan 2025 05:03:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:a5fe57a60ee9573da34f87eaa5edf04c6a94bdfc65c2a737b90c524f7bef97b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b07a080c2feda06310e3d6d790244bfd6a0a0ec160960bbf705453b4a3755ef`

```dockerfile
```

-	Layers:
	-	`sha256:f20e458946d34c50b0a1347b65b4f0672a969222c8d2b83d6ebf5eb589155013`  
		Last Modified: Tue, 14 Jan 2025 05:03:14 GMT  
		Size: 3.9 MB (3932647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0d8622b49e2f849721c02848b0f030134f69a3aa2f654e69ad45577609a701c`  
		Last Modified: Tue, 14 Jan 2025 05:03:14 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:219375f533b07b6e0b284d0671f9783533d2ca2b1ba79b6c3fb4c4cfb811c299
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:9f157b7df804abcc1933c619722da373104834a327280c342147b08afd7252f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155519664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:467a3d123beefa4fdb65757d06376befaeb709d7d85a2ab331b5ffb69a491630`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401f19b00195b76f3e0327677012339b9ffe735976f9a0cc895ec8c96ba1049d`  
		Last Modified: Tue, 14 Jan 2025 02:34:06 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00956253f209377e98ec5aced7d1a8e5a8ecc9ebc105c29b4289c093be0205b`  
		Last Modified: Tue, 14 Jan 2025 02:34:06 GMT  
		Size: 7.9 MB (7874882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc4abb3ee0a71a4283c1ab0803eef1092db98081b80a5b6a0563cf8b76b2e4d`  
		Last Modified: Tue, 14 Jan 2025 02:34:07 GMT  
		Size: 77.3 MB (77284529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40c6a8e7237ef159fe15a0213639f4aaa63e3e4549ef6289f92c26ba5f18444`  
		Last Modified: Tue, 14 Jan 2025 02:34:06 GMT  
		Size: 415.0 KB (414955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dc361a846175db20b63927cb3924b56aeaeca552509f763f67965c1efb0d1c`  
		Last Modified: Tue, 14 Jan 2025 02:34:06 GMT  
		Size: 99.3 KB (99278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a333b9a57418ecfb361ed17a6a0877cb00070aa9f945dc2f284dcfee1914a6`  
		Last Modified: Tue, 14 Jan 2025 02:34:06 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d7487a36f127c29a998687e7904af7341ff1dcd5c443b78ba5a1092e74f0f3`  
		Last Modified: Tue, 14 Jan 2025 02:34:08 GMT  
		Size: 41.6 MB (41631728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e0ef7e407a6804703e784014daa95ab53996cab851d7b005d22cdf667ba855`  
		Last Modified: Tue, 14 Jan 2025 02:34:07 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:a2a1a6ad56e693f00305dfc24564be5de95f80e454b407dbecb3db3141688df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3486620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb899444b5a962775af77b72f86b74b6981b2f8340facf171cfff057eba4bbf1`

```dockerfile
```

-	Layers:
	-	`sha256:14a5a9d04a0c493c240fae7730b5416345468555258b2aa957f00292b635cdb0`  
		Last Modified: Tue, 14 Jan 2025 02:34:06 GMT  
		Size: 3.5 MB (3462056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1a8f4d197d74e81bf5cb9f92edb6085e00d72680d7b07f9ef96c9993cc11221`  
		Last Modified: Tue, 14 Jan 2025 02:34:06 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:ef7c562863a9fb584cc36263dc82db193a4a5c3956927ae78e18f702c0c5518e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.3 MB (154278229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b719cad0c7b5fdbfdbbac6dcb7a1e2ebde3550a3fe03266cf60522f6be67bab3`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79173b3fddb7da2629dd339e0d53b403ea8827bcbd9b247d684b58d32dff7cbf`  
		Last Modified: Tue, 14 Jan 2025 07:05:12 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31829078e1f4de67fcedf6a2d2d8ca1872f489122c7b4bcfa3cd33532c8cb239`  
		Last Modified: Tue, 14 Jan 2025 07:05:12 GMT  
		Size: 7.7 MB (7654485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3369295dc500f95559ea4509a427d2c0a4ee1c8ad2b7a79ee1dc560350241f77`  
		Last Modified: Tue, 14 Jan 2025 07:05:14 GMT  
		Size: 76.6 MB (76582294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e5bbcf4591afaea2d2cdc136dc489080dd97d81c24bd3ccbe400297114b51b`  
		Last Modified: Tue, 14 Jan 2025 07:05:12 GMT  
		Size: 371.7 KB (371693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acdad20d9a721bac2eb158329512906baee9555218f01a8e6ff0f9275510c66`  
		Last Modified: Tue, 14 Jan 2025 07:05:13 GMT  
		Size: 99.2 KB (99208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e627f9bf3e789b44c13cb9953004b89c6d68b322ee687562fe9fb76268a2d868`  
		Last Modified: Tue, 14 Jan 2025 07:05:13 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebeb5aa1e3f7f6837e61861bc4d688a7cb0e40daf66afe7b53355998b6c50ed`  
		Last Modified: Tue, 14 Jan 2025 07:05:14 GMT  
		Size: 41.5 MB (41527641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10a636108d2adc58e1f2c66283165d3226827a0d533ede0055e897d2464c6ed`  
		Last Modified: Tue, 14 Jan 2025 07:05:14 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:80be29eb1df008c822ee482e3954caa2ef94c11a5a1950dd74dbbaa0c6ace91a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3485478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071743ecadfba0fe3591807a89eb13c2932c9c451dc0d4b7924bb78aef478550`

```dockerfile
```

-	Layers:
	-	`sha256:c09558bcbcbf4d95c177b3cde1b9c16427e89ea9acbaf37de09ff936af7f2e77`  
		Last Modified: Tue, 14 Jan 2025 07:05:12 GMT  
		Size: 3.5 MB (3460732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1295fd7d68dfa423f317cb0bff79f1b1008e1459b1398163e931f34e6ccd895d`  
		Last Modified: Tue, 14 Jan 2025 07:05:12 GMT  
		Size: 24.7 KB (24746 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:70e854e48366f50062fe118022844c8125c1ee9307dfa4a899f39c661bea687c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149143062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0dc69c7c10538bf592fbad114bdc96969daf978a25d2339a56d350fe8ec2ce`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59eb9e34d805c91cbb6a777786054384ca5163a44adf355f562791cd57112727`  
		Last Modified: Tue, 14 Jan 2025 05:06:15 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72b3649e7568c38e8dc24f73e32d3e465865f019800342563581fe889fefc29`  
		Last Modified: Tue, 14 Jan 2025 05:06:16 GMT  
		Size: 7.4 MB (7388037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0d623f869fab1ed1b455344ac554f62617dd4a261427922f6b40763302dbbf`  
		Last Modified: Tue, 14 Jan 2025 05:06:17 GMT  
		Size: 73.1 MB (73065000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbbabbad5fba4b48ee2e9985e834dc26b68b7bd7e2c241cd33329010b1de583`  
		Last Modified: Tue, 14 Jan 2025 05:06:15 GMT  
		Size: 378.1 KB (378077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb882edbd68f219460fed3d76efd8d1b02ea6eeb91b88f4478d814abb1cb785f`  
		Last Modified: Tue, 14 Jan 2025 05:06:16 GMT  
		Size: 99.5 KB (99453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac8ff24b5596d40fbafc84ef2c075a634398df269e7f45160322b0a919fa96d`  
		Last Modified: Tue, 14 Jan 2025 05:06:16 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722810c372d4d7cc26207ca1af3be8e8aff57f515d108689fbb17825fad61a58`  
		Last Modified: Tue, 14 Jan 2025 05:06:17 GMT  
		Size: 41.4 MB (41351879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf4e49508aa7ee5296523f9f5b4b6dfbce8441995644a16c4c782ebf7e52ef1`  
		Last Modified: Tue, 14 Jan 2025 05:06:17 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:df7142ee8126c2074cbb8b05bc9de19425070b489604fbec2e24911f6e5d3452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3480041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1886209ac83e9c5d9023aa81b789998a7114e893017d719f32a25a50e94393a`

```dockerfile
```

-	Layers:
	-	`sha256:ec7fcf2e4eaaf1a58fe669cb770e5031e3f6dcb362b566d4f6ac72a409689cf2`  
		Last Modified: Tue, 14 Jan 2025 05:06:16 GMT  
		Size: 3.5 MB (3455477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:718a2716cf1a595efbfe017fdac9f821b2107e9b1b090958af71ceb5964e1534`  
		Last Modified: Tue, 14 Jan 2025 05:06:15 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.3`

```console
$ docker pull couchdb@sha256:779634db41d96ceb70622ea2d6366cf1735e5e0fae31a2273334bfb1e77b7e4d
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
$ docker pull couchdb@sha256:544976afdc75b72fca21564bfe4e05c3a54cf45153303ebf4bae2eb49efa41c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96712023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d59155283197de1d7f0407121faac7e5bd064bdc65c553115bd607f6745734`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e222e6ec445c670b44803406ec6d47484e45c38e87d9c2efa7a1d9303fba85a`  
		Last Modified: Tue, 14 Jan 2025 02:34:00 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d435c3ec7540aa7a7f6545aa659c02a9aed5c43390738654dc89324a15a0ba2f`  
		Last Modified: Tue, 14 Jan 2025 02:34:00 GMT  
		Size: 7.9 MB (7874923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17965acb8b2972226d4a3b2f6affc3e953024737c8118488ed39c5428eb8fdfb`  
		Last Modified: Tue, 14 Jan 2025 02:34:00 GMT  
		Size: 392.1 KB (392135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b48c12b2831723d23e626a4fcea9eb249f1d3334ea07adf99ddc159a47af1c4`  
		Last Modified: Tue, 14 Jan 2025 02:34:00 GMT  
		Size: 76.3 KB (76269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ad2b148ecd8acb886cbce4658ae367e9972c9f7bff90926598c9d8d8f2a058`  
		Last Modified: Tue, 14 Jan 2025 02:34:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06389e024c2d1f6e65152e0c37c28b706fd60e286ce76f7814db62ef6bcdf1ea`  
		Last Modified: Tue, 14 Jan 2025 02:34:02 GMT  
		Size: 60.2 MB (60150853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbddd212eec4a555f9faa530e669535e08c2072a7268cf8d040496f6855a83c`  
		Last Modified: Tue, 14 Jan 2025 02:34:01 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4234039500c108c2658677cbdf2615b19d71eb37eb5dfe567fd939095463a07`  
		Last Modified: Tue, 14 Jan 2025 02:34:01 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c77b84a2fefe8b1b04733755240970fef919f762d63055bc3339a64107d3512`  
		Last Modified: Tue, 14 Jan 2025 02:34:02 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f6f8d10bddfddf19515ca7fbc678be73c7dd93de9ba7b60b7d82dd903d25f1`  
		Last Modified: Tue, 14 Jan 2025 02:34:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:e70e3a79a9c3d4eb25752ced13399a166212ce4508bca27f2be371466040d47b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3766030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c32100cdc6579b90d34673118940c812a8b482b373cb82c26d93c83e664b0d5a`

```dockerfile
```

-	Layers:
	-	`sha256:43102d76c6ec7e317538a919e0ace34cf37f9ae1cb168280106e908e1be78e61`  
		Last Modified: Tue, 14 Jan 2025 02:34:01 GMT  
		Size: 3.7 MB (3734838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4094ce5973798e57689d4c5fb28f540b2a7c52279a17ac80a1356af266daf400`  
		Last Modified: Tue, 14 Jan 2025 02:34:00 GMT  
		Size: 31.2 KB (31192 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:c0bb87f69d46b18ec45cbcf834192896e3e859db5a46d877be6d100e0f2623dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96060414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d8092deae5348ef21718fe3fcbb35c16a1c8d64b135f940c0d25846069883c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a53b506eb957ed2ca989730c18ca42f6e0128157e3b16e04b417d5e3f6a46f`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0784cd6960fabd09529a3b70371d1a31ff9aec79c20d3905d9fbc1a2691c796`  
		Last Modified: Tue, 14 Jan 2025 07:04:10 GMT  
		Size: 7.7 MB (7654466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79f2c1109f6989057dfe173d7350181a4d2c6c3094af18ca942f929b5893b99`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 348.9 KB (348911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d118af51ca1a98ff6c7e8640d57cc57f54bf619a7beef5cfe3f06f5d8299b7`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 76.2 KB (76219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70acf8981345c4c2a35e1ef34d5db2157777309445979db5767b97fc3ed74380`  
		Last Modified: Tue, 14 Jan 2025 07:05:53 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f95816f87e3225f4e1decf3e501fae6fbb6790fad0b7d8d65a087ae7b29ef8`  
		Last Modified: Tue, 14 Jan 2025 07:05:55 GMT  
		Size: 59.9 MB (59934359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2992763f8eefdb45c31411dd67a9d564ad9f745ddb5342c8d81ce027619b5f34`  
		Last Modified: Tue, 14 Jan 2025 07:05:53 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18af3d99a0909022477de34e3cd41b27f0c05f808cc2e7a9cd993b773424965b`  
		Last Modified: Tue, 14 Jan 2025 07:05:53 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22a682458745202fb57c949931140297950f9b433e640814950c8a46e89de1d`  
		Last Modified: Tue, 14 Jan 2025 07:05:54 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2beb4f8794b170cd72d38e6e6693c4646cfdc79bb031c87df8d7fee3e8a76e91`  
		Last Modified: Tue, 14 Jan 2025 07:05:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:c6a13eba71489fc59cd9c92ca465c308193f05103cfb0b5c34af7a8699d65767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3766469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d682b7d719df0c02ea96d9b87369a7aa958d848c8c1ebf95abad2e067349a2`

```dockerfile
```

-	Layers:
	-	`sha256:01960cba2344e00884c069dc1c4d74378f68588eff6590d21e9c9edfcfcc8c64`  
		Last Modified: Tue, 14 Jan 2025 07:05:54 GMT  
		Size: 3.7 MB (3735107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0709b04a14934c67ffd272b0d10dfe004ebad1b15ebbbe8635eac9ff16d5fe1a`  
		Last Modified: Tue, 14 Jan 2025 07:05:53 GMT  
		Size: 31.4 KB (31362 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:ce5f4a74cfa3e218f92a979ecb5b3e31672e4836be873bd940562a341cc68774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102836662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede2ae2501b8f0e8aaad5c35df606dc0c04d694502eea51da8352ed600148ed7`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81067e0e3bba96d20649463b18b008d3d7e179eb3bf3717b774c0755044cf9c3`  
		Last Modified: Tue, 14 Jan 2025 05:33:32 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74148a612c3f36d434969e538d6d57e4cf76649835841c5807b3ffc2cbffce7`  
		Last Modified: Tue, 14 Jan 2025 05:33:32 GMT  
		Size: 8.9 MB (8890044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ecdfa4e5d64a676ec9f86efc5a2484e2138b87e1662facb62c15ac654a14d3`  
		Last Modified: Tue, 14 Jan 2025 05:33:32 GMT  
		Size: 444.7 KB (444656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a6bc00395b03bc5e3249b488c39f64329dd3d45f2c6f2453bd5cc7eb9b41ea`  
		Last Modified: Tue, 14 Jan 2025 05:33:32 GMT  
		Size: 76.3 KB (76296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474507f74689957a855b7cd20157c95c6fe6cc2379a897969144a5ca19c4d283`  
		Last Modified: Tue, 14 Jan 2025 05:33:33 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75501244dec4e63def7f8fdfbe9688526248d4aab608083cfe00e59eb1842f57`  
		Last Modified: Tue, 14 Jan 2025 05:33:35 GMT  
		Size: 61.4 MB (61375381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0115c28916c533fa09785bc662cf095ad36452d25afbfb71d5cbfa242316cc60`  
		Last Modified: Tue, 14 Jan 2025 05:33:33 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bdcf633b0b3cb6fb8d912a8f17c7485c6b8f076c7417f3aeffe5e323b5bf6f`  
		Last Modified: Tue, 14 Jan 2025 05:33:34 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43ee460501f636effd361053cb780ff3abc1ee776488ecaf4fcfc2ee86e283b`  
		Last Modified: Tue, 14 Jan 2025 05:33:34 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee534d965d690e589e1b91f5c24d9eaf59505694adf3c10d3c621aa49bb59d2c`  
		Last Modified: Tue, 14 Jan 2025 05:33:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:e463a828e0a705d9cffeaf2f6cc0380fc3cd6ae9fef0083815045cec08178d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3770577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d3b7e0309a42d8a5bc2c7532134cf48d3924c9e300c5856a6183f23cfcfe610`

```dockerfile
```

-	Layers:
	-	`sha256:7d01da9240be067e7bbb932f994d2205ce58a416a86533385276e4159517b6f5`  
		Last Modified: Tue, 14 Jan 2025 05:33:32 GMT  
		Size: 3.7 MB (3739342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44f492900d4d03cd0eec5ec587afd6eb09fd96a5bc75e4557dbdc51c0a2b7f6a`  
		Last Modified: Tue, 14 Jan 2025 05:33:32 GMT  
		Size: 31.2 KB (31235 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3` - linux; s390x

```console
$ docker pull couchdb@sha256:28f9cf4433425a69a5bdae3d9c9ef5ed28fec149f1209de358b60b697dc93daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93424701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb7ac0c6af829cba2560c060a3d6d3a7cfb34f5479d6d35c3a3072a975d6d60d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796a06006ae38898ecb1581ebb6cb4522846078d5d7e8f8a2e300f972b51c50e`  
		Last Modified: Tue, 14 Jan 2025 05:03:14 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b027cea55a6bf96e67067e29306356b85485b1a314f72e2e2b84021d74d438f5`  
		Last Modified: Tue, 14 Jan 2025 05:03:14 GMT  
		Size: 7.4 MB (7388033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0735d11a8ad97f7a3f4b5cd4a2e5151328a005823fc219dd215c12aedeeb40f0`  
		Last Modified: Tue, 14 Jan 2025 05:03:14 GMT  
		Size: 355.7 KB (355663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6798c4ab25b5da5c70c4676230299a997c8fd1bfdcc8016b59d003a893466ab6`  
		Last Modified: Tue, 14 Jan 2025 05:03:14 GMT  
		Size: 76.4 KB (76363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c13301c1d5e64a322c24d9d3be5d1b5817e87d1c960cba8adcfbfb1bfb42eee`  
		Last Modified: Tue, 14 Jan 2025 05:07:45 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ac017d736c989b4ec0448700cdd5074cd3daa38060e351407f9c71811bbf13`  
		Last Modified: Tue, 14 Jan 2025 05:07:47 GMT  
		Size: 58.7 MB (58740471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e53eb03571e59417ecb7a43cd031fbe2a6d3a76f1d74c73cbd55e3ab829bbb`  
		Last Modified: Tue, 14 Jan 2025 05:07:45 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d091aeea5213bb02ff7b45496a3febfc588e6baf935e2cec835c61be4daa8d8c`  
		Last Modified: Tue, 14 Jan 2025 05:07:45 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a26c9d0aa440fc3655ce438466744b055bfc5888d46c08b86912bd60df872a`  
		Last Modified: Tue, 14 Jan 2025 05:07:46 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a84b5eec6e3b6928b691f4196d32e67d9550a4c464228764fd912d5c40ca937`  
		Last Modified: Tue, 14 Jan 2025 05:07:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:3657ea654efecdb25212dfa1dd9f774d42459235fb674dc228b3c0ebee70f75d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3765117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57621b36a9eda2b600fe94d97a0fa776c68c069b3b671840ea74670602ebc733`

```dockerfile
```

-	Layers:
	-	`sha256:9a8bdad6dea1cea90dd5a3a9a81fec45e05c7c813933839f0e65211a953a5a54`  
		Last Modified: Tue, 14 Jan 2025 05:07:45 GMT  
		Size: 3.7 MB (3733926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0e898e37e56677ed456734c270ddca2cc692fb63cc60fb9cc55b3f85d3ac556`  
		Last Modified: Tue, 14 Jan 2025 05:07:44 GMT  
		Size: 31.2 KB (31191 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.3.3`

```console
$ docker pull couchdb@sha256:779634db41d96ceb70622ea2d6366cf1735e5e0fae31a2273334bfb1e77b7e4d
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
$ docker pull couchdb@sha256:544976afdc75b72fca21564bfe4e05c3a54cf45153303ebf4bae2eb49efa41c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96712023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d59155283197de1d7f0407121faac7e5bd064bdc65c553115bd607f6745734`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e222e6ec445c670b44803406ec6d47484e45c38e87d9c2efa7a1d9303fba85a`  
		Last Modified: Tue, 14 Jan 2025 02:34:00 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d435c3ec7540aa7a7f6545aa659c02a9aed5c43390738654dc89324a15a0ba2f`  
		Last Modified: Tue, 14 Jan 2025 02:34:00 GMT  
		Size: 7.9 MB (7874923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17965acb8b2972226d4a3b2f6affc3e953024737c8118488ed39c5428eb8fdfb`  
		Last Modified: Tue, 14 Jan 2025 02:34:00 GMT  
		Size: 392.1 KB (392135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b48c12b2831723d23e626a4fcea9eb249f1d3334ea07adf99ddc159a47af1c4`  
		Last Modified: Tue, 14 Jan 2025 02:34:00 GMT  
		Size: 76.3 KB (76269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ad2b148ecd8acb886cbce4658ae367e9972c9f7bff90926598c9d8d8f2a058`  
		Last Modified: Tue, 14 Jan 2025 02:34:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06389e024c2d1f6e65152e0c37c28b706fd60e286ce76f7814db62ef6bcdf1ea`  
		Last Modified: Tue, 14 Jan 2025 02:34:02 GMT  
		Size: 60.2 MB (60150853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbddd212eec4a555f9faa530e669535e08c2072a7268cf8d040496f6855a83c`  
		Last Modified: Tue, 14 Jan 2025 02:34:01 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4234039500c108c2658677cbdf2615b19d71eb37eb5dfe567fd939095463a07`  
		Last Modified: Tue, 14 Jan 2025 02:34:01 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c77b84a2fefe8b1b04733755240970fef919f762d63055bc3339a64107d3512`  
		Last Modified: Tue, 14 Jan 2025 02:34:02 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f6f8d10bddfddf19515ca7fbc678be73c7dd93de9ba7b60b7d82dd903d25f1`  
		Last Modified: Tue, 14 Jan 2025 02:34:02 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:e70e3a79a9c3d4eb25752ced13399a166212ce4508bca27f2be371466040d47b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3766030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c32100cdc6579b90d34673118940c812a8b482b373cb82c26d93c83e664b0d5a`

```dockerfile
```

-	Layers:
	-	`sha256:43102d76c6ec7e317538a919e0ace34cf37f9ae1cb168280106e908e1be78e61`  
		Last Modified: Tue, 14 Jan 2025 02:34:01 GMT  
		Size: 3.7 MB (3734838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4094ce5973798e57689d4c5fb28f540b2a7c52279a17ac80a1356af266daf400`  
		Last Modified: Tue, 14 Jan 2025 02:34:00 GMT  
		Size: 31.2 KB (31192 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:c0bb87f69d46b18ec45cbcf834192896e3e859db5a46d877be6d100e0f2623dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96060414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d8092deae5348ef21718fe3fcbb35c16a1c8d64b135f940c0d25846069883c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a53b506eb957ed2ca989730c18ca42f6e0128157e3b16e04b417d5e3f6a46f`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0784cd6960fabd09529a3b70371d1a31ff9aec79c20d3905d9fbc1a2691c796`  
		Last Modified: Tue, 14 Jan 2025 07:04:10 GMT  
		Size: 7.7 MB (7654466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79f2c1109f6989057dfe173d7350181a4d2c6c3094af18ca942f929b5893b99`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 348.9 KB (348911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d118af51ca1a98ff6c7e8640d57cc57f54bf619a7beef5cfe3f06f5d8299b7`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 76.2 KB (76219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70acf8981345c4c2a35e1ef34d5db2157777309445979db5767b97fc3ed74380`  
		Last Modified: Tue, 14 Jan 2025 07:05:53 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f95816f87e3225f4e1decf3e501fae6fbb6790fad0b7d8d65a087ae7b29ef8`  
		Last Modified: Tue, 14 Jan 2025 07:05:55 GMT  
		Size: 59.9 MB (59934359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2992763f8eefdb45c31411dd67a9d564ad9f745ddb5342c8d81ce027619b5f34`  
		Last Modified: Tue, 14 Jan 2025 07:05:53 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18af3d99a0909022477de34e3cd41b27f0c05f808cc2e7a9cd993b773424965b`  
		Last Modified: Tue, 14 Jan 2025 07:05:53 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22a682458745202fb57c949931140297950f9b433e640814950c8a46e89de1d`  
		Last Modified: Tue, 14 Jan 2025 07:05:54 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2beb4f8794b170cd72d38e6e6693c4646cfdc79bb031c87df8d7fee3e8a76e91`  
		Last Modified: Tue, 14 Jan 2025 07:05:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:c6a13eba71489fc59cd9c92ca465c308193f05103cfb0b5c34af7a8699d65767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3766469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d682b7d719df0c02ea96d9b87369a7aa958d848c8c1ebf95abad2e067349a2`

```dockerfile
```

-	Layers:
	-	`sha256:01960cba2344e00884c069dc1c4d74378f68588eff6590d21e9c9edfcfcc8c64`  
		Last Modified: Tue, 14 Jan 2025 07:05:54 GMT  
		Size: 3.7 MB (3735107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0709b04a14934c67ffd272b0d10dfe004ebad1b15ebbbe8635eac9ff16d5fe1a`  
		Last Modified: Tue, 14 Jan 2025 07:05:53 GMT  
		Size: 31.4 KB (31362 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:ce5f4a74cfa3e218f92a979ecb5b3e31672e4836be873bd940562a341cc68774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102836662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede2ae2501b8f0e8aaad5c35df606dc0c04d694502eea51da8352ed600148ed7`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 01:37:24 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81067e0e3bba96d20649463b18b008d3d7e179eb3bf3717b774c0755044cf9c3`  
		Last Modified: Tue, 14 Jan 2025 05:33:32 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74148a612c3f36d434969e538d6d57e4cf76649835841c5807b3ffc2cbffce7`  
		Last Modified: Tue, 14 Jan 2025 05:33:32 GMT  
		Size: 8.9 MB (8890044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ecdfa4e5d64a676ec9f86efc5a2484e2138b87e1662facb62c15ac654a14d3`  
		Last Modified: Tue, 14 Jan 2025 05:33:32 GMT  
		Size: 444.7 KB (444656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a6bc00395b03bc5e3249b488c39f64329dd3d45f2c6f2453bd5cc7eb9b41ea`  
		Last Modified: Tue, 14 Jan 2025 05:33:32 GMT  
		Size: 76.3 KB (76296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474507f74689957a855b7cd20157c95c6fe6cc2379a897969144a5ca19c4d283`  
		Last Modified: Tue, 14 Jan 2025 05:33:33 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75501244dec4e63def7f8fdfbe9688526248d4aab608083cfe00e59eb1842f57`  
		Last Modified: Tue, 14 Jan 2025 05:33:35 GMT  
		Size: 61.4 MB (61375381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0115c28916c533fa09785bc662cf095ad36452d25afbfb71d5cbfa242316cc60`  
		Last Modified: Tue, 14 Jan 2025 05:33:33 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bdcf633b0b3cb6fb8d912a8f17c7485c6b8f076c7417f3aeffe5e323b5bf6f`  
		Last Modified: Tue, 14 Jan 2025 05:33:34 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43ee460501f636effd361053cb780ff3abc1ee776488ecaf4fcfc2ee86e283b`  
		Last Modified: Tue, 14 Jan 2025 05:33:34 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee534d965d690e589e1b91f5c24d9eaf59505694adf3c10d3c621aa49bb59d2c`  
		Last Modified: Tue, 14 Jan 2025 05:33:34 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:e463a828e0a705d9cffeaf2f6cc0380fc3cd6ae9fef0083815045cec08178d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3770577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d3b7e0309a42d8a5bc2c7532134cf48d3924c9e300c5856a6183f23cfcfe610`

```dockerfile
```

-	Layers:
	-	`sha256:7d01da9240be067e7bbb932f994d2205ce58a416a86533385276e4159517b6f5`  
		Last Modified: Tue, 14 Jan 2025 05:33:32 GMT  
		Size: 3.7 MB (3739342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44f492900d4d03cd0eec5ec587afd6eb09fd96a5bc75e4557dbdc51c0a2b7f6a`  
		Last Modified: Tue, 14 Jan 2025 05:33:32 GMT  
		Size: 31.2 KB (31235 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.3.3` - linux; s390x

```console
$ docker pull couchdb@sha256:28f9cf4433425a69a5bdae3d9c9ef5ed28fec149f1209de358b60b697dc93daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93424701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb7ac0c6af829cba2560c060a3d6d3a7cfb34f5479d6d35c3a3072a975d6d60d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.3.3
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION-1"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796a06006ae38898ecb1581ebb6cb4522846078d5d7e8f8a2e300f972b51c50e`  
		Last Modified: Tue, 14 Jan 2025 05:03:14 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b027cea55a6bf96e67067e29306356b85485b1a314f72e2e2b84021d74d438f5`  
		Last Modified: Tue, 14 Jan 2025 05:03:14 GMT  
		Size: 7.4 MB (7388033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0735d11a8ad97f7a3f4b5cd4a2e5151328a005823fc219dd215c12aedeeb40f0`  
		Last Modified: Tue, 14 Jan 2025 05:03:14 GMT  
		Size: 355.7 KB (355663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6798c4ab25b5da5c70c4676230299a997c8fd1bfdcc8016b59d003a893466ab6`  
		Last Modified: Tue, 14 Jan 2025 05:03:14 GMT  
		Size: 76.4 KB (76363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c13301c1d5e64a322c24d9d3be5d1b5817e87d1c960cba8adcfbfb1bfb42eee`  
		Last Modified: Tue, 14 Jan 2025 05:07:45 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ac017d736c989b4ec0448700cdd5074cd3daa38060e351407f9c71811bbf13`  
		Last Modified: Tue, 14 Jan 2025 05:07:47 GMT  
		Size: 58.7 MB (58740471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e53eb03571e59417ecb7a43cd031fbe2a6d3a76f1d74c73cbd55e3ab829bbb`  
		Last Modified: Tue, 14 Jan 2025 05:07:45 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d091aeea5213bb02ff7b45496a3febfc588e6baf935e2cec835c61be4daa8d8c`  
		Last Modified: Tue, 14 Jan 2025 05:07:45 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a26c9d0aa440fc3655ce438466744b055bfc5888d46c08b86912bd60df872a`  
		Last Modified: Tue, 14 Jan 2025 05:07:46 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a84b5eec6e3b6928b691f4196d32e67d9550a4c464228764fd912d5c40ca937`  
		Last Modified: Tue, 14 Jan 2025 05:07:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.3.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:3657ea654efecdb25212dfa1dd9f774d42459235fb674dc228b3c0ebee70f75d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3765117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57621b36a9eda2b600fe94d97a0fa776c68c069b3b671840ea74670602ebc733`

```dockerfile
```

-	Layers:
	-	`sha256:9a8bdad6dea1cea90dd5a3a9a81fec45e05c7c813933839f0e65211a953a5a54`  
		Last Modified: Tue, 14 Jan 2025 05:07:45 GMT  
		Size: 3.7 MB (3733926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0e898e37e56677ed456734c270ddca2cc692fb63cc60fb9cc55b3f85d3ac556`  
		Last Modified: Tue, 14 Jan 2025 05:07:44 GMT  
		Size: 31.2 KB (31191 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4`

```console
$ docker pull couchdb@sha256:ad6f63289f291bde103fd0d0f23504d5fd12a5de8f75a60317a5e228de64b46f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.4` - linux; amd64

```console
$ docker pull couchdb@sha256:a95224da3fe652bc5231bce9255d8eaeb589827d0f72d3af63b451a977d5f4c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133224084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfac4c6643a4b3f7ad19474bfe23a351fb2ef7912423a2d8df18b64bb62b06e4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94cfb7a0aadd073c09d48219fb9b682a517b3624d3f5d3d8f8a9fc1a29e8009c`  
		Last Modified: Tue, 14 Jan 2025 02:33:57 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f930d3e6857541e62b119727c90cd88062bd426dad1a2d97d3be3076f8e3b67`  
		Last Modified: Tue, 14 Jan 2025 02:33:57 GMT  
		Size: 7.9 MB (7874877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a17f12a2a50718f9ad85af6b6723e44d6a192e1ff473f4732a522ec8bd98938`  
		Last Modified: Tue, 14 Jan 2025 02:33:57 GMT  
		Size: 392.1 KB (392121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed0827d85352c811f94e2f36a99f0aca2954c1916ed3cbe059ddf88f0b45eaf`  
		Last Modified: Tue, 14 Jan 2025 02:33:57 GMT  
		Size: 76.3 KB (76255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa19dc7b250209e550ba9b11bc9680d9410a6a9c0e2c13adea5665d884edd9c5`  
		Last Modified: Tue, 14 Jan 2025 02:33:58 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc18312dcc63d53dded55cf2cea496f3449067e99317cb4a89522ca1cc9a7450`  
		Last Modified: Tue, 14 Jan 2025 02:33:59 GMT  
		Size: 96.7 MB (96662990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f883cb58292b7ed9110ffc0433e5b0c1545f164c765c031c7be05e154b863e4d`  
		Last Modified: Tue, 14 Jan 2025 02:33:58 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526420ad699c75c6d9f69f5926025f00ab7100ece6c2dc37f273a1684f3b4b71`  
		Last Modified: Tue, 14 Jan 2025 02:33:58 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18de8b09dd22f62475825a280b055d48deb17fe98b6e0cf3ffbb5291c66fe9c0`  
		Last Modified: Tue, 14 Jan 2025 02:33:58 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518a54d8eb18501bef8d2fe210909f87531c9ffa7b22cba9a32a19c253fbacf3`  
		Last Modified: Tue, 14 Jan 2025 02:33:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:6c7ac18b8bcad378884fa77920ec07987f7b8e7c139b2330af775618db4b18b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aac88a74b4468832ebae2de5148a13f5bcbea9a5049b4aff2914c15c8cbee3e7`

```dockerfile
```

-	Layers:
	-	`sha256:5fea47f279cfc6471eb29a3494dafe55bd603778641c6f55bf3557117ac8fa23`  
		Last Modified: Tue, 14 Jan 2025 02:33:57 GMT  
		Size: 3.9 MB (3933559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:098120b0ea4b9d34982ad821cf9ad78042b1755faffdc830b6568986b516d119`  
		Last Modified: Tue, 14 Jan 2025 02:33:57 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:33ad9d3878354339233afe53bb87df412283410b29708a7ca796f9ac07f8b621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132524949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414f1bc82926f249cbb136cfcfc223d28a194d2a83571874ab475e0fd4e4bbf1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a53b506eb957ed2ca989730c18ca42f6e0128157e3b16e04b417d5e3f6a46f`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0784cd6960fabd09529a3b70371d1a31ff9aec79c20d3905d9fbc1a2691c796`  
		Last Modified: Tue, 14 Jan 2025 07:04:10 GMT  
		Size: 7.7 MB (7654466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79f2c1109f6989057dfe173d7350181a4d2c6c3094af18ca942f929b5893b99`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 348.9 KB (348911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d118af51ca1a98ff6c7e8640d57cc57f54bf619a7beef5cfe3f06f5d8299b7`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 76.2 KB (76219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3f6188d465363a65faca581e7a29deff62119c7229c06b69dee041e921beff`  
		Last Modified: Tue, 14 Jan 2025 07:04:10 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4080fca21b251df01a293a38872fbe036647cd75dc3dc3d41eeacdcdc9f11e6`  
		Last Modified: Tue, 14 Jan 2025 07:04:13 GMT  
		Size: 96.4 MB (96398891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7570c55d2fc3d036f3606315986bce629111b93b08d0c34f0d640c69858cf107`  
		Last Modified: Tue, 14 Jan 2025 07:04:10 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93840e26080be7ccca7b1d4b3b6eb7444f77b3ce0c1dc501a7758bd2dddd794`  
		Last Modified: Tue, 14 Jan 2025 07:04:11 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349e54346d5fb87fe0546b92feeb3c137da315280a58ed267d31248215cee47c`  
		Last Modified: Tue, 14 Jan 2025 07:04:11 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0da7757a845ae5fd2495cc47db1219d3f9fa2fe4ce5b77dc66d72978d710e60`  
		Last Modified: Tue, 14 Jan 2025 07:04:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:81d65dd5d6ce19f884c69e8e6f10a4bdeee710be6407fc88a62f4599fdd5733a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544e391940d4445a1238cc81cff3eb9c691a770fc7915e710bf9f5799eefb829`

```dockerfile
```

-	Layers:
	-	`sha256:2faae1cf4e6c027422c66213a29885c6bea7c0675ebb0d7bc08679fc799cd5b4`  
		Last Modified: Tue, 14 Jan 2025 07:04:10 GMT  
		Size: 3.9 MB (3933852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e1b443faafdd6eb68584662f9aa0484863d3df8417e5bcb83deb538bcc5d8a2`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 32.0 KB (31970 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; s390x

```console
$ docker pull couchdb@sha256:c7e8d9e60dd0b23c1056e442f4e77c5781760cbea38e8fce29a80d5b907de056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129974576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0363ee9a1846275ab27cddc8292a5a6b0f512431ff9fa5318572c97040e8489`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796a06006ae38898ecb1581ebb6cb4522846078d5d7e8f8a2e300f972b51c50e`  
		Last Modified: Tue, 14 Jan 2025 05:03:14 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b027cea55a6bf96e67067e29306356b85485b1a314f72e2e2b84021d74d438f5`  
		Last Modified: Tue, 14 Jan 2025 05:03:14 GMT  
		Size: 7.4 MB (7388033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0735d11a8ad97f7a3f4b5cd4a2e5151328a005823fc219dd215c12aedeeb40f0`  
		Last Modified: Tue, 14 Jan 2025 05:03:14 GMT  
		Size: 355.7 KB (355663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6798c4ab25b5da5c70c4676230299a997c8fd1bfdcc8016b59d003a893466ab6`  
		Last Modified: Tue, 14 Jan 2025 05:03:14 GMT  
		Size: 76.4 KB (76363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f29ed5c6190b78c2ed8c0b5c8743ee9f67379bbed44eb54bd315e81a4d9aa21`  
		Last Modified: Tue, 14 Jan 2025 05:03:14 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6727b45b83dbfd16f7e25fabdd0c2dd979f1cd06056f045e211feec7f92c2eb2`  
		Last Modified: Tue, 14 Jan 2025 05:03:17 GMT  
		Size: 95.3 MB (95290347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa97288a42496b175156cccac188a3d05f71ef0442314740580d1da3404d5c9d`  
		Last Modified: Tue, 14 Jan 2025 05:03:15 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a531d6bae6d742f8280a170293a174fe348a43b08458c657c84520debf3a2b70`  
		Last Modified: Tue, 14 Jan 2025 05:03:15 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9ca4d8382089804dbaaa44ab24ea6b942fb920923799edc9c648305a60b10c`  
		Last Modified: Tue, 14 Jan 2025 05:03:15 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427c2f29f12e371e9f4bd0aa897ee7095a446affae5f5b5689ed1360429ffed8`  
		Last Modified: Tue, 14 Jan 2025 05:03:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:a5fe57a60ee9573da34f87eaa5edf04c6a94bdfc65c2a737b90c524f7bef97b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b07a080c2feda06310e3d6d790244bfd6a0a0ec160960bbf705453b4a3755ef`

```dockerfile
```

-	Layers:
	-	`sha256:f20e458946d34c50b0a1347b65b4f0672a969222c8d2b83d6ebf5eb589155013`  
		Last Modified: Tue, 14 Jan 2025 05:03:14 GMT  
		Size: 3.9 MB (3932647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0d8622b49e2f849721c02848b0f030134f69a3aa2f654e69ad45577609a701c`  
		Last Modified: Tue, 14 Jan 2025 05:03:14 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4-nouveau`

```console
$ docker pull couchdb@sha256:219375f533b07b6e0b284d0671f9783533d2ca2b1ba79b6c3fb4c4cfb811c299
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.4-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:9f157b7df804abcc1933c619722da373104834a327280c342147b08afd7252f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155519664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:467a3d123beefa4fdb65757d06376befaeb709d7d85a2ab331b5ffb69a491630`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401f19b00195b76f3e0327677012339b9ffe735976f9a0cc895ec8c96ba1049d`  
		Last Modified: Tue, 14 Jan 2025 02:34:06 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00956253f209377e98ec5aced7d1a8e5a8ecc9ebc105c29b4289c093be0205b`  
		Last Modified: Tue, 14 Jan 2025 02:34:06 GMT  
		Size: 7.9 MB (7874882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc4abb3ee0a71a4283c1ab0803eef1092db98081b80a5b6a0563cf8b76b2e4d`  
		Last Modified: Tue, 14 Jan 2025 02:34:07 GMT  
		Size: 77.3 MB (77284529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40c6a8e7237ef159fe15a0213639f4aaa63e3e4549ef6289f92c26ba5f18444`  
		Last Modified: Tue, 14 Jan 2025 02:34:06 GMT  
		Size: 415.0 KB (414955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dc361a846175db20b63927cb3924b56aeaeca552509f763f67965c1efb0d1c`  
		Last Modified: Tue, 14 Jan 2025 02:34:06 GMT  
		Size: 99.3 KB (99278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a333b9a57418ecfb361ed17a6a0877cb00070aa9f945dc2f284dcfee1914a6`  
		Last Modified: Tue, 14 Jan 2025 02:34:06 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d7487a36f127c29a998687e7904af7341ff1dcd5c443b78ba5a1092e74f0f3`  
		Last Modified: Tue, 14 Jan 2025 02:34:08 GMT  
		Size: 41.6 MB (41631728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e0ef7e407a6804703e784014daa95ab53996cab851d7b005d22cdf667ba855`  
		Last Modified: Tue, 14 Jan 2025 02:34:07 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:a2a1a6ad56e693f00305dfc24564be5de95f80e454b407dbecb3db3141688df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3486620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb899444b5a962775af77b72f86b74b6981b2f8340facf171cfff057eba4bbf1`

```dockerfile
```

-	Layers:
	-	`sha256:14a5a9d04a0c493c240fae7730b5416345468555258b2aa957f00292b635cdb0`  
		Last Modified: Tue, 14 Jan 2025 02:34:06 GMT  
		Size: 3.5 MB (3462056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1a8f4d197d74e81bf5cb9f92edb6085e00d72680d7b07f9ef96c9993cc11221`  
		Last Modified: Tue, 14 Jan 2025 02:34:06 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:ef7c562863a9fb584cc36263dc82db193a4a5c3956927ae78e18f702c0c5518e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.3 MB (154278229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b719cad0c7b5fdbfdbbac6dcb7a1e2ebde3550a3fe03266cf60522f6be67bab3`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79173b3fddb7da2629dd339e0d53b403ea8827bcbd9b247d684b58d32dff7cbf`  
		Last Modified: Tue, 14 Jan 2025 07:05:12 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31829078e1f4de67fcedf6a2d2d8ca1872f489122c7b4bcfa3cd33532c8cb239`  
		Last Modified: Tue, 14 Jan 2025 07:05:12 GMT  
		Size: 7.7 MB (7654485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3369295dc500f95559ea4509a427d2c0a4ee1c8ad2b7a79ee1dc560350241f77`  
		Last Modified: Tue, 14 Jan 2025 07:05:14 GMT  
		Size: 76.6 MB (76582294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e5bbcf4591afaea2d2cdc136dc489080dd97d81c24bd3ccbe400297114b51b`  
		Last Modified: Tue, 14 Jan 2025 07:05:12 GMT  
		Size: 371.7 KB (371693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acdad20d9a721bac2eb158329512906baee9555218f01a8e6ff0f9275510c66`  
		Last Modified: Tue, 14 Jan 2025 07:05:13 GMT  
		Size: 99.2 KB (99208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e627f9bf3e789b44c13cb9953004b89c6d68b322ee687562fe9fb76268a2d868`  
		Last Modified: Tue, 14 Jan 2025 07:05:13 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebeb5aa1e3f7f6837e61861bc4d688a7cb0e40daf66afe7b53355998b6c50ed`  
		Last Modified: Tue, 14 Jan 2025 07:05:14 GMT  
		Size: 41.5 MB (41527641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10a636108d2adc58e1f2c66283165d3226827a0d533ede0055e897d2464c6ed`  
		Last Modified: Tue, 14 Jan 2025 07:05:14 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:80be29eb1df008c822ee482e3954caa2ef94c11a5a1950dd74dbbaa0c6ace91a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3485478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071743ecadfba0fe3591807a89eb13c2932c9c451dc0d4b7924bb78aef478550`

```dockerfile
```

-	Layers:
	-	`sha256:c09558bcbcbf4d95c177b3cde1b9c16427e89ea9acbaf37de09ff936af7f2e77`  
		Last Modified: Tue, 14 Jan 2025 07:05:12 GMT  
		Size: 3.5 MB (3460732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1295fd7d68dfa423f317cb0bff79f1b1008e1459b1398163e931f34e6ccd895d`  
		Last Modified: Tue, 14 Jan 2025 07:05:12 GMT  
		Size: 24.7 KB (24746 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:70e854e48366f50062fe118022844c8125c1ee9307dfa4a899f39c661bea687c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149143062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0dc69c7c10538bf592fbad114bdc96969daf978a25d2339a56d350fe8ec2ce`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59eb9e34d805c91cbb6a777786054384ca5163a44adf355f562791cd57112727`  
		Last Modified: Tue, 14 Jan 2025 05:06:15 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72b3649e7568c38e8dc24f73e32d3e465865f019800342563581fe889fefc29`  
		Last Modified: Tue, 14 Jan 2025 05:06:16 GMT  
		Size: 7.4 MB (7388037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0d623f869fab1ed1b455344ac554f62617dd4a261427922f6b40763302dbbf`  
		Last Modified: Tue, 14 Jan 2025 05:06:17 GMT  
		Size: 73.1 MB (73065000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbbabbad5fba4b48ee2e9985e834dc26b68b7bd7e2c241cd33329010b1de583`  
		Last Modified: Tue, 14 Jan 2025 05:06:15 GMT  
		Size: 378.1 KB (378077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb882edbd68f219460fed3d76efd8d1b02ea6eeb91b88f4478d814abb1cb785f`  
		Last Modified: Tue, 14 Jan 2025 05:06:16 GMT  
		Size: 99.5 KB (99453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac8ff24b5596d40fbafc84ef2c075a634398df269e7f45160322b0a919fa96d`  
		Last Modified: Tue, 14 Jan 2025 05:06:16 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722810c372d4d7cc26207ca1af3be8e8aff57f515d108689fbb17825fad61a58`  
		Last Modified: Tue, 14 Jan 2025 05:06:17 GMT  
		Size: 41.4 MB (41351879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf4e49508aa7ee5296523f9f5b4b6dfbce8441995644a16c4c782ebf7e52ef1`  
		Last Modified: Tue, 14 Jan 2025 05:06:17 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:df7142ee8126c2074cbb8b05bc9de19425070b489604fbec2e24911f6e5d3452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3480041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1886209ac83e9c5d9023aa81b789998a7114e893017d719f32a25a50e94393a`

```dockerfile
```

-	Layers:
	-	`sha256:ec7fcf2e4eaaf1a58fe669cb770e5031e3f6dcb362b566d4f6ac72a409689cf2`  
		Last Modified: Tue, 14 Jan 2025 05:06:16 GMT  
		Size: 3.5 MB (3455477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:718a2716cf1a595efbfe017fdac9f821b2107e9b1b090958af71ceb5964e1534`  
		Last Modified: Tue, 14 Jan 2025 05:06:15 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.2`

```console
$ docker pull couchdb@sha256:ad6f63289f291bde103fd0d0f23504d5fd12a5de8f75a60317a5e228de64b46f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.4.2` - linux; amd64

```console
$ docker pull couchdb@sha256:a95224da3fe652bc5231bce9255d8eaeb589827d0f72d3af63b451a977d5f4c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133224084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfac4c6643a4b3f7ad19474bfe23a351fb2ef7912423a2d8df18b64bb62b06e4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94cfb7a0aadd073c09d48219fb9b682a517b3624d3f5d3d8f8a9fc1a29e8009c`  
		Last Modified: Tue, 14 Jan 2025 02:33:57 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f930d3e6857541e62b119727c90cd88062bd426dad1a2d97d3be3076f8e3b67`  
		Last Modified: Tue, 14 Jan 2025 02:33:57 GMT  
		Size: 7.9 MB (7874877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a17f12a2a50718f9ad85af6b6723e44d6a192e1ff473f4732a522ec8bd98938`  
		Last Modified: Tue, 14 Jan 2025 02:33:57 GMT  
		Size: 392.1 KB (392121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed0827d85352c811f94e2f36a99f0aca2954c1916ed3cbe059ddf88f0b45eaf`  
		Last Modified: Tue, 14 Jan 2025 02:33:57 GMT  
		Size: 76.3 KB (76255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa19dc7b250209e550ba9b11bc9680d9410a6a9c0e2c13adea5665d884edd9c5`  
		Last Modified: Tue, 14 Jan 2025 02:33:58 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc18312dcc63d53dded55cf2cea496f3449067e99317cb4a89522ca1cc9a7450`  
		Last Modified: Tue, 14 Jan 2025 02:33:59 GMT  
		Size: 96.7 MB (96662990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f883cb58292b7ed9110ffc0433e5b0c1545f164c765c031c7be05e154b863e4d`  
		Last Modified: Tue, 14 Jan 2025 02:33:58 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526420ad699c75c6d9f69f5926025f00ab7100ece6c2dc37f273a1684f3b4b71`  
		Last Modified: Tue, 14 Jan 2025 02:33:58 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18de8b09dd22f62475825a280b055d48deb17fe98b6e0cf3ffbb5291c66fe9c0`  
		Last Modified: Tue, 14 Jan 2025 02:33:58 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518a54d8eb18501bef8d2fe210909f87531c9ffa7b22cba9a32a19c253fbacf3`  
		Last Modified: Tue, 14 Jan 2025 02:33:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:6c7ac18b8bcad378884fa77920ec07987f7b8e7c139b2330af775618db4b18b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aac88a74b4468832ebae2de5148a13f5bcbea9a5049b4aff2914c15c8cbee3e7`

```dockerfile
```

-	Layers:
	-	`sha256:5fea47f279cfc6471eb29a3494dafe55bd603778641c6f55bf3557117ac8fa23`  
		Last Modified: Tue, 14 Jan 2025 02:33:57 GMT  
		Size: 3.9 MB (3933559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:098120b0ea4b9d34982ad821cf9ad78042b1755faffdc830b6568986b516d119`  
		Last Modified: Tue, 14 Jan 2025 02:33:57 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:33ad9d3878354339233afe53bb87df412283410b29708a7ca796f9ac07f8b621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132524949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414f1bc82926f249cbb136cfcfc223d28a194d2a83571874ab475e0fd4e4bbf1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a53b506eb957ed2ca989730c18ca42f6e0128157e3b16e04b417d5e3f6a46f`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0784cd6960fabd09529a3b70371d1a31ff9aec79c20d3905d9fbc1a2691c796`  
		Last Modified: Tue, 14 Jan 2025 07:04:10 GMT  
		Size: 7.7 MB (7654466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79f2c1109f6989057dfe173d7350181a4d2c6c3094af18ca942f929b5893b99`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 348.9 KB (348911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d118af51ca1a98ff6c7e8640d57cc57f54bf619a7beef5cfe3f06f5d8299b7`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 76.2 KB (76219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3f6188d465363a65faca581e7a29deff62119c7229c06b69dee041e921beff`  
		Last Modified: Tue, 14 Jan 2025 07:04:10 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4080fca21b251df01a293a38872fbe036647cd75dc3dc3d41eeacdcdc9f11e6`  
		Last Modified: Tue, 14 Jan 2025 07:04:13 GMT  
		Size: 96.4 MB (96398891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7570c55d2fc3d036f3606315986bce629111b93b08d0c34f0d640c69858cf107`  
		Last Modified: Tue, 14 Jan 2025 07:04:10 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93840e26080be7ccca7b1d4b3b6eb7444f77b3ce0c1dc501a7758bd2dddd794`  
		Last Modified: Tue, 14 Jan 2025 07:04:11 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349e54346d5fb87fe0546b92feeb3c137da315280a58ed267d31248215cee47c`  
		Last Modified: Tue, 14 Jan 2025 07:04:11 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0da7757a845ae5fd2495cc47db1219d3f9fa2fe4ce5b77dc66d72978d710e60`  
		Last Modified: Tue, 14 Jan 2025 07:04:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:81d65dd5d6ce19f884c69e8e6f10a4bdeee710be6407fc88a62f4599fdd5733a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544e391940d4445a1238cc81cff3eb9c691a770fc7915e710bf9f5799eefb829`

```dockerfile
```

-	Layers:
	-	`sha256:2faae1cf4e6c027422c66213a29885c6bea7c0675ebb0d7bc08679fc799cd5b4`  
		Last Modified: Tue, 14 Jan 2025 07:04:10 GMT  
		Size: 3.9 MB (3933852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e1b443faafdd6eb68584662f9aa0484863d3df8417e5bcb83deb538bcc5d8a2`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 32.0 KB (31970 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.2` - linux; s390x

```console
$ docker pull couchdb@sha256:c7e8d9e60dd0b23c1056e442f4e77c5781760cbea38e8fce29a80d5b907de056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129974576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0363ee9a1846275ab27cddc8292a5a6b0f512431ff9fa5318572c97040e8489`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796a06006ae38898ecb1581ebb6cb4522846078d5d7e8f8a2e300f972b51c50e`  
		Last Modified: Tue, 14 Jan 2025 05:03:14 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b027cea55a6bf96e67067e29306356b85485b1a314f72e2e2b84021d74d438f5`  
		Last Modified: Tue, 14 Jan 2025 05:03:14 GMT  
		Size: 7.4 MB (7388033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0735d11a8ad97f7a3f4b5cd4a2e5151328a005823fc219dd215c12aedeeb40f0`  
		Last Modified: Tue, 14 Jan 2025 05:03:14 GMT  
		Size: 355.7 KB (355663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6798c4ab25b5da5c70c4676230299a997c8fd1bfdcc8016b59d003a893466ab6`  
		Last Modified: Tue, 14 Jan 2025 05:03:14 GMT  
		Size: 76.4 KB (76363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f29ed5c6190b78c2ed8c0b5c8743ee9f67379bbed44eb54bd315e81a4d9aa21`  
		Last Modified: Tue, 14 Jan 2025 05:03:14 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6727b45b83dbfd16f7e25fabdd0c2dd979f1cd06056f045e211feec7f92c2eb2`  
		Last Modified: Tue, 14 Jan 2025 05:03:17 GMT  
		Size: 95.3 MB (95290347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa97288a42496b175156cccac188a3d05f71ef0442314740580d1da3404d5c9d`  
		Last Modified: Tue, 14 Jan 2025 05:03:15 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a531d6bae6d742f8280a170293a174fe348a43b08458c657c84520debf3a2b70`  
		Last Modified: Tue, 14 Jan 2025 05:03:15 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9ca4d8382089804dbaaa44ab24ea6b942fb920923799edc9c648305a60b10c`  
		Last Modified: Tue, 14 Jan 2025 05:03:15 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427c2f29f12e371e9f4bd0aa897ee7095a446affae5f5b5689ed1360429ffed8`  
		Last Modified: Tue, 14 Jan 2025 05:03:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:a5fe57a60ee9573da34f87eaa5edf04c6a94bdfc65c2a737b90c524f7bef97b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b07a080c2feda06310e3d6d790244bfd6a0a0ec160960bbf705453b4a3755ef`

```dockerfile
```

-	Layers:
	-	`sha256:f20e458946d34c50b0a1347b65b4f0672a969222c8d2b83d6ebf5eb589155013`  
		Last Modified: Tue, 14 Jan 2025 05:03:14 GMT  
		Size: 3.9 MB (3932647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0d8622b49e2f849721c02848b0f030134f69a3aa2f654e69ad45577609a701c`  
		Last Modified: Tue, 14 Jan 2025 05:03:14 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.2-nouveau`

```console
$ docker pull couchdb@sha256:219375f533b07b6e0b284d0671f9783533d2ca2b1ba79b6c3fb4c4cfb811c299
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.4.2-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:9f157b7df804abcc1933c619722da373104834a327280c342147b08afd7252f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155519664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:467a3d123beefa4fdb65757d06376befaeb709d7d85a2ab331b5ffb69a491630`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401f19b00195b76f3e0327677012339b9ffe735976f9a0cc895ec8c96ba1049d`  
		Last Modified: Tue, 14 Jan 2025 02:34:06 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00956253f209377e98ec5aced7d1a8e5a8ecc9ebc105c29b4289c093be0205b`  
		Last Modified: Tue, 14 Jan 2025 02:34:06 GMT  
		Size: 7.9 MB (7874882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc4abb3ee0a71a4283c1ab0803eef1092db98081b80a5b6a0563cf8b76b2e4d`  
		Last Modified: Tue, 14 Jan 2025 02:34:07 GMT  
		Size: 77.3 MB (77284529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40c6a8e7237ef159fe15a0213639f4aaa63e3e4549ef6289f92c26ba5f18444`  
		Last Modified: Tue, 14 Jan 2025 02:34:06 GMT  
		Size: 415.0 KB (414955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dc361a846175db20b63927cb3924b56aeaeca552509f763f67965c1efb0d1c`  
		Last Modified: Tue, 14 Jan 2025 02:34:06 GMT  
		Size: 99.3 KB (99278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a333b9a57418ecfb361ed17a6a0877cb00070aa9f945dc2f284dcfee1914a6`  
		Last Modified: Tue, 14 Jan 2025 02:34:06 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d7487a36f127c29a998687e7904af7341ff1dcd5c443b78ba5a1092e74f0f3`  
		Last Modified: Tue, 14 Jan 2025 02:34:08 GMT  
		Size: 41.6 MB (41631728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e0ef7e407a6804703e784014daa95ab53996cab851d7b005d22cdf667ba855`  
		Last Modified: Tue, 14 Jan 2025 02:34:07 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.2-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:a2a1a6ad56e693f00305dfc24564be5de95f80e454b407dbecb3db3141688df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3486620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb899444b5a962775af77b72f86b74b6981b2f8340facf171cfff057eba4bbf1`

```dockerfile
```

-	Layers:
	-	`sha256:14a5a9d04a0c493c240fae7730b5416345468555258b2aa957f00292b635cdb0`  
		Last Modified: Tue, 14 Jan 2025 02:34:06 GMT  
		Size: 3.5 MB (3462056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1a8f4d197d74e81bf5cb9f92edb6085e00d72680d7b07f9ef96c9993cc11221`  
		Last Modified: Tue, 14 Jan 2025 02:34:06 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.2-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:ef7c562863a9fb584cc36263dc82db193a4a5c3956927ae78e18f702c0c5518e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.3 MB (154278229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b719cad0c7b5fdbfdbbac6dcb7a1e2ebde3550a3fe03266cf60522f6be67bab3`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79173b3fddb7da2629dd339e0d53b403ea8827bcbd9b247d684b58d32dff7cbf`  
		Last Modified: Tue, 14 Jan 2025 07:05:12 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31829078e1f4de67fcedf6a2d2d8ca1872f489122c7b4bcfa3cd33532c8cb239`  
		Last Modified: Tue, 14 Jan 2025 07:05:12 GMT  
		Size: 7.7 MB (7654485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3369295dc500f95559ea4509a427d2c0a4ee1c8ad2b7a79ee1dc560350241f77`  
		Last Modified: Tue, 14 Jan 2025 07:05:14 GMT  
		Size: 76.6 MB (76582294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e5bbcf4591afaea2d2cdc136dc489080dd97d81c24bd3ccbe400297114b51b`  
		Last Modified: Tue, 14 Jan 2025 07:05:12 GMT  
		Size: 371.7 KB (371693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acdad20d9a721bac2eb158329512906baee9555218f01a8e6ff0f9275510c66`  
		Last Modified: Tue, 14 Jan 2025 07:05:13 GMT  
		Size: 99.2 KB (99208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e627f9bf3e789b44c13cb9953004b89c6d68b322ee687562fe9fb76268a2d868`  
		Last Modified: Tue, 14 Jan 2025 07:05:13 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebeb5aa1e3f7f6837e61861bc4d688a7cb0e40daf66afe7b53355998b6c50ed`  
		Last Modified: Tue, 14 Jan 2025 07:05:14 GMT  
		Size: 41.5 MB (41527641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10a636108d2adc58e1f2c66283165d3226827a0d533ede0055e897d2464c6ed`  
		Last Modified: Tue, 14 Jan 2025 07:05:14 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.2-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:80be29eb1df008c822ee482e3954caa2ef94c11a5a1950dd74dbbaa0c6ace91a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3485478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071743ecadfba0fe3591807a89eb13c2932c9c451dc0d4b7924bb78aef478550`

```dockerfile
```

-	Layers:
	-	`sha256:c09558bcbcbf4d95c177b3cde1b9c16427e89ea9acbaf37de09ff936af7f2e77`  
		Last Modified: Tue, 14 Jan 2025 07:05:12 GMT  
		Size: 3.5 MB (3460732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1295fd7d68dfa423f317cb0bff79f1b1008e1459b1398163e931f34e6ccd895d`  
		Last Modified: Tue, 14 Jan 2025 07:05:12 GMT  
		Size: 24.7 KB (24746 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.2-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:70e854e48366f50062fe118022844c8125c1ee9307dfa4a899f39c661bea687c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149143062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0dc69c7c10538bf592fbad114bdc96969daf978a25d2339a56d350fe8ec2ce`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.2~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/nouveau/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59eb9e34d805c91cbb6a777786054384ca5163a44adf355f562791cd57112727`  
		Last Modified: Tue, 14 Jan 2025 05:06:15 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72b3649e7568c38e8dc24f73e32d3e465865f019800342563581fe889fefc29`  
		Last Modified: Tue, 14 Jan 2025 05:06:16 GMT  
		Size: 7.4 MB (7388037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0d623f869fab1ed1b455344ac554f62617dd4a261427922f6b40763302dbbf`  
		Last Modified: Tue, 14 Jan 2025 05:06:17 GMT  
		Size: 73.1 MB (73065000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbbabbad5fba4b48ee2e9985e834dc26b68b7bd7e2c241cd33329010b1de583`  
		Last Modified: Tue, 14 Jan 2025 05:06:15 GMT  
		Size: 378.1 KB (378077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb882edbd68f219460fed3d76efd8d1b02ea6eeb91b88f4478d814abb1cb785f`  
		Last Modified: Tue, 14 Jan 2025 05:06:16 GMT  
		Size: 99.5 KB (99453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac8ff24b5596d40fbafc84ef2c075a634398df269e7f45160322b0a919fa96d`  
		Last Modified: Tue, 14 Jan 2025 05:06:16 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722810c372d4d7cc26207ca1af3be8e8aff57f515d108689fbb17825fad61a58`  
		Last Modified: Tue, 14 Jan 2025 05:06:17 GMT  
		Size: 41.4 MB (41351879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf4e49508aa7ee5296523f9f5b4b6dfbce8441995644a16c4c782ebf7e52ef1`  
		Last Modified: Tue, 14 Jan 2025 05:06:17 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.2-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:df7142ee8126c2074cbb8b05bc9de19425070b489604fbec2e24911f6e5d3452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3480041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1886209ac83e9c5d9023aa81b789998a7114e893017d719f32a25a50e94393a`

```dockerfile
```

-	Layers:
	-	`sha256:ec7fcf2e4eaaf1a58fe669cb770e5031e3f6dcb362b566d4f6ac72a409689cf2`  
		Last Modified: Tue, 14 Jan 2025 05:06:16 GMT  
		Size: 3.5 MB (3455477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:718a2716cf1a595efbfe017fdac9f821b2107e9b1b090958af71ceb5964e1534`  
		Last Modified: Tue, 14 Jan 2025 05:06:15 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:ad6f63289f291bde103fd0d0f23504d5fd12a5de8f75a60317a5e228de64b46f
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
$ docker pull couchdb@sha256:a95224da3fe652bc5231bce9255d8eaeb589827d0f72d3af63b451a977d5f4c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133224084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfac4c6643a4b3f7ad19474bfe23a351fb2ef7912423a2d8df18b64bb62b06e4`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94cfb7a0aadd073c09d48219fb9b682a517b3624d3f5d3d8f8a9fc1a29e8009c`  
		Last Modified: Tue, 14 Jan 2025 02:33:57 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f930d3e6857541e62b119727c90cd88062bd426dad1a2d97d3be3076f8e3b67`  
		Last Modified: Tue, 14 Jan 2025 02:33:57 GMT  
		Size: 7.9 MB (7874877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a17f12a2a50718f9ad85af6b6723e44d6a192e1ff473f4732a522ec8bd98938`  
		Last Modified: Tue, 14 Jan 2025 02:33:57 GMT  
		Size: 392.1 KB (392121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed0827d85352c811f94e2f36a99f0aca2954c1916ed3cbe059ddf88f0b45eaf`  
		Last Modified: Tue, 14 Jan 2025 02:33:57 GMT  
		Size: 76.3 KB (76255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa19dc7b250209e550ba9b11bc9680d9410a6a9c0e2c13adea5665d884edd9c5`  
		Last Modified: Tue, 14 Jan 2025 02:33:58 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc18312dcc63d53dded55cf2cea496f3449067e99317cb4a89522ca1cc9a7450`  
		Last Modified: Tue, 14 Jan 2025 02:33:59 GMT  
		Size: 96.7 MB (96662990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f883cb58292b7ed9110ffc0433e5b0c1545f164c765c031c7be05e154b863e4d`  
		Last Modified: Tue, 14 Jan 2025 02:33:58 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526420ad699c75c6d9f69f5926025f00ab7100ece6c2dc37f273a1684f3b4b71`  
		Last Modified: Tue, 14 Jan 2025 02:33:58 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18de8b09dd22f62475825a280b055d48deb17fe98b6e0cf3ffbb5291c66fe9c0`  
		Last Modified: Tue, 14 Jan 2025 02:33:58 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518a54d8eb18501bef8d2fe210909f87531c9ffa7b22cba9a32a19c253fbacf3`  
		Last Modified: Tue, 14 Jan 2025 02:33:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:6c7ac18b8bcad378884fa77920ec07987f7b8e7c139b2330af775618db4b18b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aac88a74b4468832ebae2de5148a13f5bcbea9a5049b4aff2914c15c8cbee3e7`

```dockerfile
```

-	Layers:
	-	`sha256:5fea47f279cfc6471eb29a3494dafe55bd603778641c6f55bf3557117ac8fa23`  
		Last Modified: Tue, 14 Jan 2025 02:33:57 GMT  
		Size: 3.9 MB (3933559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:098120b0ea4b9d34982ad821cf9ad78042b1755faffdc830b6568986b516d119`  
		Last Modified: Tue, 14 Jan 2025 02:33:57 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:33ad9d3878354339233afe53bb87df412283410b29708a7ca796f9ac07f8b621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132524949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414f1bc82926f249cbb136cfcfc223d28a194d2a83571874ab475e0fd4e4bbf1`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a53b506eb957ed2ca989730c18ca42f6e0128157e3b16e04b417d5e3f6a46f`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0784cd6960fabd09529a3b70371d1a31ff9aec79c20d3905d9fbc1a2691c796`  
		Last Modified: Tue, 14 Jan 2025 07:04:10 GMT  
		Size: 7.7 MB (7654466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79f2c1109f6989057dfe173d7350181a4d2c6c3094af18ca942f929b5893b99`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 348.9 KB (348911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d118af51ca1a98ff6c7e8640d57cc57f54bf619a7beef5cfe3f06f5d8299b7`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 76.2 KB (76219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3f6188d465363a65faca581e7a29deff62119c7229c06b69dee041e921beff`  
		Last Modified: Tue, 14 Jan 2025 07:04:10 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4080fca21b251df01a293a38872fbe036647cd75dc3dc3d41eeacdcdc9f11e6`  
		Last Modified: Tue, 14 Jan 2025 07:04:13 GMT  
		Size: 96.4 MB (96398891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7570c55d2fc3d036f3606315986bce629111b93b08d0c34f0d640c69858cf107`  
		Last Modified: Tue, 14 Jan 2025 07:04:10 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93840e26080be7ccca7b1d4b3b6eb7444f77b3ce0c1dc501a7758bd2dddd794`  
		Last Modified: Tue, 14 Jan 2025 07:04:11 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349e54346d5fb87fe0546b92feeb3c137da315280a58ed267d31248215cee47c`  
		Last Modified: Tue, 14 Jan 2025 07:04:11 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0da7757a845ae5fd2495cc47db1219d3f9fa2fe4ce5b77dc66d72978d710e60`  
		Last Modified: Tue, 14 Jan 2025 07:04:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:81d65dd5d6ce19f884c69e8e6f10a4bdeee710be6407fc88a62f4599fdd5733a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544e391940d4445a1238cc81cff3eb9c691a770fc7915e710bf9f5799eefb829`

```dockerfile
```

-	Layers:
	-	`sha256:2faae1cf4e6c027422c66213a29885c6bea7c0675ebb0d7bc08679fc799cd5b4`  
		Last Modified: Tue, 14 Jan 2025 07:04:10 GMT  
		Size: 3.9 MB (3933852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e1b443faafdd6eb68584662f9aa0484863d3df8417e5bcb83deb538bcc5d8a2`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 32.0 KB (31970 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:c7e8d9e60dd0b23c1056e442f4e77c5781760cbea38e8fce29a80d5b907de056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129974576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0363ee9a1846275ab27cddc8292a5a6b0f512431ff9fa5318572c97040e8489`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 22 Oct 2024 18:47:05 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Tue, 22 Oct 2024 18:47:05 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 22 Oct 2024 18:47:05 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENV COUCHDB_VERSION=3.4.2
# Tue, 22 Oct 2024 18:47:05 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Tue, 22 Oct 2024 18:47:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Tue, 22 Oct 2024 18:47:05 GMT
VOLUME [/opt/couchdb/data]
# Tue, 22 Oct 2024 18:47:05 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Tue, 22 Oct 2024 18:47:05 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796a06006ae38898ecb1581ebb6cb4522846078d5d7e8f8a2e300f972b51c50e`  
		Last Modified: Tue, 14 Jan 2025 05:03:14 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b027cea55a6bf96e67067e29306356b85485b1a314f72e2e2b84021d74d438f5`  
		Last Modified: Tue, 14 Jan 2025 05:03:14 GMT  
		Size: 7.4 MB (7388033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0735d11a8ad97f7a3f4b5cd4a2e5151328a005823fc219dd215c12aedeeb40f0`  
		Last Modified: Tue, 14 Jan 2025 05:03:14 GMT  
		Size: 355.7 KB (355663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6798c4ab25b5da5c70c4676230299a997c8fd1bfdcc8016b59d003a893466ab6`  
		Last Modified: Tue, 14 Jan 2025 05:03:14 GMT  
		Size: 76.4 KB (76363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f29ed5c6190b78c2ed8c0b5c8743ee9f67379bbed44eb54bd315e81a4d9aa21`  
		Last Modified: Tue, 14 Jan 2025 05:03:14 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6727b45b83dbfd16f7e25fabdd0c2dd979f1cd06056f045e211feec7f92c2eb2`  
		Last Modified: Tue, 14 Jan 2025 05:03:17 GMT  
		Size: 95.3 MB (95290347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa97288a42496b175156cccac188a3d05f71ef0442314740580d1da3404d5c9d`  
		Last Modified: Tue, 14 Jan 2025 05:03:15 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a531d6bae6d742f8280a170293a174fe348a43b08458c657c84520debf3a2b70`  
		Last Modified: Tue, 14 Jan 2025 05:03:15 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9ca4d8382089804dbaaa44ab24ea6b942fb920923799edc9c648305a60b10c`  
		Last Modified: Tue, 14 Jan 2025 05:03:15 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427c2f29f12e371e9f4bd0aa897ee7095a446affae5f5b5689ed1360429ffed8`  
		Last Modified: Tue, 14 Jan 2025 05:03:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:a5fe57a60ee9573da34f87eaa5edf04c6a94bdfc65c2a737b90c524f7bef97b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3964423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b07a080c2feda06310e3d6d790244bfd6a0a0ec160960bbf705453b4a3755ef`

```dockerfile
```

-	Layers:
	-	`sha256:f20e458946d34c50b0a1347b65b4f0672a969222c8d2b83d6ebf5eb589155013`  
		Last Modified: Tue, 14 Jan 2025 05:03:14 GMT  
		Size: 3.9 MB (3932647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0d8622b49e2f849721c02848b0f030134f69a3aa2f654e69ad45577609a701c`  
		Last Modified: Tue, 14 Jan 2025 05:03:14 GMT  
		Size: 31.8 KB (31776 bytes)  
		MIME: application/vnd.in-toto+json
