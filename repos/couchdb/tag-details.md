<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchdb`

-	[`couchdb:3`](#couchdb3)
-	[`couchdb:3-nouveau`](#couchdb3-nouveau)
-	[`couchdb:3.4`](#couchdb34)
-	[`couchdb:3.4-nouveau`](#couchdb34-nouveau)
-	[`couchdb:3.4.3`](#couchdb343)
-	[`couchdb:3.4.3-nouveau`](#couchdb343-nouveau)
-	[`couchdb:3.5`](#couchdb35)
-	[`couchdb:3.5-nouveau`](#couchdb35-nouveau)
-	[`couchdb:3.5.2`](#couchdb352)
-	[`couchdb:3.5.2-nouveau`](#couchdb352-nouveau)
-	[`couchdb:3.5.2.1`](#couchdb3521)
-	[`couchdb:3.5.2.1-nouveau`](#couchdb3521-nouveau)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:3`

```console
$ docker pull couchdb@sha256:7219f4799fec01f35adcc445b9333cfd890bf9d2957e0ae32a345017dd0563a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:cc3732411c64ced82a0b60aa8aa3de3d506085745bc70a74ecb3b3be6116502d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148844108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d44232e2936d17afb2b1798bf2c507aec7faf0cafbd28fe901513e041cdbd91b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:41:45 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 01:41:45 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 24 Jun 2026 01:41:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:41:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 01:41:56 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 01:42:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:02 GMT
ENV COUCHDB_VERSION=3.5.2.1
# Wed, 24 Jun 2026 01:42:02 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y couchdb="$COUCHDB_VERSION"~trixie ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:42:14 GMT
VOLUME [/opt/couchdb/data]
# Wed, 24 Jun 2026 01:42:14 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 24 Jun 2026 01:42:14 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf4e623ec506cc4a3dac913d3b56b90e4fef2a77a9c36fdcf173f8d3b5278c5`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41389ef1d3c08b13549c1b4348192c604ad3a284329e5871b954354eea29701a`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 7.5 MB (7492182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacc441dd0740be802ff13f9f1b47daf5a3bc15af218d5781f017c26802a8a59`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 417.6 KB (417586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff6e59fcf95b99c098ff3c8880d2452b7aba9d13bf6c0f19ad0b5fe06b97e30`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 338.6 KB (338589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502ff7fc683f79f37d7c73b6e619ed701d657f0ceb516a15a687ca25a370a2d2`  
		Last Modified: Wed, 24 Jun 2026 01:42:29 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1729ef1d7ef490d9df9a9bef35e40236961c036f4e42e61b4bba68825d9f4200`  
		Last Modified: Wed, 24 Jun 2026 01:42:31 GMT  
		Size: 110.8 MB (110804902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fcad644c61c6a3b04844a48f337699db4d160e2c4236738941c1396e297ed7`  
		Last Modified: Wed, 24 Jun 2026 01:42:29 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30231fb7931d1261052bec6b2a3aea93155252de5867b2d3056530b0b784d3af`  
		Last Modified: Wed, 24 Jun 2026 01:42:29 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3153c610da961afa19f846e0e599bf564690dbfb87a41ac22e613f5ec4e042b7`  
		Last Modified: Wed, 24 Jun 2026 01:42:30 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe1d9b4ca3855ee21d8ca2d057b734e762a2749caf05b395eb4314e6d18e99c`  
		Last Modified: Wed, 24 Jun 2026 01:42:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:c0a6265cdedc5f932c8432b70206466e94fa714fbd92ba1a364ba1e2d977b915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb9afdcbd7a9e6a733e0fb6934737903fae00152b13a1d44bfe1701f63b0eaf`

```dockerfile
```

-	Layers:
	-	`sha256:a2a421c48dedd1c7d59b486174d617e7b94ad5a4ad3b1dbd53f3d3643e38722e`  
		Last Modified: Wed, 24 Jun 2026 01:42:28 GMT  
		Size: 4.2 MB (4180389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5350a5f3c13beedaf06d881b2ad3a3232267c800b3458b46c120994b684bd98a`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 31.7 KB (31675 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:3beeeddf8bd41e3d3175a81706041970931a6b9648ebe7cf0d83592dc9008cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148610960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2709151b5d31ef9083ce177249e3dc839908ce169530879c0dd33f6e6291a9e0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:45:14 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 01:45:14 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 24 Jun 2026 01:45:21 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 01:45:25 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 01:45:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:32 GMT
ENV COUCHDB_VERSION=3.5.2.1
# Wed, 24 Jun 2026 01:45:32 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 01:45:46 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y couchdb="$COUCHDB_VERSION"~trixie ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 24 Jun 2026 01:45:46 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 24 Jun 2026 01:45:46 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 24 Jun 2026 01:45:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 24 Jun 2026 01:45:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:45:46 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:45:46 GMT
VOLUME [/opt/couchdb/data]
# Wed, 24 Jun 2026 01:45:46 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 24 Jun 2026 01:45:46 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c34eafb21ffe87f9a1c7c17f11fcd3e474ff4be443d91b71069650935b45a49`  
		Last Modified: Wed, 24 Jun 2026 01:46:00 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c374173332b5fe10199e92b26dc196540789ebd47eac3a886163b9464183886`  
		Last Modified: Wed, 24 Jun 2026 01:46:00 GMT  
		Size: 7.3 MB (7261195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297cb5e063f5f7b21b877726abd1f8405924db8308e3dcacee0c9e445b5ca12b`  
		Last Modified: Wed, 24 Jun 2026 01:45:59 GMT  
		Size: 382.6 KB (382569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abf1699b7f712532e1c52400041c3cac70d15748da6008be064fd8079c6fd40`  
		Last Modified: Wed, 24 Jun 2026 01:46:00 GMT  
		Size: 338.8 KB (338754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f72ba21251a958d30a6b73bc738d047432036c794fc833b7b0f21bb77e23d5`  
		Last Modified: Wed, 24 Jun 2026 01:46:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee9883bcd6f5199cd1e4f0fb706d8bf2f12edf32903a1130ba9db387e5e7635`  
		Last Modified: Wed, 24 Jun 2026 01:46:04 GMT  
		Size: 110.5 MB (110474451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a15b9c4b1dd4da36e2a55a7d99596e53fb6b9e49556011dec18fa7279a5675d`  
		Last Modified: Wed, 24 Jun 2026 01:46:01 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0296e07dd1255baf3497c9bec73923346caa0078781774be87398df60c049d`  
		Last Modified: Wed, 24 Jun 2026 01:46:02 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbdfe6ea98ff36a0183910c32e21cc4c24ae6daec0a796c79764c7003ff21c0`  
		Last Modified: Wed, 24 Jun 2026 01:46:02 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87768653aa52520d0148009b743d1f4bb4208d3823d82c5c4729a8675d0bbb73`  
		Last Modified: Wed, 24 Jun 2026 01:46:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:2e3aea75ac902ad62649f52dad674240011a18bc5d8a35c6efaa8b78a22ef191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cff6de0fe65d5f070e7419be4529463bd15fd4ebe411a60aa94143041e2865a`

```dockerfile
```

-	Layers:
	-	`sha256:423f4c76bf94fe0a53f7180c4dccfcac2815cf31624db583c1b3f6aaab5f7f75`  
		Last Modified: Wed, 24 Jun 2026 01:46:00 GMT  
		Size: 4.2 MB (4180697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:391f250f12f470c2d1e19307a7d7020d0db34c3ca6e546585ce0b3d112b9762f`  
		Last Modified: Wed, 24 Jun 2026 01:46:00 GMT  
		Size: 31.9 KB (31882 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:46e19736e1f738038af63b073bac826a1c1002b5b12013557800728a7448f283
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:a4f81ea823e89814fd49342b7afaa10ec5484a088bd7b04431364d3decdfec59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150900912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066f2bd675e9f8eefe75ed8101f03c04593468ae1ba9fd0dab60ee09a3f28a61`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:41:46 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 01:41:46 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 24 Jun 2026 01:41:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:41:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-21-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 01:42:01 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 01:42:06 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:06 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ trixie main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 01:42:11 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --no-install-recommends couchdb-nouveau=3.5.2.1~trixie;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 24 Jun 2026 01:42:11 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 24 Jun 2026 01:42:11 GMT
VOLUME [/opt/nouveau/data]
# Wed, 24 Jun 2026 01:42:11 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 24 Jun 2026 01:42:11 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b4f3a550bbab7a60d55fe4084cdfb1461ec280fc6ebb368c7f7ff552d75b4f`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501acc060a5c6b292aae2516f814a1327c0172c7248a72eaefa6c94ca45b3ea4`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 7.5 MB (7492088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38a0a807b1c3e2ef8ac7093fe8ba8fbde384bc101830ec3a5f7bc06a80812cb`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 70.0 MB (70032502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90fb09798c8df22a655cd0d6e428703b97158dadbb5522427bff65bfe767b6ae`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 426.0 KB (425954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef8732e1e77f7f125f10e74108815945d28d1ef4c0214620b3871fd3440be62`  
		Last Modified: Wed, 24 Jun 2026 01:42:26 GMT  
		Size: 347.4 KB (347406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115e152bad6a028a7a5ba2099e6e2a2bbaeb01176aa328e5ab39a72496ba6af8`  
		Last Modified: Wed, 24 Jun 2026 01:42:26 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc568814ebcaf941d047d29b0ce94404c65a9c12eeea4474390818a991a1f329`  
		Last Modified: Wed, 24 Jun 2026 01:42:28 GMT  
		Size: 42.8 MB (42815670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871728428bcca3734b8e1fe6b9df1e0be4cded4f20c40b5fb5f27216c0bf984d`  
		Last Modified: Wed, 24 Jun 2026 01:42:28 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:bc251961f9e3fac2cd1ac06330d76fc2fe8157f19ee13bb6da811597e27843d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3389170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e5d71ae57d78ac9697623eddbe290111da65587ddbc7671cb8db1dc17332e2a`

```dockerfile
```

-	Layers:
	-	`sha256:9d4ad28e48e6b7218fbcf6f5f24c87bea7f88a8f0615675a064a7fb5e1be71cf`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 3.4 MB (3364655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0d2bf3efdfcf1edb20b2925aa4fd8ec8bb10f6be633c4c1bd26e32329caf959`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 24.5 KB (24515 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:88f01a2895ccbc2ad4a4809d08a4ab34bada1cf459b90e408f677594febdc495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150060849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17fe359bdea2848ec50aa9ef2d607cc2581d2ad6ad03913fb00c0e3620979107`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:45:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 01:45:19 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 24 Jun 2026 01:45:27 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:33 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-21-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 01:45:37 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 01:45:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ trixie main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 01:45:49 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --no-install-recommends couchdb-nouveau=3.5.2.1~trixie;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 24 Jun 2026 01:45:49 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 24 Jun 2026 01:45:49 GMT
VOLUME [/opt/nouveau/data]
# Wed, 24 Jun 2026 01:45:49 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 24 Jun 2026 01:45:49 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afed3b15d19dc54098462361bd70be3167d1b4a2056095f6ea6b457239e0404e`  
		Last Modified: Wed, 24 Jun 2026 01:46:04 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2154a32b22e91cd532570515930309f7dc6ac5e11a359590effab20c7e5c83`  
		Last Modified: Wed, 24 Jun 2026 01:46:04 GMT  
		Size: 7.3 MB (7261182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77072d82cc95086e1b40e56a00e632fcd1a25c76b2fcf3054b4b65fde807b15d`  
		Last Modified: Wed, 24 Jun 2026 01:46:05 GMT  
		Size: 69.2 MB (69179776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4c068d6f2d2e441939047e06caf8a0e5fbd716b233ae63fc3790ba33a01ee6`  
		Last Modified: Wed, 24 Jun 2026 01:46:04 GMT  
		Size: 390.3 KB (390257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00028a2c864bb7e8a1ac6b0b2696419d4a70a5e52c8e5504d8a301637f3e486b`  
		Last Modified: Wed, 24 Jun 2026 01:46:05 GMT  
		Size: 347.4 KB (347413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3296c6540ed840d3914cb6e0e5a60c4b39e81c98d16e191429647085082c4888`  
		Last Modified: Wed, 24 Jun 2026 01:46:05 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adaa48dc2c10bbb2e9cab0e15f705a1b59f9b434758e23de5f25d1c9c0e2315a`  
		Last Modified: Wed, 24 Jun 2026 01:46:07 GMT  
		Size: 42.7 MB (42731788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dade987fdbe20973e04a762797ca68cc6ef72feef621a5ce4f9df4d2c7ca6768`  
		Last Modified: Wed, 24 Jun 2026 01:46:06 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:49d26e1d18ca48370c6d10add80d541441bec9cb9843f3ad085e6e726ceb0abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3388017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3ed08f5407b481c2ccde6de9e4913fcd1fcd1d33d15e859e376f49659e5b5a`

```dockerfile
```

-	Layers:
	-	`sha256:6e7e4636b53e3343add9560359cbf01f9b18700b04aa67e3431e1fa07bec70ce`  
		Last Modified: Wed, 24 Jun 2026 01:46:04 GMT  
		Size: 3.4 MB (3363308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d42543e31bac53348e2864f384be3c0cb44ee069ec0cf0e34cbf29f4de874f7`  
		Last Modified: Wed, 24 Jun 2026 01:46:04 GMT  
		Size: 24.7 KB (24709 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4`

```console
$ docker pull couchdb@sha256:b1d84a34afba114d6e9f4fe3fad210e60eaaadab8fd9cd1d218d7d2cad663874
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
$ docker pull couchdb@sha256:6c5046c5e71559d43247120c8d2cb88e40ffa5155820e52b58238acdf9466f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139025765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0f3695187d24d1c4884f1b570ff032ecc37a1872fe78df3289571b02934cd0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:41:55 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 01:41:55 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 24 Jun 2026 01:42:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 01:42:03 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 01:42:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:07 GMT
ENV COUCHDB_VERSION=3.4.3
# Wed, 24 Jun 2026 01:42:07 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 01:42:20 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 24 Jun 2026 01:42:20 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 24 Jun 2026 01:42:20 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 24 Jun 2026 01:42:20 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 24 Jun 2026 01:42:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:42:20 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:42:20 GMT
VOLUME [/opt/couchdb/data]
# Wed, 24 Jun 2026 01:42:20 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 24 Jun 2026 01:42:20 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a7e9dddcaceb4ae46ab993ad4dde748a920aee3f2c65009f2846c2856f9c6e`  
		Last Modified: Wed, 24 Jun 2026 01:42:33 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609d850789af8f7bf837bdc26e3183c08cf4bbb04d8aef88481a85388b1ba607`  
		Last Modified: Wed, 24 Jun 2026 01:42:33 GMT  
		Size: 7.9 MB (7884360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e2dd308906c78bcbaf32250f34c3a878a859a0770a9d8aaf79c0ca9e4ed4e9`  
		Last Modified: Wed, 24 Jun 2026 01:42:33 GMT  
		Size: 401.8 KB (401780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f364d64a056ed9ae609a36b63604ff2adb1cb4a52bee407ee7d4a6fab5a823`  
		Last Modified: Wed, 24 Jun 2026 01:42:33 GMT  
		Size: 76.5 KB (76477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502a29388f3637bfb5a66dcd70786551e66372cc96fe5557fe6964ffc7e9cf03`  
		Last Modified: Wed, 24 Jun 2026 01:42:34 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3315bf91ee656ef13cb64342c6cb8a8f1e169c28d5a1dff4dbf222737d1773bb`  
		Last Modified: Wed, 24 Jun 2026 01:42:37 GMT  
		Size: 102.4 MB (102420072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae451b4e5e7897443e48a95d0f8c01e158f562928a1ecf6c6e82f757267d7e4`  
		Last Modified: Wed, 24 Jun 2026 01:42:34 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf69c505fa71b86bf6dda2dbb714ee276a7a7b8d38e8fcdd2aa8368f09357c3e`  
		Last Modified: Wed, 24 Jun 2026 01:42:34 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac33719b5de063d014d61d41eb8f7715970f3a0aa989332bafc8f4b58906fb8`  
		Last Modified: Wed, 24 Jun 2026 01:42:35 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45bbba1e489a6af08c5fa86ad2f9f14fe2e94e0d24420fafc1b202a092c2690`  
		Last Modified: Wed, 24 Jun 2026 01:42:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:11fcf65d96cbc7b98be04221d78f53163817a408f9512d9f37ad81002690f172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b661c8c6e786e985007005388f98df0b8c1a7dc6ca917c9e1ab90ac551eb9017`

```dockerfile
```

-	Layers:
	-	`sha256:24892a59691d3dca135a945bb9ef1a05981c542ab8196dbde25a0d4ced1d3ffe`  
		Last Modified: Wed, 24 Jun 2026 01:42:33 GMT  
		Size: 4.1 MB (4125431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50e0984901f8f8bc511de0f1a23678d63f272e15c6af91f4bc089f263b87bc3e`  
		Last Modified: Wed, 24 Jun 2026 01:42:32 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:69feeb09f54ae3bbdaadd50e0ac1344b5dd8dff03c8413349ff5b6b4bc949b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138439983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd052eb35dd25dd468f114941fc64d5fc47a9f5c8c1cd54697faf2d942ba11a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:45:23 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 01:45:23 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 24 Jun 2026 01:45:30 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 01:45:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 01:45:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:38 GMT
ENV COUCHDB_VERSION=3.4.3
# Wed, 24 Jun 2026 01:45:38 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 01:45:50 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 24 Jun 2026 01:45:50 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 24 Jun 2026 01:45:50 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 24 Jun 2026 01:45:50 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 24 Jun 2026 01:45:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:45:51 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:45:51 GMT
VOLUME [/opt/couchdb/data]
# Wed, 24 Jun 2026 01:45:51 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 24 Jun 2026 01:45:51 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e101bc9f32b2805af9cc873b8fbe2b938f8985decfa30d5f0ec4618765298b1`  
		Last Modified: Wed, 24 Jun 2026 01:46:06 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56d7a078dd4ae02386cdad07635fb8b88207ed1d6b8ede36a7e0b291c9b0d8d`  
		Last Modified: Wed, 24 Jun 2026 01:46:06 GMT  
		Size: 7.7 MB (7695580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfa424fc62e28cd749d61117d5a2ea67ebec9c052241984eb1568958d84b96e`  
		Last Modified: Wed, 24 Jun 2026 01:46:06 GMT  
		Size: 370.6 KB (370550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4682dcbcf40051f7cc07d160c3374440c5d13fe0a1e91ae0d259e2a8302b1f`  
		Last Modified: Wed, 24 Jun 2026 01:46:07 GMT  
		Size: 76.5 KB (76536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88372eeb9cfebfd709c34a3a1f8b0ecfbd4a70ba66d0974e0992ace476c16f53`  
		Last Modified: Wed, 24 Jun 2026 01:46:08 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0b4fb7db8a6727888ba8408a2437a4129bbaead1f9af660408a5eba5561127`  
		Last Modified: Wed, 24 Jun 2026 01:46:11 GMT  
		Size: 102.2 MB (102169471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb7217f6a1690a538a7f3913a0ae652e1ba86470a00bf11373e143f3ce87e79`  
		Last Modified: Wed, 24 Jun 2026 01:46:08 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067c3d052cc37ac2681f6f903b4405f456e0d284fe06dc3a1581e13fc1044dca`  
		Last Modified: Wed, 24 Jun 2026 01:46:08 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dfdbc26218958e01a38c92372b34a7537a9f16167e15a2ce806885a45e21312`  
		Last Modified: Wed, 24 Jun 2026 01:46:09 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fbd9f42094b3776bcaadc87c0505aa866592965f329f9a6644a13a61685f19`  
		Last Modified: Wed, 24 Jun 2026 01:46:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:6ac8f28761840fd7a4db90971e540e861a797ece9a76f20d5235d0347a0a8885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4157018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71f85b84bfefce1d824c332253393559a86dff302043eed7fd499b8e2a3f062e`

```dockerfile
```

-	Layers:
	-	`sha256:326731787f4c9ab5bd57c742537031f7489e5bfe814368ba4cd5897fa6a97500`  
		Last Modified: Wed, 24 Jun 2026 01:46:07 GMT  
		Size: 4.1 MB (4125700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a3edeea7bfe170edce1f371c4fd3f15e1a1729ade93e20f84ca7137b926fc9d`  
		Last Modified: Wed, 24 Jun 2026 01:46:06 GMT  
		Size: 31.3 KB (31318 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; s390x

```console
$ docker pull couchdb@sha256:944ffe7706b9190f28ea763cb14210f7995f0ef9e94a39375b8e44e2c12da149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135804777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31901e766b8cfcb28ae354d0a8531dbb6cc7d6007d21e22ac5462ebdc7b17b3`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:46:24 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 02:46:24 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 24 Jun 2026 02:46:30 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:46:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 02:46:33 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 02:46:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:46:38 GMT
ENV COUCHDB_VERSION=3.4.3
# Wed, 24 Jun 2026 02:46:38 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 02:46:55 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 24 Jun 2026 02:46:56 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 24 Jun 2026 02:46:56 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 24 Jun 2026 02:46:56 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 24 Jun 2026 02:46:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 02:46:56 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:46:56 GMT
VOLUME [/opt/couchdb/data]
# Wed, 24 Jun 2026 02:46:56 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 24 Jun 2026 02:46:56 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:e9aeeda7513dde59469463716e9e14f36210d6570c3cad5e5440b32d941733cd`  
		Last Modified: Wed, 24 Jun 2026 00:27:21 GMT  
		Size: 26.9 MB (26893585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c74692a8c1f4356abe88429f627fd6b302f6f73952b95d71b04569b79dc6c6`  
		Last Modified: Wed, 24 Jun 2026 02:47:16 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a44e034a2e5b15aeb96ce5473cdf2d322c1c3da7424bfa8a501a5a829b686b1`  
		Last Modified: Wed, 24 Jun 2026 02:47:17 GMT  
		Size: 7.4 MB (7400241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a512d7ee7f021226d1a5f24e929b0f155040e189302657566cca875db2956ba`  
		Last Modified: Wed, 24 Jun 2026 02:47:16 GMT  
		Size: 372.2 KB (372163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed82bc36abb2bd092c5c734e96c3302b9454f639465572e632ebd3a84d0115c`  
		Last Modified: Wed, 24 Jun 2026 02:47:16 GMT  
		Size: 76.6 KB (76561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd9d835f4fab2a7b392bf2531caea1b576fe8f461bce2784bcc35599124cbf2`  
		Last Modified: Wed, 24 Jun 2026 02:47:17 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426265479a0f717d0e9bf0518216548ebbc6e250a12f07f84b634f0eb5752aee`  
		Last Modified: Wed, 24 Jun 2026 02:47:20 GMT  
		Size: 101.1 MB (101056797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d444136e52d33b379d93d2cc02b4e14a558181d3b9bcd843f9e6fe84dfab55`  
		Last Modified: Wed, 24 Jun 2026 02:47:18 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af920742abefb95b12c6fbb530efe765248948f0e620e08fbd59690e9f25a0d2`  
		Last Modified: Wed, 24 Jun 2026 02:47:18 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d86e99b1478db4f20a19804afb135333f7ab7bc313a4cd224e8de4d39e267ed`  
		Last Modified: Wed, 24 Jun 2026 02:47:19 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663ff4ede45caf34f6004d8566ba4abfbea9253226272723ae64888bdafb7abe`  
		Last Modified: Wed, 24 Jun 2026 02:47:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:2fc360f7ad0f86472acf7286b2b4e54e45f730dfc9c9062c1094e191aad9e253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a69249aa1ff2a90be0fc30a76bfd2ed3ffcdcae0b05a91f55bc89be9adae8b`

```dockerfile
```

-	Layers:
	-	`sha256:075451d8e58ce370d95c940192f581b11e58f0ac036932a6921d2bf4ac912455`  
		Last Modified: Wed, 24 Jun 2026 02:47:16 GMT  
		Size: 4.1 MB (4121627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c35576e828da9763b750c1a355f0428ae7eb253bc7c242491801f9203c0f2b4`  
		Last Modified: Wed, 24 Jun 2026 02:47:16 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4-nouveau`

```console
$ docker pull couchdb@sha256:7ae5ba7358f7024ca4a6a40b1f27a79796b84e16bc5922df644bea43e80908c5
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
$ docker pull couchdb@sha256:cc9b3be27ab36ddb3b29e5747ef2bc2dd320b2d819e02d372232a765632771cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.6 MB (156561204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299345f2f4e404d10d894b00f4ec5912eb8f712eb2c92be52da8b74ac12a5be1`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:42:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 01:42:08 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 24 Jun 2026 01:42:15 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:22 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 01:42:25 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 01:42:29 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:29 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 01:42:33 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 24 Jun 2026 01:42:34 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 24 Jun 2026 01:42:34 GMT
VOLUME [/opt/nouveau/data]
# Wed, 24 Jun 2026 01:42:34 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 24 Jun 2026 01:42:34 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4e082a827213656d819e35a25d5e435bb7935cc2652958e1fc78a50f8a1208`  
		Last Modified: Wed, 24 Jun 2026 01:42:49 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7f581f923ae5bc7db932a63377062178c8cb8bf01cbddbc55c4a20f5db385e`  
		Last Modified: Wed, 24 Jun 2026 01:42:50 GMT  
		Size: 7.9 MB (7884338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1855dcbd232eb8f3abff21fa8f607de64bb3925091e8c0f2007287e14ef0aa2f`  
		Last Modified: Wed, 24 Jun 2026 01:42:52 GMT  
		Size: 77.5 MB (77477845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a66ec35499463ebbc4dd500a66e4351553ac59bec84998b1c2779fceace47f6`  
		Last Modified: Wed, 24 Jun 2026 01:42:50 GMT  
		Size: 424.1 KB (424140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b7c01d8c31ceb84a2f9759f4b15d7d8bfbacd23884bc8682a262bb5b01bc66`  
		Last Modified: Wed, 24 Jun 2026 01:42:51 GMT  
		Size: 99.6 KB (99592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bfc78b7a7af23034d4c2cff48545faf054087a21d51936822d339eded093f0`  
		Last Modified: Wed, 24 Jun 2026 01:42:51 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92cd722f7f3474b05eaa3170813628e30a9f7d4852d1564ea129eee87998cbf`  
		Last Modified: Wed, 24 Jun 2026 01:42:53 GMT  
		Size: 42.4 MB (42435771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38e460ad23878163f8f38587cced6d70081b37e0d6dfdc7a7f58412dc4a4ce1`  
		Last Modified: Wed, 24 Jun 2026 01:42:53 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:b228fa9269fd3b9a929356c90a82b04572db4fc8208f084b9a9d770a28e7aab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b38f210d53a9f63d9e85cbbdf424221ce2981b982eda86677418501414a72d`

```dockerfile
```

-	Layers:
	-	`sha256:7489782a4f9c466ed9c86dbb3d0dc731b0ac9058d8b03043c2aaf6e438d11287`  
		Last Modified: Wed, 24 Jun 2026 01:42:50 GMT  
		Size: 3.7 MB (3658671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8acc8b7f976d3ec1c9d3f62e3f154792332212a46e7c7ecb76fcfafbb8392c7`  
		Last Modified: Wed, 24 Jun 2026 01:42:49 GMT  
		Size: 24.2 KB (24214 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:2f251695136cbb6735b3e195a3bab1127b13b0e8710bad39ef27508666d9f0aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155443657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2975e631cdb54c26d3ebab103126963651fdd9b0e7fde7f2eada08956bc7d81f`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:45:32 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 01:45:32 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 24 Jun 2026 01:45:39 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 01:45:49 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 01:45:53 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:53 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 01:45:58 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 24 Jun 2026 01:45:58 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 24 Jun 2026 01:45:58 GMT
VOLUME [/opt/nouveau/data]
# Wed, 24 Jun 2026 01:45:58 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 24 Jun 2026 01:45:58 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521c24b6ce6ee1717c396669b0b31f219f196b8ae1808794a608188609902b6d`  
		Last Modified: Wed, 24 Jun 2026 01:46:14 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca378e46b6999a8ccb73a520f186772840f56ed550aa0ddeb7be85bf3f91276`  
		Last Modified: Wed, 24 Jun 2026 01:46:14 GMT  
		Size: 7.7 MB (7695553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f468a2f17d0696c5056857cba74db5e74595bec6276942cb282d57c1d559b28`  
		Last Modified: Wed, 24 Jun 2026 01:46:16 GMT  
		Size: 76.8 MB (76793406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4557430451bd3914a75738f21196bfced787420f78fed484bf47e828de1e88c4`  
		Last Modified: Wed, 24 Jun 2026 01:46:14 GMT  
		Size: 392.8 KB (392801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3ad80377e9251007fc729c81a8173596d15f6f9f6023196e440a0593b5a680`  
		Last Modified: Wed, 24 Jun 2026 01:46:15 GMT  
		Size: 99.5 KB (99531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2240fdf4a1d8899fb7e547663566289c9ef7696603084e719b81e07ac44b267c`  
		Last Modified: Wed, 24 Jun 2026 01:46:15 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fe4e492fe44fd32f1b56d663dcf866ee42fbb3563ba33bb50b07d2c7b26ef7`  
		Last Modified: Wed, 24 Jun 2026 01:46:17 GMT  
		Size: 42.3 MB (42338066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4384862444dd8af9bfbd1da7cea122c9faae782afdb58b4c35308bed0f900b`  
		Last Modified: Wed, 24 Jun 2026 01:46:16 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:03a9282b880bf10dcaf5e8bf6c101ebd382681ea8958125b2f249ae8a9e97047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0dfb06876ae5bad10252876674413417a073003a52f52e9ace022da1e3b8ad9`

```dockerfile
```

-	Layers:
	-	`sha256:724fe05d6b339d5d9ea1ac9c9fb3d25fdfbd444087dd2bdb05894ea96acd8565`  
		Last Modified: Wed, 24 Jun 2026 01:46:14 GMT  
		Size: 3.7 MB (3657339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7db9801e984309cd27374fe144be58749aa2d531118de86de16f9dd3f565301e`  
		Last Modified: Wed, 24 Jun 2026 01:46:13 GMT  
		Size: 24.4 KB (24385 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:5da3f6a6a5db3f9bd7d1cfea6f5c66773f8d777aa4b480743794afc00c2c921b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.2 MB (150178075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8bf166913572b785e904d38e406ef9d27585473fb6a7d757a3f4b4927a47f15`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:46:31 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 02:46:31 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 24 Jun 2026 02:46:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:46:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:46:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 02:46:48 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 02:46:52 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:46:52 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 02:47:00 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 24 Jun 2026 02:47:00 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 24 Jun 2026 02:47:00 GMT
VOLUME [/opt/nouveau/data]
# Wed, 24 Jun 2026 02:47:00 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 24 Jun 2026 02:47:00 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:e9aeeda7513dde59469463716e9e14f36210d6570c3cad5e5440b32d941733cd`  
		Last Modified: Wed, 24 Jun 2026 00:27:21 GMT  
		Size: 26.9 MB (26893585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183c4c35f9774ecad1c3bad431f618287d5d25f795c2abdf32ebcab26128efef`  
		Last Modified: Wed, 24 Jun 2026 02:47:23 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059ff1c6e29c8344a8a59c5641838b7636b539ede46fa83ae2c13dfcb1e4958e`  
		Last Modified: Wed, 24 Jun 2026 02:47:23 GMT  
		Size: 7.4 MB (7400193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd709311124fab46ec7c9282d0c30a5d6a479ca082c744135d182ee9d81b1748`  
		Last Modified: Wed, 24 Jun 2026 02:47:24 GMT  
		Size: 73.2 MB (73225361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87813195098071fe74d5d1ac69a2dcca169b13019de131fa6260734e740d5068`  
		Last Modified: Wed, 24 Jun 2026 02:47:23 GMT  
		Size: 394.5 KB (394518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abdcf0dde2ac53ff144117390f118341c362a4a599d223d8f3f361d7bf6e4969`  
		Last Modified: Wed, 24 Jun 2026 02:47:24 GMT  
		Size: 99.7 KB (99687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98f10795ec0711c6fb1c1c2d9aaf02a8135b77ce56fb1448fda05b4d13a7717`  
		Last Modified: Wed, 24 Jun 2026 02:47:24 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aaabca7f1103b56ac333a0be1240140af54cd0ed33fc57c0ad749c6b3adc633`  
		Last Modified: Wed, 24 Jun 2026 02:47:25 GMT  
		Size: 42.2 MB (42162856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b27e6fcecf7b713c53863d2b5bd48f86d03d5b195fa8e6051741d0bce49c3d2`  
		Last Modified: Wed, 24 Jun 2026 02:47:25 GMT  
		Size: 415.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:6ff4682ef484e2f8e1ebb2ce54f44b3cebd2895336a188c5b714fc0d61c440cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de6284d11fb18093a35538214885a90f057e29e3ca45e48caca07259686fb31`

```dockerfile
```

-	Layers:
	-	`sha256:be79239d219b209b9d2f18f33d324866a220b298b9ccbea8d10047d5f8923441`  
		Last Modified: Wed, 24 Jun 2026 02:47:23 GMT  
		Size: 3.6 MB (3649204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d63773d4b69bde66025c54ba37e5906bed3b59835ac891ec8f2c451730179eb`  
		Last Modified: Wed, 24 Jun 2026 02:47:23 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3`

```console
$ docker pull couchdb@sha256:b1d84a34afba114d6e9f4fe3fad210e60eaaadab8fd9cd1d218d7d2cad663874
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.4.3` - linux; amd64

```console
$ docker pull couchdb@sha256:6c5046c5e71559d43247120c8d2cb88e40ffa5155820e52b58238acdf9466f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139025765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0f3695187d24d1c4884f1b570ff032ecc37a1872fe78df3289571b02934cd0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:41:55 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 01:41:55 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 24 Jun 2026 01:42:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:03 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 01:42:03 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 01:42:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:07 GMT
ENV COUCHDB_VERSION=3.4.3
# Wed, 24 Jun 2026 01:42:07 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 01:42:20 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 24 Jun 2026 01:42:20 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 24 Jun 2026 01:42:20 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 24 Jun 2026 01:42:20 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 24 Jun 2026 01:42:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:42:20 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:42:20 GMT
VOLUME [/opt/couchdb/data]
# Wed, 24 Jun 2026 01:42:20 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 24 Jun 2026 01:42:20 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a7e9dddcaceb4ae46ab993ad4dde748a920aee3f2c65009f2846c2856f9c6e`  
		Last Modified: Wed, 24 Jun 2026 01:42:33 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609d850789af8f7bf837bdc26e3183c08cf4bbb04d8aef88481a85388b1ba607`  
		Last Modified: Wed, 24 Jun 2026 01:42:33 GMT  
		Size: 7.9 MB (7884360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e2dd308906c78bcbaf32250f34c3a878a859a0770a9d8aaf79c0ca9e4ed4e9`  
		Last Modified: Wed, 24 Jun 2026 01:42:33 GMT  
		Size: 401.8 KB (401780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f364d64a056ed9ae609a36b63604ff2adb1cb4a52bee407ee7d4a6fab5a823`  
		Last Modified: Wed, 24 Jun 2026 01:42:33 GMT  
		Size: 76.5 KB (76477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502a29388f3637bfb5a66dcd70786551e66372cc96fe5557fe6964ffc7e9cf03`  
		Last Modified: Wed, 24 Jun 2026 01:42:34 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3315bf91ee656ef13cb64342c6cb8a8f1e169c28d5a1dff4dbf222737d1773bb`  
		Last Modified: Wed, 24 Jun 2026 01:42:37 GMT  
		Size: 102.4 MB (102420072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae451b4e5e7897443e48a95d0f8c01e158f562928a1ecf6c6e82f757267d7e4`  
		Last Modified: Wed, 24 Jun 2026 01:42:34 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf69c505fa71b86bf6dda2dbb714ee276a7a7b8d38e8fcdd2aa8368f09357c3e`  
		Last Modified: Wed, 24 Jun 2026 01:42:34 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac33719b5de063d014d61d41eb8f7715970f3a0aa989332bafc8f4b58906fb8`  
		Last Modified: Wed, 24 Jun 2026 01:42:35 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45bbba1e489a6af08c5fa86ad2f9f14fe2e94e0d24420fafc1b202a092c2690`  
		Last Modified: Wed, 24 Jun 2026 01:42:35 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:11fcf65d96cbc7b98be04221d78f53163817a408f9512d9f37ad81002690f172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b661c8c6e786e985007005388f98df0b8c1a7dc6ca917c9e1ab90ac551eb9017`

```dockerfile
```

-	Layers:
	-	`sha256:24892a59691d3dca135a945bb9ef1a05981c542ab8196dbde25a0d4ced1d3ffe`  
		Last Modified: Wed, 24 Jun 2026 01:42:33 GMT  
		Size: 4.1 MB (4125431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50e0984901f8f8bc511de0f1a23678d63f272e15c6af91f4bc089f263b87bc3e`  
		Last Modified: Wed, 24 Jun 2026 01:42:32 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:69feeb09f54ae3bbdaadd50e0ac1344b5dd8dff03c8413349ff5b6b4bc949b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138439983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd052eb35dd25dd468f114941fc64d5fc47a9f5c8c1cd54697faf2d942ba11a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:45:23 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 01:45:23 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 24 Jun 2026 01:45:30 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 01:45:32 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 01:45:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:38 GMT
ENV COUCHDB_VERSION=3.4.3
# Wed, 24 Jun 2026 01:45:38 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 01:45:50 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 24 Jun 2026 01:45:50 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 24 Jun 2026 01:45:50 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 24 Jun 2026 01:45:50 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 24 Jun 2026 01:45:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:45:51 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:45:51 GMT
VOLUME [/opt/couchdb/data]
# Wed, 24 Jun 2026 01:45:51 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 24 Jun 2026 01:45:51 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e101bc9f32b2805af9cc873b8fbe2b938f8985decfa30d5f0ec4618765298b1`  
		Last Modified: Wed, 24 Jun 2026 01:46:06 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56d7a078dd4ae02386cdad07635fb8b88207ed1d6b8ede36a7e0b291c9b0d8d`  
		Last Modified: Wed, 24 Jun 2026 01:46:06 GMT  
		Size: 7.7 MB (7695580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfa424fc62e28cd749d61117d5a2ea67ebec9c052241984eb1568958d84b96e`  
		Last Modified: Wed, 24 Jun 2026 01:46:06 GMT  
		Size: 370.6 KB (370550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4682dcbcf40051f7cc07d160c3374440c5d13fe0a1e91ae0d259e2a8302b1f`  
		Last Modified: Wed, 24 Jun 2026 01:46:07 GMT  
		Size: 76.5 KB (76536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88372eeb9cfebfd709c34a3a1f8b0ecfbd4a70ba66d0974e0992ace476c16f53`  
		Last Modified: Wed, 24 Jun 2026 01:46:08 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0b4fb7db8a6727888ba8408a2437a4129bbaead1f9af660408a5eba5561127`  
		Last Modified: Wed, 24 Jun 2026 01:46:11 GMT  
		Size: 102.2 MB (102169471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb7217f6a1690a538a7f3913a0ae652e1ba86470a00bf11373e143f3ce87e79`  
		Last Modified: Wed, 24 Jun 2026 01:46:08 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067c3d052cc37ac2681f6f903b4405f456e0d284fe06dc3a1581e13fc1044dca`  
		Last Modified: Wed, 24 Jun 2026 01:46:08 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dfdbc26218958e01a38c92372b34a7537a9f16167e15a2ce806885a45e21312`  
		Last Modified: Wed, 24 Jun 2026 01:46:09 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fbd9f42094b3776bcaadc87c0505aa866592965f329f9a6644a13a61685f19`  
		Last Modified: Wed, 24 Jun 2026 01:46:10 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:6ac8f28761840fd7a4db90971e540e861a797ece9a76f20d5235d0347a0a8885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4157018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71f85b84bfefce1d824c332253393559a86dff302043eed7fd499b8e2a3f062e`

```dockerfile
```

-	Layers:
	-	`sha256:326731787f4c9ab5bd57c742537031f7489e5bfe814368ba4cd5897fa6a97500`  
		Last Modified: Wed, 24 Jun 2026 01:46:07 GMT  
		Size: 4.1 MB (4125700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a3edeea7bfe170edce1f371c4fd3f15e1a1729ade93e20f84ca7137b926fc9d`  
		Last Modified: Wed, 24 Jun 2026 01:46:06 GMT  
		Size: 31.3 KB (31318 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; s390x

```console
$ docker pull couchdb@sha256:944ffe7706b9190f28ea763cb14210f7995f0ef9e94a39375b8e44e2c12da149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135804777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31901e766b8cfcb28ae354d0a8531dbb6cc7d6007d21e22ac5462ebdc7b17b3`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:46:24 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 02:46:24 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 24 Jun 2026 02:46:30 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:46:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 02:46:33 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 02:46:38 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:46:38 GMT
ENV COUCHDB_VERSION=3.4.3
# Wed, 24 Jun 2026 02:46:38 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 02:46:55 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 24 Jun 2026 02:46:56 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 24 Jun 2026 02:46:56 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 24 Jun 2026 02:46:56 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 24 Jun 2026 02:46:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 02:46:56 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:46:56 GMT
VOLUME [/opt/couchdb/data]
# Wed, 24 Jun 2026 02:46:56 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 24 Jun 2026 02:46:56 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:e9aeeda7513dde59469463716e9e14f36210d6570c3cad5e5440b32d941733cd`  
		Last Modified: Wed, 24 Jun 2026 00:27:21 GMT  
		Size: 26.9 MB (26893585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c74692a8c1f4356abe88429f627fd6b302f6f73952b95d71b04569b79dc6c6`  
		Last Modified: Wed, 24 Jun 2026 02:47:16 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a44e034a2e5b15aeb96ce5473cdf2d322c1c3da7424bfa8a501a5a829b686b1`  
		Last Modified: Wed, 24 Jun 2026 02:47:17 GMT  
		Size: 7.4 MB (7400241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a512d7ee7f021226d1a5f24e929b0f155040e189302657566cca875db2956ba`  
		Last Modified: Wed, 24 Jun 2026 02:47:16 GMT  
		Size: 372.2 KB (372163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed82bc36abb2bd092c5c734e96c3302b9454f639465572e632ebd3a84d0115c`  
		Last Modified: Wed, 24 Jun 2026 02:47:16 GMT  
		Size: 76.6 KB (76561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd9d835f4fab2a7b392bf2531caea1b576fe8f461bce2784bcc35599124cbf2`  
		Last Modified: Wed, 24 Jun 2026 02:47:17 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426265479a0f717d0e9bf0518216548ebbc6e250a12f07f84b634f0eb5752aee`  
		Last Modified: Wed, 24 Jun 2026 02:47:20 GMT  
		Size: 101.1 MB (101056797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d444136e52d33b379d93d2cc02b4e14a558181d3b9bcd843f9e6fe84dfab55`  
		Last Modified: Wed, 24 Jun 2026 02:47:18 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af920742abefb95b12c6fbb530efe765248948f0e620e08fbd59690e9f25a0d2`  
		Last Modified: Wed, 24 Jun 2026 02:47:18 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d86e99b1478db4f20a19804afb135333f7ab7bc313a4cd224e8de4d39e267ed`  
		Last Modified: Wed, 24 Jun 2026 02:47:19 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663ff4ede45caf34f6004d8566ba4abfbea9253226272723ae64888bdafb7abe`  
		Last Modified: Wed, 24 Jun 2026 02:47:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:2fc360f7ad0f86472acf7286b2b4e54e45f730dfc9c9062c1094e191aad9e253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a69249aa1ff2a90be0fc30a76bfd2ed3ffcdcae0b05a91f55bc89be9adae8b`

```dockerfile
```

-	Layers:
	-	`sha256:075451d8e58ce370d95c940192f581b11e58f0ac036932a6921d2bf4ac912455`  
		Last Modified: Wed, 24 Jun 2026 02:47:16 GMT  
		Size: 4.1 MB (4121627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c35576e828da9763b750c1a355f0428ae7eb253bc7c242491801f9203c0f2b4`  
		Last Modified: Wed, 24 Jun 2026 02:47:16 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3-nouveau`

```console
$ docker pull couchdb@sha256:7ae5ba7358f7024ca4a6a40b1f27a79796b84e16bc5922df644bea43e80908c5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.4.3-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:cc9b3be27ab36ddb3b29e5747ef2bc2dd320b2d819e02d372232a765632771cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.6 MB (156561204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299345f2f4e404d10d894b00f4ec5912eb8f712eb2c92be52da8b74ac12a5be1`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:42:08 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 01:42:08 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 24 Jun 2026 01:42:15 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:22 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 01:42:25 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 01:42:29 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:29 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 01:42:33 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 24 Jun 2026 01:42:34 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 24 Jun 2026 01:42:34 GMT
VOLUME [/opt/nouveau/data]
# Wed, 24 Jun 2026 01:42:34 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 24 Jun 2026 01:42:34 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4e082a827213656d819e35a25d5e435bb7935cc2652958e1fc78a50f8a1208`  
		Last Modified: Wed, 24 Jun 2026 01:42:49 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7f581f923ae5bc7db932a63377062178c8cb8bf01cbddbc55c4a20f5db385e`  
		Last Modified: Wed, 24 Jun 2026 01:42:50 GMT  
		Size: 7.9 MB (7884338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1855dcbd232eb8f3abff21fa8f607de64bb3925091e8c0f2007287e14ef0aa2f`  
		Last Modified: Wed, 24 Jun 2026 01:42:52 GMT  
		Size: 77.5 MB (77477845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a66ec35499463ebbc4dd500a66e4351553ac59bec84998b1c2779fceace47f6`  
		Last Modified: Wed, 24 Jun 2026 01:42:50 GMT  
		Size: 424.1 KB (424140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b7c01d8c31ceb84a2f9759f4b15d7d8bfbacd23884bc8682a262bb5b01bc66`  
		Last Modified: Wed, 24 Jun 2026 01:42:51 GMT  
		Size: 99.6 KB (99592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bfc78b7a7af23034d4c2cff48545faf054087a21d51936822d339eded093f0`  
		Last Modified: Wed, 24 Jun 2026 01:42:51 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92cd722f7f3474b05eaa3170813628e30a9f7d4852d1564ea129eee87998cbf`  
		Last Modified: Wed, 24 Jun 2026 01:42:53 GMT  
		Size: 42.4 MB (42435771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38e460ad23878163f8f38587cced6d70081b37e0d6dfdc7a7f58412dc4a4ce1`  
		Last Modified: Wed, 24 Jun 2026 01:42:53 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:b228fa9269fd3b9a929356c90a82b04572db4fc8208f084b9a9d770a28e7aab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b38f210d53a9f63d9e85cbbdf424221ce2981b982eda86677418501414a72d`

```dockerfile
```

-	Layers:
	-	`sha256:7489782a4f9c466ed9c86dbb3d0dc731b0ac9058d8b03043c2aaf6e438d11287`  
		Last Modified: Wed, 24 Jun 2026 01:42:50 GMT  
		Size: 3.7 MB (3658671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8acc8b7f976d3ec1c9d3f62e3f154792332212a46e7c7ecb76fcfafbb8392c7`  
		Last Modified: Wed, 24 Jun 2026 01:42:49 GMT  
		Size: 24.2 KB (24214 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:2f251695136cbb6735b3e195a3bab1127b13b0e8710bad39ef27508666d9f0aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155443657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2975e631cdb54c26d3ebab103126963651fdd9b0e7fde7f2eada08956bc7d81f`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:45:32 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 01:45:32 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 24 Jun 2026 01:45:39 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:46 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:49 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 01:45:49 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 01:45:53 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:53 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 01:45:58 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 24 Jun 2026 01:45:58 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 24 Jun 2026 01:45:58 GMT
VOLUME [/opt/nouveau/data]
# Wed, 24 Jun 2026 01:45:58 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 24 Jun 2026 01:45:58 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521c24b6ce6ee1717c396669b0b31f219f196b8ae1808794a608188609902b6d`  
		Last Modified: Wed, 24 Jun 2026 01:46:14 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca378e46b6999a8ccb73a520f186772840f56ed550aa0ddeb7be85bf3f91276`  
		Last Modified: Wed, 24 Jun 2026 01:46:14 GMT  
		Size: 7.7 MB (7695553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f468a2f17d0696c5056857cba74db5e74595bec6276942cb282d57c1d559b28`  
		Last Modified: Wed, 24 Jun 2026 01:46:16 GMT  
		Size: 76.8 MB (76793406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4557430451bd3914a75738f21196bfced787420f78fed484bf47e828de1e88c4`  
		Last Modified: Wed, 24 Jun 2026 01:46:14 GMT  
		Size: 392.8 KB (392801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3ad80377e9251007fc729c81a8173596d15f6f9f6023196e440a0593b5a680`  
		Last Modified: Wed, 24 Jun 2026 01:46:15 GMT  
		Size: 99.5 KB (99531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2240fdf4a1d8899fb7e547663566289c9ef7696603084e719b81e07ac44b267c`  
		Last Modified: Wed, 24 Jun 2026 01:46:15 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fe4e492fe44fd32f1b56d663dcf866ee42fbb3563ba33bb50b07d2c7b26ef7`  
		Last Modified: Wed, 24 Jun 2026 01:46:17 GMT  
		Size: 42.3 MB (42338066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4384862444dd8af9bfbd1da7cea122c9faae782afdb58b4c35308bed0f900b`  
		Last Modified: Wed, 24 Jun 2026 01:46:16 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:03a9282b880bf10dcaf5e8bf6c101ebd382681ea8958125b2f249ae8a9e97047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0dfb06876ae5bad10252876674413417a073003a52f52e9ace022da1e3b8ad9`

```dockerfile
```

-	Layers:
	-	`sha256:724fe05d6b339d5d9ea1ac9c9fb3d25fdfbd444087dd2bdb05894ea96acd8565`  
		Last Modified: Wed, 24 Jun 2026 01:46:14 GMT  
		Size: 3.7 MB (3657339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7db9801e984309cd27374fe144be58749aa2d531118de86de16f9dd3f565301e`  
		Last Modified: Wed, 24 Jun 2026 01:46:13 GMT  
		Size: 24.4 KB (24385 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:5da3f6a6a5db3f9bd7d1cfea6f5c66773f8d777aa4b480743794afc00c2c921b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.2 MB (150178075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8bf166913572b785e904d38e406ef9d27585473fb6a7d757a3f4b4927a47f15`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:46:31 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 02:46:31 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 24 Jun 2026 02:46:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:46:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:46:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 02:46:48 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 02:46:52 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:46:52 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 02:47:00 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 24 Jun 2026 02:47:00 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 24 Jun 2026 02:47:00 GMT
VOLUME [/opt/nouveau/data]
# Wed, 24 Jun 2026 02:47:00 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 24 Jun 2026 02:47:00 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:e9aeeda7513dde59469463716e9e14f36210d6570c3cad5e5440b32d941733cd`  
		Last Modified: Wed, 24 Jun 2026 00:27:21 GMT  
		Size: 26.9 MB (26893585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183c4c35f9774ecad1c3bad431f618287d5d25f795c2abdf32ebcab26128efef`  
		Last Modified: Wed, 24 Jun 2026 02:47:23 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059ff1c6e29c8344a8a59c5641838b7636b539ede46fa83ae2c13dfcb1e4958e`  
		Last Modified: Wed, 24 Jun 2026 02:47:23 GMT  
		Size: 7.4 MB (7400193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd709311124fab46ec7c9282d0c30a5d6a479ca082c744135d182ee9d81b1748`  
		Last Modified: Wed, 24 Jun 2026 02:47:24 GMT  
		Size: 73.2 MB (73225361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87813195098071fe74d5d1ac69a2dcca169b13019de131fa6260734e740d5068`  
		Last Modified: Wed, 24 Jun 2026 02:47:23 GMT  
		Size: 394.5 KB (394518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abdcf0dde2ac53ff144117390f118341c362a4a599d223d8f3f361d7bf6e4969`  
		Last Modified: Wed, 24 Jun 2026 02:47:24 GMT  
		Size: 99.7 KB (99687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98f10795ec0711c6fb1c1c2d9aaf02a8135b77ce56fb1448fda05b4d13a7717`  
		Last Modified: Wed, 24 Jun 2026 02:47:24 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aaabca7f1103b56ac333a0be1240140af54cd0ed33fc57c0ad749c6b3adc633`  
		Last Modified: Wed, 24 Jun 2026 02:47:25 GMT  
		Size: 42.2 MB (42162856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b27e6fcecf7b713c53863d2b5bd48f86d03d5b195fa8e6051741d0bce49c3d2`  
		Last Modified: Wed, 24 Jun 2026 02:47:25 GMT  
		Size: 415.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:6ff4682ef484e2f8e1ebb2ce54f44b3cebd2895336a188c5b714fc0d61c440cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de6284d11fb18093a35538214885a90f057e29e3ca45e48caca07259686fb31`

```dockerfile
```

-	Layers:
	-	`sha256:be79239d219b209b9d2f18f33d324866a220b298b9ccbea8d10047d5f8923441`  
		Last Modified: Wed, 24 Jun 2026 02:47:23 GMT  
		Size: 3.6 MB (3649204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d63773d4b69bde66025c54ba37e5906bed3b59835ac891ec8f2c451730179eb`  
		Last Modified: Wed, 24 Jun 2026 02:47:23 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5`

```console
$ docker pull couchdb@sha256:7219f4799fec01f35adcc445b9333cfd890bf9d2957e0ae32a345017dd0563a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.5` - linux; amd64

```console
$ docker pull couchdb@sha256:cc3732411c64ced82a0b60aa8aa3de3d506085745bc70a74ecb3b3be6116502d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148844108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d44232e2936d17afb2b1798bf2c507aec7faf0cafbd28fe901513e041cdbd91b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:41:45 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 01:41:45 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 24 Jun 2026 01:41:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:41:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 01:41:56 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 01:42:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:02 GMT
ENV COUCHDB_VERSION=3.5.2.1
# Wed, 24 Jun 2026 01:42:02 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y couchdb="$COUCHDB_VERSION"~trixie ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:42:14 GMT
VOLUME [/opt/couchdb/data]
# Wed, 24 Jun 2026 01:42:14 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 24 Jun 2026 01:42:14 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf4e623ec506cc4a3dac913d3b56b90e4fef2a77a9c36fdcf173f8d3b5278c5`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41389ef1d3c08b13549c1b4348192c604ad3a284329e5871b954354eea29701a`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 7.5 MB (7492182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacc441dd0740be802ff13f9f1b47daf5a3bc15af218d5781f017c26802a8a59`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 417.6 KB (417586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff6e59fcf95b99c098ff3c8880d2452b7aba9d13bf6c0f19ad0b5fe06b97e30`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 338.6 KB (338589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502ff7fc683f79f37d7c73b6e619ed701d657f0ceb516a15a687ca25a370a2d2`  
		Last Modified: Wed, 24 Jun 2026 01:42:29 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1729ef1d7ef490d9df9a9bef35e40236961c036f4e42e61b4bba68825d9f4200`  
		Last Modified: Wed, 24 Jun 2026 01:42:31 GMT  
		Size: 110.8 MB (110804902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fcad644c61c6a3b04844a48f337699db4d160e2c4236738941c1396e297ed7`  
		Last Modified: Wed, 24 Jun 2026 01:42:29 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30231fb7931d1261052bec6b2a3aea93155252de5867b2d3056530b0b784d3af`  
		Last Modified: Wed, 24 Jun 2026 01:42:29 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3153c610da961afa19f846e0e599bf564690dbfb87a41ac22e613f5ec4e042b7`  
		Last Modified: Wed, 24 Jun 2026 01:42:30 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe1d9b4ca3855ee21d8ca2d057b734e762a2749caf05b395eb4314e6d18e99c`  
		Last Modified: Wed, 24 Jun 2026 01:42:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:c0a6265cdedc5f932c8432b70206466e94fa714fbd92ba1a364ba1e2d977b915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb9afdcbd7a9e6a733e0fb6934737903fae00152b13a1d44bfe1701f63b0eaf`

```dockerfile
```

-	Layers:
	-	`sha256:a2a421c48dedd1c7d59b486174d617e7b94ad5a4ad3b1dbd53f3d3643e38722e`  
		Last Modified: Wed, 24 Jun 2026 01:42:28 GMT  
		Size: 4.2 MB (4180389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5350a5f3c13beedaf06d881b2ad3a3232267c800b3458b46c120994b684bd98a`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 31.7 KB (31675 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:3beeeddf8bd41e3d3175a81706041970931a6b9648ebe7cf0d83592dc9008cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148610960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2709151b5d31ef9083ce177249e3dc839908ce169530879c0dd33f6e6291a9e0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:45:14 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 01:45:14 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 24 Jun 2026 01:45:21 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 01:45:25 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 01:45:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:32 GMT
ENV COUCHDB_VERSION=3.5.2.1
# Wed, 24 Jun 2026 01:45:32 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 01:45:46 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y couchdb="$COUCHDB_VERSION"~trixie ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 24 Jun 2026 01:45:46 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 24 Jun 2026 01:45:46 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 24 Jun 2026 01:45:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 24 Jun 2026 01:45:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:45:46 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:45:46 GMT
VOLUME [/opt/couchdb/data]
# Wed, 24 Jun 2026 01:45:46 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 24 Jun 2026 01:45:46 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c34eafb21ffe87f9a1c7c17f11fcd3e474ff4be443d91b71069650935b45a49`  
		Last Modified: Wed, 24 Jun 2026 01:46:00 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c374173332b5fe10199e92b26dc196540789ebd47eac3a886163b9464183886`  
		Last Modified: Wed, 24 Jun 2026 01:46:00 GMT  
		Size: 7.3 MB (7261195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297cb5e063f5f7b21b877726abd1f8405924db8308e3dcacee0c9e445b5ca12b`  
		Last Modified: Wed, 24 Jun 2026 01:45:59 GMT  
		Size: 382.6 KB (382569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abf1699b7f712532e1c52400041c3cac70d15748da6008be064fd8079c6fd40`  
		Last Modified: Wed, 24 Jun 2026 01:46:00 GMT  
		Size: 338.8 KB (338754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f72ba21251a958d30a6b73bc738d047432036c794fc833b7b0f21bb77e23d5`  
		Last Modified: Wed, 24 Jun 2026 01:46:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee9883bcd6f5199cd1e4f0fb706d8bf2f12edf32903a1130ba9db387e5e7635`  
		Last Modified: Wed, 24 Jun 2026 01:46:04 GMT  
		Size: 110.5 MB (110474451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a15b9c4b1dd4da36e2a55a7d99596e53fb6b9e49556011dec18fa7279a5675d`  
		Last Modified: Wed, 24 Jun 2026 01:46:01 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0296e07dd1255baf3497c9bec73923346caa0078781774be87398df60c049d`  
		Last Modified: Wed, 24 Jun 2026 01:46:02 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbdfe6ea98ff36a0183910c32e21cc4c24ae6daec0a796c79764c7003ff21c0`  
		Last Modified: Wed, 24 Jun 2026 01:46:02 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87768653aa52520d0148009b743d1f4bb4208d3823d82c5c4729a8675d0bbb73`  
		Last Modified: Wed, 24 Jun 2026 01:46:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:2e3aea75ac902ad62649f52dad674240011a18bc5d8a35c6efaa8b78a22ef191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cff6de0fe65d5f070e7419be4529463bd15fd4ebe411a60aa94143041e2865a`

```dockerfile
```

-	Layers:
	-	`sha256:423f4c76bf94fe0a53f7180c4dccfcac2815cf31624db583c1b3f6aaab5f7f75`  
		Last Modified: Wed, 24 Jun 2026 01:46:00 GMT  
		Size: 4.2 MB (4180697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:391f250f12f470c2d1e19307a7d7020d0db34c3ca6e546585ce0b3d112b9762f`  
		Last Modified: Wed, 24 Jun 2026 01:46:00 GMT  
		Size: 31.9 KB (31882 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5-nouveau`

```console
$ docker pull couchdb@sha256:46e19736e1f738038af63b073bac826a1c1002b5b12013557800728a7448f283
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.5-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:a4f81ea823e89814fd49342b7afaa10ec5484a088bd7b04431364d3decdfec59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150900912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066f2bd675e9f8eefe75ed8101f03c04593468ae1ba9fd0dab60ee09a3f28a61`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:41:46 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 01:41:46 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 24 Jun 2026 01:41:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:41:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-21-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 01:42:01 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 01:42:06 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:06 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ trixie main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 01:42:11 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --no-install-recommends couchdb-nouveau=3.5.2.1~trixie;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 24 Jun 2026 01:42:11 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 24 Jun 2026 01:42:11 GMT
VOLUME [/opt/nouveau/data]
# Wed, 24 Jun 2026 01:42:11 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 24 Jun 2026 01:42:11 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b4f3a550bbab7a60d55fe4084cdfb1461ec280fc6ebb368c7f7ff552d75b4f`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501acc060a5c6b292aae2516f814a1327c0172c7248a72eaefa6c94ca45b3ea4`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 7.5 MB (7492088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38a0a807b1c3e2ef8ac7093fe8ba8fbde384bc101830ec3a5f7bc06a80812cb`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 70.0 MB (70032502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90fb09798c8df22a655cd0d6e428703b97158dadbb5522427bff65bfe767b6ae`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 426.0 KB (425954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef8732e1e77f7f125f10e74108815945d28d1ef4c0214620b3871fd3440be62`  
		Last Modified: Wed, 24 Jun 2026 01:42:26 GMT  
		Size: 347.4 KB (347406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115e152bad6a028a7a5ba2099e6e2a2bbaeb01176aa328e5ab39a72496ba6af8`  
		Last Modified: Wed, 24 Jun 2026 01:42:26 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc568814ebcaf941d047d29b0ce94404c65a9c12eeea4474390818a991a1f329`  
		Last Modified: Wed, 24 Jun 2026 01:42:28 GMT  
		Size: 42.8 MB (42815670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871728428bcca3734b8e1fe6b9df1e0be4cded4f20c40b5fb5f27216c0bf984d`  
		Last Modified: Wed, 24 Jun 2026 01:42:28 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:bc251961f9e3fac2cd1ac06330d76fc2fe8157f19ee13bb6da811597e27843d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3389170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e5d71ae57d78ac9697623eddbe290111da65587ddbc7671cb8db1dc17332e2a`

```dockerfile
```

-	Layers:
	-	`sha256:9d4ad28e48e6b7218fbcf6f5f24c87bea7f88a8f0615675a064a7fb5e1be71cf`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 3.4 MB (3364655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0d2bf3efdfcf1edb20b2925aa4fd8ec8bb10f6be633c4c1bd26e32329caf959`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 24.5 KB (24515 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:88f01a2895ccbc2ad4a4809d08a4ab34bada1cf459b90e408f677594febdc495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150060849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17fe359bdea2848ec50aa9ef2d607cc2581d2ad6ad03913fb00c0e3620979107`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:45:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 01:45:19 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 24 Jun 2026 01:45:27 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:33 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-21-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 01:45:37 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 01:45:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ trixie main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 01:45:49 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --no-install-recommends couchdb-nouveau=3.5.2.1~trixie;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 24 Jun 2026 01:45:49 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 24 Jun 2026 01:45:49 GMT
VOLUME [/opt/nouveau/data]
# Wed, 24 Jun 2026 01:45:49 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 24 Jun 2026 01:45:49 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afed3b15d19dc54098462361bd70be3167d1b4a2056095f6ea6b457239e0404e`  
		Last Modified: Wed, 24 Jun 2026 01:46:04 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2154a32b22e91cd532570515930309f7dc6ac5e11a359590effab20c7e5c83`  
		Last Modified: Wed, 24 Jun 2026 01:46:04 GMT  
		Size: 7.3 MB (7261182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77072d82cc95086e1b40e56a00e632fcd1a25c76b2fcf3054b4b65fde807b15d`  
		Last Modified: Wed, 24 Jun 2026 01:46:05 GMT  
		Size: 69.2 MB (69179776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4c068d6f2d2e441939047e06caf8a0e5fbd716b233ae63fc3790ba33a01ee6`  
		Last Modified: Wed, 24 Jun 2026 01:46:04 GMT  
		Size: 390.3 KB (390257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00028a2c864bb7e8a1ac6b0b2696419d4a70a5e52c8e5504d8a301637f3e486b`  
		Last Modified: Wed, 24 Jun 2026 01:46:05 GMT  
		Size: 347.4 KB (347413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3296c6540ed840d3914cb6e0e5a60c4b39e81c98d16e191429647085082c4888`  
		Last Modified: Wed, 24 Jun 2026 01:46:05 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adaa48dc2c10bbb2e9cab0e15f705a1b59f9b434758e23de5f25d1c9c0e2315a`  
		Last Modified: Wed, 24 Jun 2026 01:46:07 GMT  
		Size: 42.7 MB (42731788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dade987fdbe20973e04a762797ca68cc6ef72feef621a5ce4f9df4d2c7ca6768`  
		Last Modified: Wed, 24 Jun 2026 01:46:06 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:49d26e1d18ca48370c6d10add80d541441bec9cb9843f3ad085e6e726ceb0abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3388017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3ed08f5407b481c2ccde6de9e4913fcd1fcd1d33d15e859e376f49659e5b5a`

```dockerfile
```

-	Layers:
	-	`sha256:6e7e4636b53e3343add9560359cbf01f9b18700b04aa67e3431e1fa07bec70ce`  
		Last Modified: Wed, 24 Jun 2026 01:46:04 GMT  
		Size: 3.4 MB (3363308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d42543e31bac53348e2864f384be3c0cb44ee069ec0cf0e34cbf29f4de874f7`  
		Last Modified: Wed, 24 Jun 2026 01:46:04 GMT  
		Size: 24.7 KB (24709 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.2`

```console
$ docker pull couchdb@sha256:7219f4799fec01f35adcc445b9333cfd890bf9d2957e0ae32a345017dd0563a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.5.2` - linux; amd64

```console
$ docker pull couchdb@sha256:cc3732411c64ced82a0b60aa8aa3de3d506085745bc70a74ecb3b3be6116502d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148844108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d44232e2936d17afb2b1798bf2c507aec7faf0cafbd28fe901513e041cdbd91b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:41:45 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 01:41:45 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 24 Jun 2026 01:41:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:41:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 01:41:56 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 01:42:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:02 GMT
ENV COUCHDB_VERSION=3.5.2.1
# Wed, 24 Jun 2026 01:42:02 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y couchdb="$COUCHDB_VERSION"~trixie ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:42:14 GMT
VOLUME [/opt/couchdb/data]
# Wed, 24 Jun 2026 01:42:14 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 24 Jun 2026 01:42:14 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf4e623ec506cc4a3dac913d3b56b90e4fef2a77a9c36fdcf173f8d3b5278c5`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41389ef1d3c08b13549c1b4348192c604ad3a284329e5871b954354eea29701a`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 7.5 MB (7492182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacc441dd0740be802ff13f9f1b47daf5a3bc15af218d5781f017c26802a8a59`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 417.6 KB (417586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff6e59fcf95b99c098ff3c8880d2452b7aba9d13bf6c0f19ad0b5fe06b97e30`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 338.6 KB (338589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502ff7fc683f79f37d7c73b6e619ed701d657f0ceb516a15a687ca25a370a2d2`  
		Last Modified: Wed, 24 Jun 2026 01:42:29 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1729ef1d7ef490d9df9a9bef35e40236961c036f4e42e61b4bba68825d9f4200`  
		Last Modified: Wed, 24 Jun 2026 01:42:31 GMT  
		Size: 110.8 MB (110804902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fcad644c61c6a3b04844a48f337699db4d160e2c4236738941c1396e297ed7`  
		Last Modified: Wed, 24 Jun 2026 01:42:29 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30231fb7931d1261052bec6b2a3aea93155252de5867b2d3056530b0b784d3af`  
		Last Modified: Wed, 24 Jun 2026 01:42:29 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3153c610da961afa19f846e0e599bf564690dbfb87a41ac22e613f5ec4e042b7`  
		Last Modified: Wed, 24 Jun 2026 01:42:30 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe1d9b4ca3855ee21d8ca2d057b734e762a2749caf05b395eb4314e6d18e99c`  
		Last Modified: Wed, 24 Jun 2026 01:42:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:c0a6265cdedc5f932c8432b70206466e94fa714fbd92ba1a364ba1e2d977b915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb9afdcbd7a9e6a733e0fb6934737903fae00152b13a1d44bfe1701f63b0eaf`

```dockerfile
```

-	Layers:
	-	`sha256:a2a421c48dedd1c7d59b486174d617e7b94ad5a4ad3b1dbd53f3d3643e38722e`  
		Last Modified: Wed, 24 Jun 2026 01:42:28 GMT  
		Size: 4.2 MB (4180389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5350a5f3c13beedaf06d881b2ad3a3232267c800b3458b46c120994b684bd98a`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 31.7 KB (31675 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:3beeeddf8bd41e3d3175a81706041970931a6b9648ebe7cf0d83592dc9008cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148610960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2709151b5d31ef9083ce177249e3dc839908ce169530879c0dd33f6e6291a9e0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:45:14 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 01:45:14 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 24 Jun 2026 01:45:21 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 01:45:25 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 01:45:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:32 GMT
ENV COUCHDB_VERSION=3.5.2.1
# Wed, 24 Jun 2026 01:45:32 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 01:45:46 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y couchdb="$COUCHDB_VERSION"~trixie ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 24 Jun 2026 01:45:46 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 24 Jun 2026 01:45:46 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 24 Jun 2026 01:45:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 24 Jun 2026 01:45:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:45:46 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:45:46 GMT
VOLUME [/opt/couchdb/data]
# Wed, 24 Jun 2026 01:45:46 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 24 Jun 2026 01:45:46 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c34eafb21ffe87f9a1c7c17f11fcd3e474ff4be443d91b71069650935b45a49`  
		Last Modified: Wed, 24 Jun 2026 01:46:00 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c374173332b5fe10199e92b26dc196540789ebd47eac3a886163b9464183886`  
		Last Modified: Wed, 24 Jun 2026 01:46:00 GMT  
		Size: 7.3 MB (7261195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297cb5e063f5f7b21b877726abd1f8405924db8308e3dcacee0c9e445b5ca12b`  
		Last Modified: Wed, 24 Jun 2026 01:45:59 GMT  
		Size: 382.6 KB (382569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abf1699b7f712532e1c52400041c3cac70d15748da6008be064fd8079c6fd40`  
		Last Modified: Wed, 24 Jun 2026 01:46:00 GMT  
		Size: 338.8 KB (338754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f72ba21251a958d30a6b73bc738d047432036c794fc833b7b0f21bb77e23d5`  
		Last Modified: Wed, 24 Jun 2026 01:46:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee9883bcd6f5199cd1e4f0fb706d8bf2f12edf32903a1130ba9db387e5e7635`  
		Last Modified: Wed, 24 Jun 2026 01:46:04 GMT  
		Size: 110.5 MB (110474451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a15b9c4b1dd4da36e2a55a7d99596e53fb6b9e49556011dec18fa7279a5675d`  
		Last Modified: Wed, 24 Jun 2026 01:46:01 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0296e07dd1255baf3497c9bec73923346caa0078781774be87398df60c049d`  
		Last Modified: Wed, 24 Jun 2026 01:46:02 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbdfe6ea98ff36a0183910c32e21cc4c24ae6daec0a796c79764c7003ff21c0`  
		Last Modified: Wed, 24 Jun 2026 01:46:02 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87768653aa52520d0148009b743d1f4bb4208d3823d82c5c4729a8675d0bbb73`  
		Last Modified: Wed, 24 Jun 2026 01:46:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.2` - unknown; unknown

```console
$ docker pull couchdb@sha256:2e3aea75ac902ad62649f52dad674240011a18bc5d8a35c6efaa8b78a22ef191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cff6de0fe65d5f070e7419be4529463bd15fd4ebe411a60aa94143041e2865a`

```dockerfile
```

-	Layers:
	-	`sha256:423f4c76bf94fe0a53f7180c4dccfcac2815cf31624db583c1b3f6aaab5f7f75`  
		Last Modified: Wed, 24 Jun 2026 01:46:00 GMT  
		Size: 4.2 MB (4180697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:391f250f12f470c2d1e19307a7d7020d0db34c3ca6e546585ce0b3d112b9762f`  
		Last Modified: Wed, 24 Jun 2026 01:46:00 GMT  
		Size: 31.9 KB (31882 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.2-nouveau`

```console
$ docker pull couchdb@sha256:46e19736e1f738038af63b073bac826a1c1002b5b12013557800728a7448f283
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.5.2-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:a4f81ea823e89814fd49342b7afaa10ec5484a088bd7b04431364d3decdfec59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150900912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066f2bd675e9f8eefe75ed8101f03c04593468ae1ba9fd0dab60ee09a3f28a61`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:41:46 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 01:41:46 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 24 Jun 2026 01:41:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:41:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-21-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 01:42:01 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 01:42:06 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:06 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ trixie main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 01:42:11 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --no-install-recommends couchdb-nouveau=3.5.2.1~trixie;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 24 Jun 2026 01:42:11 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 24 Jun 2026 01:42:11 GMT
VOLUME [/opt/nouveau/data]
# Wed, 24 Jun 2026 01:42:11 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 24 Jun 2026 01:42:11 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b4f3a550bbab7a60d55fe4084cdfb1461ec280fc6ebb368c7f7ff552d75b4f`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501acc060a5c6b292aae2516f814a1327c0172c7248a72eaefa6c94ca45b3ea4`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 7.5 MB (7492088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38a0a807b1c3e2ef8ac7093fe8ba8fbde384bc101830ec3a5f7bc06a80812cb`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 70.0 MB (70032502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90fb09798c8df22a655cd0d6e428703b97158dadbb5522427bff65bfe767b6ae`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 426.0 KB (425954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef8732e1e77f7f125f10e74108815945d28d1ef4c0214620b3871fd3440be62`  
		Last Modified: Wed, 24 Jun 2026 01:42:26 GMT  
		Size: 347.4 KB (347406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115e152bad6a028a7a5ba2099e6e2a2bbaeb01176aa328e5ab39a72496ba6af8`  
		Last Modified: Wed, 24 Jun 2026 01:42:26 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc568814ebcaf941d047d29b0ce94404c65a9c12eeea4474390818a991a1f329`  
		Last Modified: Wed, 24 Jun 2026 01:42:28 GMT  
		Size: 42.8 MB (42815670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871728428bcca3734b8e1fe6b9df1e0be4cded4f20c40b5fb5f27216c0bf984d`  
		Last Modified: Wed, 24 Jun 2026 01:42:28 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.2-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:bc251961f9e3fac2cd1ac06330d76fc2fe8157f19ee13bb6da811597e27843d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3389170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e5d71ae57d78ac9697623eddbe290111da65587ddbc7671cb8db1dc17332e2a`

```dockerfile
```

-	Layers:
	-	`sha256:9d4ad28e48e6b7218fbcf6f5f24c87bea7f88a8f0615675a064a7fb5e1be71cf`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 3.4 MB (3364655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0d2bf3efdfcf1edb20b2925aa4fd8ec8bb10f6be633c4c1bd26e32329caf959`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 24.5 KB (24515 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.2-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:88f01a2895ccbc2ad4a4809d08a4ab34bada1cf459b90e408f677594febdc495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150060849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17fe359bdea2848ec50aa9ef2d607cc2581d2ad6ad03913fb00c0e3620979107`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:45:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 01:45:19 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 24 Jun 2026 01:45:27 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:33 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-21-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 01:45:37 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 01:45:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ trixie main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 01:45:49 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --no-install-recommends couchdb-nouveau=3.5.2.1~trixie;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 24 Jun 2026 01:45:49 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 24 Jun 2026 01:45:49 GMT
VOLUME [/opt/nouveau/data]
# Wed, 24 Jun 2026 01:45:49 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 24 Jun 2026 01:45:49 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afed3b15d19dc54098462361bd70be3167d1b4a2056095f6ea6b457239e0404e`  
		Last Modified: Wed, 24 Jun 2026 01:46:04 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2154a32b22e91cd532570515930309f7dc6ac5e11a359590effab20c7e5c83`  
		Last Modified: Wed, 24 Jun 2026 01:46:04 GMT  
		Size: 7.3 MB (7261182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77072d82cc95086e1b40e56a00e632fcd1a25c76b2fcf3054b4b65fde807b15d`  
		Last Modified: Wed, 24 Jun 2026 01:46:05 GMT  
		Size: 69.2 MB (69179776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4c068d6f2d2e441939047e06caf8a0e5fbd716b233ae63fc3790ba33a01ee6`  
		Last Modified: Wed, 24 Jun 2026 01:46:04 GMT  
		Size: 390.3 KB (390257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00028a2c864bb7e8a1ac6b0b2696419d4a70a5e52c8e5504d8a301637f3e486b`  
		Last Modified: Wed, 24 Jun 2026 01:46:05 GMT  
		Size: 347.4 KB (347413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3296c6540ed840d3914cb6e0e5a60c4b39e81c98d16e191429647085082c4888`  
		Last Modified: Wed, 24 Jun 2026 01:46:05 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adaa48dc2c10bbb2e9cab0e15f705a1b59f9b434758e23de5f25d1c9c0e2315a`  
		Last Modified: Wed, 24 Jun 2026 01:46:07 GMT  
		Size: 42.7 MB (42731788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dade987fdbe20973e04a762797ca68cc6ef72feef621a5ce4f9df4d2c7ca6768`  
		Last Modified: Wed, 24 Jun 2026 01:46:06 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.2-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:49d26e1d18ca48370c6d10add80d541441bec9cb9843f3ad085e6e726ceb0abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3388017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3ed08f5407b481c2ccde6de9e4913fcd1fcd1d33d15e859e376f49659e5b5a`

```dockerfile
```

-	Layers:
	-	`sha256:6e7e4636b53e3343add9560359cbf01f9b18700b04aa67e3431e1fa07bec70ce`  
		Last Modified: Wed, 24 Jun 2026 01:46:04 GMT  
		Size: 3.4 MB (3363308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d42543e31bac53348e2864f384be3c0cb44ee069ec0cf0e34cbf29f4de874f7`  
		Last Modified: Wed, 24 Jun 2026 01:46:04 GMT  
		Size: 24.7 KB (24709 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.2.1`

```console
$ docker pull couchdb@sha256:7219f4799fec01f35adcc445b9333cfd890bf9d2957e0ae32a345017dd0563a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.5.2.1` - linux; amd64

```console
$ docker pull couchdb@sha256:cc3732411c64ced82a0b60aa8aa3de3d506085745bc70a74ecb3b3be6116502d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148844108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d44232e2936d17afb2b1798bf2c507aec7faf0cafbd28fe901513e041cdbd91b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:41:45 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 01:41:45 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 24 Jun 2026 01:41:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:41:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 01:41:56 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 01:42:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:02 GMT
ENV COUCHDB_VERSION=3.5.2.1
# Wed, 24 Jun 2026 01:42:02 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y couchdb="$COUCHDB_VERSION"~trixie ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:42:14 GMT
VOLUME [/opt/couchdb/data]
# Wed, 24 Jun 2026 01:42:14 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 24 Jun 2026 01:42:14 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf4e623ec506cc4a3dac913d3b56b90e4fef2a77a9c36fdcf173f8d3b5278c5`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41389ef1d3c08b13549c1b4348192c604ad3a284329e5871b954354eea29701a`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 7.5 MB (7492182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacc441dd0740be802ff13f9f1b47daf5a3bc15af218d5781f017c26802a8a59`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 417.6 KB (417586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff6e59fcf95b99c098ff3c8880d2452b7aba9d13bf6c0f19ad0b5fe06b97e30`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 338.6 KB (338589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502ff7fc683f79f37d7c73b6e619ed701d657f0ceb516a15a687ca25a370a2d2`  
		Last Modified: Wed, 24 Jun 2026 01:42:29 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1729ef1d7ef490d9df9a9bef35e40236961c036f4e42e61b4bba68825d9f4200`  
		Last Modified: Wed, 24 Jun 2026 01:42:31 GMT  
		Size: 110.8 MB (110804902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fcad644c61c6a3b04844a48f337699db4d160e2c4236738941c1396e297ed7`  
		Last Modified: Wed, 24 Jun 2026 01:42:29 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30231fb7931d1261052bec6b2a3aea93155252de5867b2d3056530b0b784d3af`  
		Last Modified: Wed, 24 Jun 2026 01:42:29 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3153c610da961afa19f846e0e599bf564690dbfb87a41ac22e613f5ec4e042b7`  
		Last Modified: Wed, 24 Jun 2026 01:42:30 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe1d9b4ca3855ee21d8ca2d057b734e762a2749caf05b395eb4314e6d18e99c`  
		Last Modified: Wed, 24 Jun 2026 01:42:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.2.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:c0a6265cdedc5f932c8432b70206466e94fa714fbd92ba1a364ba1e2d977b915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb9afdcbd7a9e6a733e0fb6934737903fae00152b13a1d44bfe1701f63b0eaf`

```dockerfile
```

-	Layers:
	-	`sha256:a2a421c48dedd1c7d59b486174d617e7b94ad5a4ad3b1dbd53f3d3643e38722e`  
		Last Modified: Wed, 24 Jun 2026 01:42:28 GMT  
		Size: 4.2 MB (4180389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5350a5f3c13beedaf06d881b2ad3a3232267c800b3458b46c120994b684bd98a`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 31.7 KB (31675 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.2.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:3beeeddf8bd41e3d3175a81706041970931a6b9648ebe7cf0d83592dc9008cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148610960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2709151b5d31ef9083ce177249e3dc839908ce169530879c0dd33f6e6291a9e0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:45:14 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 01:45:14 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 24 Jun 2026 01:45:21 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 01:45:25 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 01:45:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:32 GMT
ENV COUCHDB_VERSION=3.5.2.1
# Wed, 24 Jun 2026 01:45:32 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 01:45:46 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y couchdb="$COUCHDB_VERSION"~trixie ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 24 Jun 2026 01:45:46 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 24 Jun 2026 01:45:46 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 24 Jun 2026 01:45:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 24 Jun 2026 01:45:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:45:46 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:45:46 GMT
VOLUME [/opt/couchdb/data]
# Wed, 24 Jun 2026 01:45:46 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 24 Jun 2026 01:45:46 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c34eafb21ffe87f9a1c7c17f11fcd3e474ff4be443d91b71069650935b45a49`  
		Last Modified: Wed, 24 Jun 2026 01:46:00 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c374173332b5fe10199e92b26dc196540789ebd47eac3a886163b9464183886`  
		Last Modified: Wed, 24 Jun 2026 01:46:00 GMT  
		Size: 7.3 MB (7261195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297cb5e063f5f7b21b877726abd1f8405924db8308e3dcacee0c9e445b5ca12b`  
		Last Modified: Wed, 24 Jun 2026 01:45:59 GMT  
		Size: 382.6 KB (382569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abf1699b7f712532e1c52400041c3cac70d15748da6008be064fd8079c6fd40`  
		Last Modified: Wed, 24 Jun 2026 01:46:00 GMT  
		Size: 338.8 KB (338754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f72ba21251a958d30a6b73bc738d047432036c794fc833b7b0f21bb77e23d5`  
		Last Modified: Wed, 24 Jun 2026 01:46:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee9883bcd6f5199cd1e4f0fb706d8bf2f12edf32903a1130ba9db387e5e7635`  
		Last Modified: Wed, 24 Jun 2026 01:46:04 GMT  
		Size: 110.5 MB (110474451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a15b9c4b1dd4da36e2a55a7d99596e53fb6b9e49556011dec18fa7279a5675d`  
		Last Modified: Wed, 24 Jun 2026 01:46:01 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0296e07dd1255baf3497c9bec73923346caa0078781774be87398df60c049d`  
		Last Modified: Wed, 24 Jun 2026 01:46:02 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbdfe6ea98ff36a0183910c32e21cc4c24ae6daec0a796c79764c7003ff21c0`  
		Last Modified: Wed, 24 Jun 2026 01:46:02 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87768653aa52520d0148009b743d1f4bb4208d3823d82c5c4729a8675d0bbb73`  
		Last Modified: Wed, 24 Jun 2026 01:46:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.2.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:2e3aea75ac902ad62649f52dad674240011a18bc5d8a35c6efaa8b78a22ef191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cff6de0fe65d5f070e7419be4529463bd15fd4ebe411a60aa94143041e2865a`

```dockerfile
```

-	Layers:
	-	`sha256:423f4c76bf94fe0a53f7180c4dccfcac2815cf31624db583c1b3f6aaab5f7f75`  
		Last Modified: Wed, 24 Jun 2026 01:46:00 GMT  
		Size: 4.2 MB (4180697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:391f250f12f470c2d1e19307a7d7020d0db34c3ca6e546585ce0b3d112b9762f`  
		Last Modified: Wed, 24 Jun 2026 01:46:00 GMT  
		Size: 31.9 KB (31882 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.2.1-nouveau`

```console
$ docker pull couchdb@sha256:46e19736e1f738038af63b073bac826a1c1002b5b12013557800728a7448f283
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:3.5.2.1-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:a4f81ea823e89814fd49342b7afaa10ec5484a088bd7b04431364d3decdfec59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150900912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:066f2bd675e9f8eefe75ed8101f03c04593468ae1ba9fd0dab60ee09a3f28a61`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:41:46 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 01:41:46 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 24 Jun 2026 01:41:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:41:59 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-21-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 01:42:01 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 01:42:06 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:06 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ trixie main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 01:42:11 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --no-install-recommends couchdb-nouveau=3.5.2.1~trixie;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 24 Jun 2026 01:42:11 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 24 Jun 2026 01:42:11 GMT
VOLUME [/opt/nouveau/data]
# Wed, 24 Jun 2026 01:42:11 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 24 Jun 2026 01:42:11 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b4f3a550bbab7a60d55fe4084cdfb1461ec280fc6ebb368c7f7ff552d75b4f`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501acc060a5c6b292aae2516f814a1327c0172c7248a72eaefa6c94ca45b3ea4`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 7.5 MB (7492088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38a0a807b1c3e2ef8ac7093fe8ba8fbde384bc101830ec3a5f7bc06a80812cb`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 70.0 MB (70032502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90fb09798c8df22a655cd0d6e428703b97158dadbb5522427bff65bfe767b6ae`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 426.0 KB (425954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef8732e1e77f7f125f10e74108815945d28d1ef4c0214620b3871fd3440be62`  
		Last Modified: Wed, 24 Jun 2026 01:42:26 GMT  
		Size: 347.4 KB (347406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115e152bad6a028a7a5ba2099e6e2a2bbaeb01176aa328e5ab39a72496ba6af8`  
		Last Modified: Wed, 24 Jun 2026 01:42:26 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc568814ebcaf941d047d29b0ce94404c65a9c12eeea4474390818a991a1f329`  
		Last Modified: Wed, 24 Jun 2026 01:42:28 GMT  
		Size: 42.8 MB (42815670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871728428bcca3734b8e1fe6b9df1e0be4cded4f20c40b5fb5f27216c0bf984d`  
		Last Modified: Wed, 24 Jun 2026 01:42:28 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.2.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:bc251961f9e3fac2cd1ac06330d76fc2fe8157f19ee13bb6da811597e27843d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3389170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e5d71ae57d78ac9697623eddbe290111da65587ddbc7671cb8db1dc17332e2a`

```dockerfile
```

-	Layers:
	-	`sha256:9d4ad28e48e6b7218fbcf6f5f24c87bea7f88a8f0615675a064a7fb5e1be71cf`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 3.4 MB (3364655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0d2bf3efdfcf1edb20b2925aa4fd8ec8bb10f6be633c4c1bd26e32329caf959`  
		Last Modified: Wed, 24 Jun 2026 01:42:25 GMT  
		Size: 24.5 KB (24515 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.2.1-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:88f01a2895ccbc2ad4a4809d08a4ab34bada1cf459b90e408f677594febdc495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150060849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17fe359bdea2848ec50aa9ef2d607cc2581d2ad6ad03913fb00c0e3620979107`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:45:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 01:45:19 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Wed, 24 Jun 2026 01:45:27 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:33 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-21-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 01:45:37 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 01:45:43 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:43 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ trixie main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 01:45:49 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --no-install-recommends couchdb-nouveau=3.5.2.1~trixie;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Wed, 24 Jun 2026 01:45:49 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Wed, 24 Jun 2026 01:45:49 GMT
VOLUME [/opt/nouveau/data]
# Wed, 24 Jun 2026 01:45:49 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Wed, 24 Jun 2026 01:45:49 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afed3b15d19dc54098462361bd70be3167d1b4a2056095f6ea6b457239e0404e`  
		Last Modified: Wed, 24 Jun 2026 01:46:04 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2154a32b22e91cd532570515930309f7dc6ac5e11a359590effab20c7e5c83`  
		Last Modified: Wed, 24 Jun 2026 01:46:04 GMT  
		Size: 7.3 MB (7261182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77072d82cc95086e1b40e56a00e632fcd1a25c76b2fcf3054b4b65fde807b15d`  
		Last Modified: Wed, 24 Jun 2026 01:46:05 GMT  
		Size: 69.2 MB (69179776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4c068d6f2d2e441939047e06caf8a0e5fbd716b233ae63fc3790ba33a01ee6`  
		Last Modified: Wed, 24 Jun 2026 01:46:04 GMT  
		Size: 390.3 KB (390257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00028a2c864bb7e8a1ac6b0b2696419d4a70a5e52c8e5504d8a301637f3e486b`  
		Last Modified: Wed, 24 Jun 2026 01:46:05 GMT  
		Size: 347.4 KB (347413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3296c6540ed840d3914cb6e0e5a60c4b39e81c98d16e191429647085082c4888`  
		Last Modified: Wed, 24 Jun 2026 01:46:05 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adaa48dc2c10bbb2e9cab0e15f705a1b59f9b434758e23de5f25d1c9c0e2315a`  
		Last Modified: Wed, 24 Jun 2026 01:46:07 GMT  
		Size: 42.7 MB (42731788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dade987fdbe20973e04a762797ca68cc6ef72feef621a5ce4f9df4d2c7ca6768`  
		Last Modified: Wed, 24 Jun 2026 01:46:06 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.2.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:49d26e1d18ca48370c6d10add80d541441bec9cb9843f3ad085e6e726ceb0abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3388017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3ed08f5407b481c2ccde6de9e4913fcd1fcd1d33d15e859e376f49659e5b5a`

```dockerfile
```

-	Layers:
	-	`sha256:6e7e4636b53e3343add9560359cbf01f9b18700b04aa67e3431e1fa07bec70ce`  
		Last Modified: Wed, 24 Jun 2026 01:46:04 GMT  
		Size: 3.4 MB (3363308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d42543e31bac53348e2864f384be3c0cb44ee069ec0cf0e34cbf29f4de874f7`  
		Last Modified: Wed, 24 Jun 2026 01:46:04 GMT  
		Size: 24.7 KB (24709 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:7219f4799fec01f35adcc445b9333cfd890bf9d2957e0ae32a345017dd0563a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:cc3732411c64ced82a0b60aa8aa3de3d506085745bc70a74ecb3b3be6116502d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148844108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d44232e2936d17afb2b1798bf2c507aec7faf0cafbd28fe901513e041cdbd91b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:41:45 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 01:41:45 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 24 Jun 2026 01:41:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:41:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 01:41:56 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 01:42:02 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:42:02 GMT
ENV COUCHDB_VERSION=3.5.2.1
# Wed, 24 Jun 2026 01:42:02 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y couchdb="$COUCHDB_VERSION"~trixie ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:42:14 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:42:14 GMT
VOLUME [/opt/couchdb/data]
# Wed, 24 Jun 2026 01:42:14 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 24 Jun 2026 01:42:14 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf4e623ec506cc4a3dac913d3b56b90e4fef2a77a9c36fdcf173f8d3b5278c5`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41389ef1d3c08b13549c1b4348192c604ad3a284329e5871b954354eea29701a`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 7.5 MB (7492182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacc441dd0740be802ff13f9f1b47daf5a3bc15af218d5781f017c26802a8a59`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 417.6 KB (417586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff6e59fcf95b99c098ff3c8880d2452b7aba9d13bf6c0f19ad0b5fe06b97e30`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 338.6 KB (338589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502ff7fc683f79f37d7c73b6e619ed701d657f0ceb516a15a687ca25a370a2d2`  
		Last Modified: Wed, 24 Jun 2026 01:42:29 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1729ef1d7ef490d9df9a9bef35e40236961c036f4e42e61b4bba68825d9f4200`  
		Last Modified: Wed, 24 Jun 2026 01:42:31 GMT  
		Size: 110.8 MB (110804902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fcad644c61c6a3b04844a48f337699db4d160e2c4236738941c1396e297ed7`  
		Last Modified: Wed, 24 Jun 2026 01:42:29 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30231fb7931d1261052bec6b2a3aea93155252de5867b2d3056530b0b784d3af`  
		Last Modified: Wed, 24 Jun 2026 01:42:29 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3153c610da961afa19f846e0e599bf564690dbfb87a41ac22e613f5ec4e042b7`  
		Last Modified: Wed, 24 Jun 2026 01:42:30 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe1d9b4ca3855ee21d8ca2d057b734e762a2749caf05b395eb4314e6d18e99c`  
		Last Modified: Wed, 24 Jun 2026 01:42:31 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:c0a6265cdedc5f932c8432b70206466e94fa714fbd92ba1a364ba1e2d977b915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb9afdcbd7a9e6a733e0fb6934737903fae00152b13a1d44bfe1701f63b0eaf`

```dockerfile
```

-	Layers:
	-	`sha256:a2a421c48dedd1c7d59b486174d617e7b94ad5a4ad3b1dbd53f3d3643e38722e`  
		Last Modified: Wed, 24 Jun 2026 01:42:28 GMT  
		Size: 4.2 MB (4180389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5350a5f3c13beedaf06d881b2ad3a3232267c800b3458b46c120994b684bd98a`  
		Last Modified: Wed, 24 Jun 2026 01:42:27 GMT  
		Size: 31.7 KB (31675 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:3beeeddf8bd41e3d3175a81706041970931a6b9648ebe7cf0d83592dc9008cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148610960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2709151b5d31ef9083ce177249e3dc839908ce169530879c0dd33f6e6291a9e0`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:45:14 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 24 Jun 2026 01:45:14 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Wed, 24 Jun 2026 01:45:21 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:25 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Wed, 24 Jun 2026 01:45:25 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 24 Jun 2026 01:45:32 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:32 GMT
ENV COUCHDB_VERSION=3.5.2.1
# Wed, 24 Jun 2026 01:45:32 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Wed, 24 Jun 2026 01:45:46 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y couchdb="$COUCHDB_VERSION"~trixie ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Wed, 24 Jun 2026 01:45:46 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Wed, 24 Jun 2026 01:45:46 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Wed, 24 Jun 2026 01:45:46 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Wed, 24 Jun 2026 01:45:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Wed, 24 Jun 2026 01:45:46 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:45:46 GMT
VOLUME [/opt/couchdb/data]
# Wed, 24 Jun 2026 01:45:46 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Wed, 24 Jun 2026 01:45:46 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c34eafb21ffe87f9a1c7c17f11fcd3e474ff4be443d91b71069650935b45a49`  
		Last Modified: Wed, 24 Jun 2026 01:46:00 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c374173332b5fe10199e92b26dc196540789ebd47eac3a886163b9464183886`  
		Last Modified: Wed, 24 Jun 2026 01:46:00 GMT  
		Size: 7.3 MB (7261195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297cb5e063f5f7b21b877726abd1f8405924db8308e3dcacee0c9e445b5ca12b`  
		Last Modified: Wed, 24 Jun 2026 01:45:59 GMT  
		Size: 382.6 KB (382569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abf1699b7f712532e1c52400041c3cac70d15748da6008be064fd8079c6fd40`  
		Last Modified: Wed, 24 Jun 2026 01:46:00 GMT  
		Size: 338.8 KB (338754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f72ba21251a958d30a6b73bc738d047432036c794fc833b7b0f21bb77e23d5`  
		Last Modified: Wed, 24 Jun 2026 01:46:01 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee9883bcd6f5199cd1e4f0fb706d8bf2f12edf32903a1130ba9db387e5e7635`  
		Last Modified: Wed, 24 Jun 2026 01:46:04 GMT  
		Size: 110.5 MB (110474451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a15b9c4b1dd4da36e2a55a7d99596e53fb6b9e49556011dec18fa7279a5675d`  
		Last Modified: Wed, 24 Jun 2026 01:46:01 GMT  
		Size: 381.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0296e07dd1255baf3497c9bec73923346caa0078781774be87398df60c049d`  
		Last Modified: Wed, 24 Jun 2026 01:46:02 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbdfe6ea98ff36a0183910c32e21cc4c24ae6daec0a796c79764c7003ff21c0`  
		Last Modified: Wed, 24 Jun 2026 01:46:02 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87768653aa52520d0148009b743d1f4bb4208d3823d82c5c4729a8675d0bbb73`  
		Last Modified: Wed, 24 Jun 2026 01:46:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:2e3aea75ac902ad62649f52dad674240011a18bc5d8a35c6efaa8b78a22ef191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cff6de0fe65d5f070e7419be4529463bd15fd4ebe411a60aa94143041e2865a`

```dockerfile
```

-	Layers:
	-	`sha256:423f4c76bf94fe0a53f7180c4dccfcac2815cf31624db583c1b3f6aaab5f7f75`  
		Last Modified: Wed, 24 Jun 2026 01:46:00 GMT  
		Size: 4.2 MB (4180697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:391f250f12f470c2d1e19307a7d7020d0db34c3ca6e546585ce0b3d112b9762f`  
		Last Modified: Wed, 24 Jun 2026 01:46:00 GMT  
		Size: 31.9 KB (31882 bytes)  
		MIME: application/vnd.in-toto+json
