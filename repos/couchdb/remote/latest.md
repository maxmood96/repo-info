## `couchdb:latest`

```console
$ docker pull couchdb@sha256:1c9b191b061a3b8f678b6084c2af0fa478ef1506fe910edcc5c2c9f1f8f35a73
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

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:4331421a2e5dff323618e823c60efcc1ae8eacbe318319945e4855800d80fd2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89655707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e531576bbaefd82bf65c1645920e94469b7e49ec5c3ad840d545fb9eeab148c9`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d906fcb7e77b51c81aba3df31e682564bfc67c9ee478357ba93ccd921360a295`  
		Last Modified: Tue, 14 May 2024 02:56:12 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99bdf844da7575b7a40112dfc38f45b64fc0309377eb7cdb323e8094bf1330d6`  
		Last Modified: Tue, 14 May 2024 02:56:12 GMT  
		Size: 5.0 MB (5019697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c432908a4bea2a28515a63bdf25cec4cd7d30946cc8345733a17f742b92f8a2`  
		Last Modified: Tue, 14 May 2024 02:56:12 GMT  
		Size: 394.3 KB (394318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0901a2ab1c8cf3bcfdf8539468bd3aabf9d367f2b3db9f1a1dc4e05849b51bcd`  
		Last Modified: Tue, 14 May 2024 02:56:12 GMT  
		Size: 77.9 KB (77891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49ef1bac64f318092a920be080d071cae96b005a5bda54778e86df20c1e38aa`  
		Last Modified: Tue, 14 May 2024 02:56:13 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144b0b16749fe2b786daa57858eb3f1d70da0fb15365e5ad92122b065ce51e52`  
		Last Modified: Tue, 14 May 2024 02:56:15 GMT  
		Size: 52.7 MB (52722303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832249bf8a9bb00720985cfed188497d1de365c9aaf52ea3b61ee1d59bdec669`  
		Last Modified: Tue, 14 May 2024 02:56:13 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca46de6fcc9c3d401ed229e4613ebc74de01b085c9f11a6b0d370f85e0f8067`  
		Last Modified: Tue, 14 May 2024 02:56:13 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc2999f6ec16d99fc4ead75fe603e73db9a37f9dca77aa0e40e9566e0407305`  
		Last Modified: Tue, 14 May 2024 02:56:14 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6536369e9e5921aef5e7173fc3372a996702c23bb6b850a0799ae5c762baefc9`  
		Last Modified: Tue, 14 May 2024 02:56:14 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:773db3b1f338a1cb34126e05583d59e8defefca80d4bb7a031887434aa5c117c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522035137d5c1936095a79d50124269c66969a0853f2551641cfbfa24f250cdd`

```dockerfile
```

-	Layers:
	-	`sha256:dc6b608370ebad9c972b3749519a5bfb9a6209849f052b64d9c2dfc18efc27c3`  
		Last Modified: Tue, 14 May 2024 02:56:12 GMT  
		Size: 4.0 MB (3965078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79751d31bbe331aca7734b8c91c8d80b89d7369796647f7044b3073049aac7c1`  
		Last Modified: Tue, 14 May 2024 02:56:12 GMT  
		Size: 31.7 KB (31730 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:f0e9b2c649a6724a24d2fad16ef90e14854d2a30be1eac01136b37ef8ca75fe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88100685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4158510fdd76185be535e81514159eeeb23941484eb43479a99b9bebde744489`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
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
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a159f04f5ba449e2ac588d65dac07b043f3869765baaa698f95493ff0b771f36`  
		Last Modified: Wed, 24 Apr 2024 16:33:38 GMT  
		Size: 3.3 KB (3349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3d37b9bbcc43de1f8fe8118c41081cdcfd966be8958b1580a55f5bf7c28f2d`  
		Last Modified: Wed, 24 Apr 2024 16:33:38 GMT  
		Size: 5.0 MB (5004097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286cf5fbaea9e4f37a8f90443318d2871d9713908a665e662dc92d60d3834920`  
		Last Modified: Wed, 24 Apr 2024 16:33:38 GMT  
		Size: 350.5 KB (350540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e46401911bbcb91945b101aa870c0e07bb1375043745db2dbb7e7f5bb9606f`  
		Last Modified: Wed, 24 Apr 2024 16:33:39 GMT  
		Size: 77.8 KB (77805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccef9aef5aa61d73182fb3588b6057882ab40b9df4a38eaaa6b0b1e4bde19e6`  
		Last Modified: Wed, 24 Apr 2024 16:33:39 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1d39ab8449fcc390c58a6154c0ce1b84e3744cf58b9328561d547ec9f4f9cd`  
		Last Modified: Wed, 24 Apr 2024 16:33:41 GMT  
		Size: 52.6 MB (52573310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e70f98e6ef6a3d89751ebb0a1ca161863df9ce35bbf9e3e5f67d0c008a2aa1`  
		Last Modified: Wed, 24 Apr 2024 16:33:40 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42909ec628ccda6f4c354819ff59a4e6694dea073705aba035e4881e2c98b7f`  
		Last Modified: Wed, 24 Apr 2024 16:33:40 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02019e9d3e69204668325fa500054957eaeff2ea662474a7fba7d35e2ec2d52d`  
		Last Modified: Wed, 24 Apr 2024 16:33:41 GMT  
		Size: 2.2 KB (2231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1852a167c7c17f616cfb8af6e64f66ce24e126c77bff92ddc5c24cb07f6db796`  
		Last Modified: Wed, 24 Apr 2024 16:33:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:ec658f3a337854cc192e391a55c35fa0845050edd7a7bc291b54046200bee5c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3997052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed006c670980e9d3a71a17ba24813c4d71ba9e7c0529d8c9177e9f3fb9fef89e`

```dockerfile
```

-	Layers:
	-	`sha256:4ba15cba561d024911c651ed74ab31b845e759ecbc1ed4a3465f1c23ff71485f`  
		Last Modified: Wed, 24 Apr 2024 16:33:38 GMT  
		Size: 4.0 MB (3965312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8d0f5469c522b5bd39214ac5a04134c1472292202b433de6ad699d17ed2a545`  
		Last Modified: Wed, 24 Apr 2024 16:33:38 GMT  
		Size: 31.7 KB (31740 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:58156bd24dfd7de4227f32f2dbde19f9acab236ab7d52ed51b15811b19f29814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95382853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107df9c0c0bbf7bc6c9bc7639943efd8d44aff0852963b413ef3559e84d1619a`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:7c74907a13931bf5f38ce8642536ee05738ba9d233424998c52fc548130034b5 in / 
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
	-	`sha256:8fd45f8fa7e828bdb5dd8878febd6f367c5092a047db5f6ca094056a1b0c627c`  
		Last Modified: Tue, 14 May 2024 01:24:52 GMT  
		Size: 35.3 MB (35311159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cf93d48de5264d046dc227a4328348a5ea98f8e5e17f3e44d45ea98e9c0e37`  
		Last Modified: Tue, 14 May 2024 07:25:07 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029e3d567de2a5542d5bfe4bd503ee45d6d696e74c26694e1c7bd08cb3cbbb2b`  
		Last Modified: Tue, 14 May 2024 07:25:08 GMT  
		Size: 5.8 MB (5839119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89646478ea3afd92bdc34e494f0065b7e16ba2d0dcbc68e3873a4cd85ac0f6f6`  
		Last Modified: Tue, 14 May 2024 07:25:08 GMT  
		Size: 446.6 KB (446638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5849ebb34c9f0408a08f2b9f9db21571eb050743cce644f69c7061041d499412`  
		Last Modified: Tue, 14 May 2024 07:25:09 GMT  
		Size: 77.8 KB (77836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1fd03b0ed7fa194ee23ef921f686c04a7faeb6f9ade2bd8ced8298341d56e7`  
		Last Modified: Tue, 14 May 2024 07:25:09 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa1e4d4072a4816c3de34f524ab4b2844328c1a6241e54fa07920f6aa2f1632`  
		Last Modified: Tue, 14 May 2024 07:25:11 GMT  
		Size: 53.7 MB (53700522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe786dabcaebd644d5eeb21594657da050a313f9292b3c065bcec9b2062af839`  
		Last Modified: Tue, 14 May 2024 07:25:10 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b35f04877d50ddb49947e9ec9fd1cd70955e2648c10ab1ee6a548efaa1ea865`  
		Last Modified: Tue, 14 May 2024 07:25:10 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74919c23b96621fbba9071ef08f76ad12eff2d4a424b8b464fe71f3da76e544`  
		Last Modified: Tue, 14 May 2024 07:25:10 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5094108149380d384cfc1787f1111c32697f41ac74ffc663eb77e88ecbcacc1d`  
		Last Modified: Tue, 14 May 2024 07:25:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:b4240c74cc620cb13c95219d0cd4ebddb3c152a9cc6c6f9c768b1d41ccb7e2d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4001390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:903c624fd72120f948fe122cc9954fe45c482b1e74e26b0eda2a40313d739dc9`

```dockerfile
```

-	Layers:
	-	`sha256:c997d4f66204e210e94dca5c7dd72af9d9c30c50fa2c23150c1f3f55abea3fe5`  
		Last Modified: Tue, 14 May 2024 07:25:08 GMT  
		Size: 4.0 MB (3969610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:779824a851a2435907e1243f288941db96a8065847d330c4df65929055494b46`  
		Last Modified: Tue, 14 May 2024 07:25:07 GMT  
		Size: 31.8 KB (31780 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:8468aca9a5cbbaa6100efa87302661ce255feb45b6e50986a0d565e85345dfea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86397842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74463f0ad8a9e79556f2d92b80851de5a94d5547dda4183e65bff33d8f06dfec`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Tue, 05 Dec 2023 19:33:12 GMT
ADD file:bac230200161ff0b0332af3dc90dc1aba6bdeb875d95659699251b2af4eec8dc in / 
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
	-	`sha256:14d39445de105c0a8fe00b3899e9fdab7cdfbb3ff27c8b39dd9059f3264a4841`  
		Last Modified: Tue, 14 May 2024 00:48:06 GMT  
		Size: 29.7 MB (29673656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17949f5b9178ff1f3dce8917d65f6abb49fa54851e8a88b3e0aecc1743f9b47`  
		Last Modified: Tue, 14 May 2024 07:12:14 GMT  
		Size: 3.3 KB (3349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec78ff4e8cf95d46165b4d84b185bed3ac8ea331c246d1915ca1c70a76c2b6c`  
		Last Modified: Tue, 14 May 2024 07:12:15 GMT  
		Size: 4.9 MB (4905536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b810001bf2a7e98cb5e0ba1e9b1997a57d1d5d4ff86cced5a78c4febb4f7eb01`  
		Last Modified: Tue, 14 May 2024 07:12:15 GMT  
		Size: 357.4 KB (357436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b269993425a3098b5e0b499fe3db204c94a8be0ae19360b3da54256fa2003f`  
		Last Modified: Tue, 14 May 2024 07:12:15 GMT  
		Size: 77.8 KB (77836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281891daf068f5795ee2a24ba747a80ec915f8229c131a925a2c5a29be72437d`  
		Last Modified: Tue, 14 May 2024 07:12:16 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7989fc17c203a837193f1aa6faab79d4a0219c82ac4fec1ce3e099f1d8666b0f`  
		Last Modified: Tue, 14 May 2024 07:12:17 GMT  
		Size: 51.4 MB (51375789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e8d59c4b116719043dacc2dcdc2a0d667eb73da2c3f03bf6a946bae551ca17`  
		Last Modified: Tue, 14 May 2024 07:12:16 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b024bfc2555c5ff15c877ffa24d5893096351c23d861094be82172b21244505`  
		Last Modified: Tue, 14 May 2024 07:12:16 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b058b59294f503329c5691063af2d32c36da46e2d0bf4af1c55275d7d42d6e0b`  
		Last Modified: Tue, 14 May 2024 07:12:17 GMT  
		Size: 2.2 KB (2225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48caa89c0ae55f706e44f768b7a231e55670970dbec0bb4b05c3404a6cfbfbe`  
		Last Modified: Tue, 14 May 2024 07:12:17 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:f111937931c3b100dfca90df9bea0d3df521194f4009489616638f863975e372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3996378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:725927a02b9b4713f3245424fdd91c84333cb7aad4a15b0dea68b51261edc36a`

```dockerfile
```

-	Layers:
	-	`sha256:ede20e200e411cf8dda2d4a31cc6c72fbeb9accbe9310106eeeaf75f60ce103f`  
		Last Modified: Tue, 14 May 2024 07:12:15 GMT  
		Size: 4.0 MB (3964648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16afbe0c3eff6c45da1676533800c7b55a674f0375bafe76ee8cb7f50124174b`  
		Last Modified: Tue, 14 May 2024 07:12:14 GMT  
		Size: 31.7 KB (31730 bytes)  
		MIME: application/vnd.in-toto+json
