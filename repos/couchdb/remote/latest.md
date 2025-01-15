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
		Last Modified: Tue, 14 Jan 2025 20:32:59 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94cfb7a0aadd073c09d48219fb9b682a517b3624d3f5d3d8f8a9fc1a29e8009c`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:33:52 GMT  
		Size: 76.3 KB (76255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa19dc7b250209e550ba9b11bc9680d9410a6a9c0e2c13adea5665d884edd9c5`  
		Last Modified: Tue, 14 Jan 2025 20:33:52 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:33:52 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18de8b09dd22f62475825a280b055d48deb17fe98b6e0cf3ffbb5291c66fe9c0`  
		Last Modified: Tue, 14 Jan 2025 20:33:52 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518a54d8eb18501bef8d2fe210909f87531c9ffa7b22cba9a32a19c253fbacf3`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a53b506eb957ed2ca989730c18ca42f6e0128157e3b16e04b417d5e3f6a46f`  
		Last Modified: Tue, 14 Jan 2025 20:52:23 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0784cd6960fabd09529a3b70371d1a31ff9aec79c20d3905d9fbc1a2691c796`  
		Last Modified: Tue, 14 Jan 2025 07:04:10 GMT  
		Size: 7.7 MB (7654466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79f2c1109f6989057dfe173d7350181a4d2c6c3094af18ca942f929b5893b99`  
		Last Modified: Tue, 14 Jan 2025 20:42:49 GMT  
		Size: 348.9 KB (348911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d118af51ca1a98ff6c7e8640d57cc57f54bf619a7beef5cfe3f06f5d8299b7`  
		Last Modified: Tue, 14 Jan 2025 07:04:09 GMT  
		Size: 76.2 KB (76219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3f6188d465363a65faca581e7a29deff62119c7229c06b69dee041e921beff`  
		Last Modified: Tue, 14 Jan 2025 20:42:50 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4080fca21b251df01a293a38872fbe036647cd75dc3dc3d41eeacdcdc9f11e6`  
		Last Modified: Tue, 14 Jan 2025 20:59:14 GMT  
		Size: 96.4 MB (96398891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7570c55d2fc3d036f3606315986bce629111b93b08d0c34f0d640c69858cf107`  
		Last Modified: Tue, 14 Jan 2025 20:42:50 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93840e26080be7ccca7b1d4b3b6eb7444f77b3ce0c1dc501a7758bd2dddd794`  
		Last Modified: Tue, 14 Jan 2025 20:52:23 GMT  
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
		Last Modified: Tue, 14 Jan 2025 22:24:50 GMT  
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
		Last Modified: Tue, 14 Jan 2025 20:36:29 GMT  
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
