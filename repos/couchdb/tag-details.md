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
-	[`couchdb:3.5.1`](#couchdb351)
-	[`couchdb:3.5.1-nouveau`](#couchdb351-nouveau)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:3`

```console
$ docker pull couchdb@sha256:24c854639f2f14f346caa10c80f9f246c656b869020bb171b3afd375c02098f0
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
$ docker pull couchdb@sha256:414799d7a687c714246d1d6c8033b00e34fff4060a7b9ff92cdb82669d532a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142059762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:595b13672075944f8455e1500533e469a7208c52d8b432abeb86afd1afabffaa`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:38:58 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 16 Mar 2026 22:38:58 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Mon, 16 Mar 2026 22:39:04 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:39:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 16 Mar 2026 22:39:06 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 16 Mar 2026 22:39:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:39:11 GMT
ENV COUCHDB_VERSION=3.5.1
# Mon, 16 Mar 2026 22:39:11 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 16 Mar 2026 22:39:25 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 16 Mar 2026 22:39:26 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Mon, 16 Mar 2026 22:39:26 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Mon, 16 Mar 2026 22:39:26 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 16 Mar 2026 22:39:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 16 Mar 2026 22:39:26 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:39:26 GMT
VOLUME [/opt/couchdb/data]
# Mon, 16 Mar 2026 22:39:26 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Mon, 16 Mar 2026 22:39:26 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef9f6538a75b47d65696d8725a4856d08435f55fb49544f7d5765fdd2fe9f21`  
		Last Modified: Mon, 16 Mar 2026 22:39:39 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1d4c09467ad6a157a8fc64695003e96208a72cbb3f879feb6f75389e9c79d0`  
		Last Modified: Mon, 16 Mar 2026 22:39:39 GMT  
		Size: 7.9 MB (7883135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1923c6e324517621c74d21a82203c23bfcf8688ad7244d63fa1f1230c21971`  
		Last Modified: Mon, 16 Mar 2026 22:39:39 GMT  
		Size: 401.8 KB (401785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2ab6b8f282ff901e21be15bceb055824bb30a8bbc59ce8186e78c6ef512d64`  
		Last Modified: Mon, 16 Mar 2026 22:39:39 GMT  
		Size: 76.5 KB (76540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c837407581c764041f008e2ec54e18db3174a03e2c8949d8c09c8ce91c64cb`  
		Last Modified: Mon, 16 Mar 2026 22:39:40 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bf3899d4ad55fa4b2b0974dc50d0df3ac2f650ead5ee7a8a67d5a6ac360b5f`  
		Last Modified: Mon, 16 Mar 2026 22:39:42 GMT  
		Size: 105.5 MB (105456645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8a0298689508852560a9b43e262470b1a74cc3ccff8a3d14a31ee75498d6d8`  
		Last Modified: Mon, 16 Mar 2026 22:39:40 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ad287e587a659f04865cf56e1c25c2429089f6c1f52a165dac9b5fcbd8c900`  
		Last Modified: Mon, 16 Mar 2026 22:39:40 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880f56f9032fbc2271389d30b0bdc1b1bf570f47676d478433ce3ab7a166a466`  
		Last Modified: Mon, 16 Mar 2026 22:39:41 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ba2ed9334cc296114edf25811e1da5f2b8bc0bbc9fcdb211cdf22409aafb5b`  
		Last Modified: Mon, 16 Mar 2026 22:39:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:6afc4563ac34384961c9de16a1cc849ce87e8911105a2ef15a3b30c4080ab030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236a4110a5a3dc5bb082c6413b7e3f6342a46f877be58042079fdcc40c3fc797`

```dockerfile
```

-	Layers:
	-	`sha256:50d91288bdf8dbefe8d82af16a41d1155445ed47499a386e3cb855ca17bf445e`  
		Last Modified: Mon, 16 Mar 2026 22:39:39 GMT  
		Size: 4.2 MB (4184421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eee46221c3433800b2766ed95c9678823c45e95ea106e1d4fec6a2f459021a4e`  
		Last Modified: Mon, 16 Mar 2026 22:39:39 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:bd747ed44d406d384f33363bbaaad0d9ccda0acfbeabd73718e3db9892346c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141419542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:920df9f28ec471d86800c350b48526603b535e18988460c0b86def9a79ab08ec`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:41:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 16 Mar 2026 22:41:19 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Mon, 16 Mar 2026 22:41:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:41:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 16 Mar 2026 22:41:29 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 16 Mar 2026 22:41:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:41:34 GMT
ENV COUCHDB_VERSION=3.5.1
# Mon, 16 Mar 2026 22:41:34 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 16 Mar 2026 22:41:49 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 16 Mar 2026 22:41:49 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Mon, 16 Mar 2026 22:41:49 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Mon, 16 Mar 2026 22:41:49 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 16 Mar 2026 22:41:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 16 Mar 2026 22:41:49 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:41:49 GMT
VOLUME [/opt/couchdb/data]
# Mon, 16 Mar 2026 22:41:49 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Mon, 16 Mar 2026 22:41:49 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa0cede3e0f2feab974ae02f2598d3cf7a37a98de00dc8ca77a1aa1d8788212`  
		Last Modified: Mon, 16 Mar 2026 22:42:02 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab95ec8b9934b5998f305c64a030e2057c1be214a4aefc4531f3ace3823985c4`  
		Last Modified: Mon, 16 Mar 2026 22:42:03 GMT  
		Size: 7.7 MB (7692626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247749839ec175fd2a5832e25afe9657afa5cd019baec5473f36d6d1e26eae8f`  
		Last Modified: Mon, 16 Mar 2026 22:42:03 GMT  
		Size: 370.5 KB (370540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051efd7db244ccf55863f859f8d20493333ca87363c0c74747b6120a7e0ee126`  
		Last Modified: Mon, 16 Mar 2026 22:42:03 GMT  
		Size: 76.5 KB (76497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b637b3e217e5f0c59e445e8f5e4bb003c989cb223ee76a84d92a63ff6d0ad433`  
		Last Modified: Mon, 16 Mar 2026 22:42:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926d3d79e57918a1a7be1747233fc784944a4d627798ff5761be52eae4a39699`  
		Last Modified: Mon, 16 Mar 2026 22:42:06 GMT  
		Size: 105.2 MB (105158381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdcd6eb0ed723eacd9c7cc3abd0b3417ce5d9d9347240981340f6b315dc71f08`  
		Last Modified: Mon, 16 Mar 2026 22:42:04 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916be7e299bc935d7a1cbb1d26db7b76dfe339cd959447ae913c8337a451e55c`  
		Last Modified: Mon, 16 Mar 2026 22:42:04 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c369c463533f5530fb59e35bbc53495e1f2e9947cf76f8c1d20a2a2478f6da0`  
		Last Modified: Mon, 16 Mar 2026 22:42:05 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498e0ac80a1e4b597724b8d3c18b0c4c0d5e8750d6508e6c0f14878cc25d769e`  
		Last Modified: Mon, 16 Mar 2026 22:42:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:5928b2369a9e9031686de5954d21abf01b838ff103feb5fc9127a2587f2f735d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d004aa4f1fdb43f8fcc2cd2f4aa6c1a8089ebe3a71d43f9a46b69874775146b7`

```dockerfile
```

-	Layers:
	-	`sha256:0dbe5aa4df470af5d65145a5a772ee21b194622a9777309a1ecee94be8b065f9`  
		Last Modified: Mon, 16 Mar 2026 22:42:03 GMT  
		Size: 4.2 MB (4184714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89213b5f6c98eb7f62ad0bade139c868ea00c06d2d41c0f61756193e303c5b82`  
		Last Modified: Mon, 16 Mar 2026 22:42:02 GMT  
		Size: 31.9 KB (31932 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3` - linux; s390x

```console
$ docker pull couchdb@sha256:af5747db0f4972ca2fc79f4503e409147de823df2bccff1cf422c52f2aada6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138772796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77c530165a69d2ab9249c0c74f0246e42b9fd11ca3cae2a096bd25ef915c0299`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:45:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 16 Mar 2026 23:45:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Mon, 16 Mar 2026 23:45:41 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:45:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 16 Mar 2026 23:45:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 16 Mar 2026 23:45:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:45:50 GMT
ENV COUCHDB_VERSION=3.5.1
# Mon, 16 Mar 2026 23:45:50 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 16 Mar 2026 23:46:09 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 16 Mar 2026 23:46:09 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Mon, 16 Mar 2026 23:46:09 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Mon, 16 Mar 2026 23:46:09 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 16 Mar 2026 23:46:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 16 Mar 2026 23:46:09 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:46:09 GMT
VOLUME [/opt/couchdb/data]
# Mon, 16 Mar 2026 23:46:09 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Mon, 16 Mar 2026 23:46:09 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc166a58c1fecf673f62f4091d42d02f4c1a894c2ed565839038726ebc18da34`  
		Last Modified: Mon, 16 Mar 2026 23:46:31 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ea42a57cb5bb763d81d353dd9b7f2a13324471f99e3ddbe45a2e2989c4ce94`  
		Last Modified: Mon, 16 Mar 2026 23:46:32 GMT  
		Size: 7.4 MB (7398917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c95fef27f09197a9d00c0cd752b8c6c2625641c9b1ae06a9f3b65ce561a241`  
		Last Modified: Mon, 16 Mar 2026 23:46:32 GMT  
		Size: 372.1 KB (372134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ee185bb90f593b326ce3a58df49f4242fc146fbd6bccaa5934d7b7f4c387ec`  
		Last Modified: Mon, 16 Mar 2026 23:46:32 GMT  
		Size: 76.5 KB (76531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2e75ce37eda500f02cad45c83748a647b05c95f5414948e891d98743032bbe`  
		Last Modified: Mon, 16 Mar 2026 23:46:32 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5935131b751bb1611b8f3bd484db9b35fdd626b426f3bf75395a7378f667d2a3`  
		Last Modified: Mon, 16 Mar 2026 23:46:35 GMT  
		Size: 104.0 MB (104028262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd32eeff5fdce3a2fb3ba53b84f9fb55da2206400831970d75fb298be8acc89`  
		Last Modified: Mon, 16 Mar 2026 23:46:33 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2463cbce9627643b9ad93c3e025e804d27b5ac30d1605ad2e2c97424c4499365`  
		Last Modified: Mon, 16 Mar 2026 23:46:33 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575d09b033ac2de54b68066760e536851b48162e3df744ac0001e894032fd44c`  
		Last Modified: Mon, 16 Mar 2026 23:46:33 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0bb59c495c83c952fe0e50cd5e58508526dc1423883150d6b275601cc870384`  
		Last Modified: Mon, 16 Mar 2026 23:46:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3` - unknown; unknown

```console
$ docker pull couchdb@sha256:e99bb4a3846df8987d45c6651c16de26dcea9ce7a293c279a0995fca6ea98026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1aad3b61d898ba3de99497a8ad2f81915ae32f297b34bc3c48e9609ceff0055`

```dockerfile
```

-	Layers:
	-	`sha256:fe1e2f4e222df784e3b44f9027b43a7885c62b96326dbce298ce196e495a01ee`  
		Last Modified: Mon, 16 Mar 2026 23:46:32 GMT  
		Size: 4.2 MB (4180617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f7e76a1f23c3f7c2e57afbcb85e5fe646786f593b79909f10a0494b9b95e6d6`  
		Last Modified: Mon, 16 Mar 2026 23:46:32 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:9131624a2131e47988a97a31896b16bf1846128eada06797a9ed9da89490857d
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
$ docker pull couchdb@sha256:66905a5091a2cb2d8faa52dcf9b3f425436511a400948185a6324b145a3ead93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156462320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9198f3fae5b768ddc9db9cb20ecc30e590d0601ecbb530f430866b9300a855bb`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:39:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 16 Mar 2026 22:39:12 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Mon, 16 Mar 2026 22:39:19 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:39:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:39:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 16 Mar 2026 22:39:29 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 16 Mar 2026 22:39:33 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:39:34 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 16 Mar 2026 22:39:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Mon, 16 Mar 2026 22:39:42 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Mon, 16 Mar 2026 22:39:42 GMT
VOLUME [/opt/nouveau/data]
# Mon, 16 Mar 2026 22:39:42 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Mon, 16 Mar 2026 22:39:42 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731285356d8ffd8aedfad1aed43867e332b75e30bfdf9681aefcca45338d8896`  
		Last Modified: Mon, 16 Mar 2026 22:39:57 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a26c8268c825aab0756aeeb3481f797d234b1e286e6c28b4265e13119cb893b`  
		Last Modified: Mon, 16 Mar 2026 22:39:58 GMT  
		Size: 7.9 MB (7883132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9703690c74d9b76a45a46284d2ee88525d362745cf641ccd169b32311cca003e`  
		Last Modified: Mon, 16 Mar 2026 22:39:59 GMT  
		Size: 77.4 MB (77380945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ca46e15625a6d3698f9968da1380d36b091e2b7144e45553163060d15b8119`  
		Last Modified: Mon, 16 Mar 2026 22:39:57 GMT  
		Size: 424.2 KB (424171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf181de51e309059919ad2ad9383104015306ce0d2ee3807e9688cf2dfed83d9`  
		Last Modified: Mon, 16 Mar 2026 22:39:58 GMT  
		Size: 99.6 KB (99571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1b194683ffb9128556d678c203b7fd4888b2f101a80cbb618345b3d5d28e98`  
		Last Modified: Mon, 16 Mar 2026 22:39:59 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd12494842a1c1b590f98078b31baa917f2578e09bef508117c40ab3d357c60`  
		Last Modified: Mon, 16 Mar 2026 22:40:00 GMT  
		Size: 42.4 MB (42436398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a1f74366cfdea0c9c80e6b3b1560bfef9502eec9d692d8ab66caeabcac50b0`  
		Last Modified: Mon, 16 Mar 2026 22:39:59 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:02ac1ee8b5495efa2305d9047b1531e1456414e822f913652f3aad3f00b0e89b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc3877860a24054a3732394082c42fe3060878ce3dbcf7536b916429209628e1`

```dockerfile
```

-	Layers:
	-	`sha256:8151da2ee8b4c9aac062d9f41dfb6598b3711e4371025976470e84eacf2d6a1e`  
		Last Modified: Mon, 16 Mar 2026 22:39:58 GMT  
		Size: 3.7 MB (3658095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfebd7cf8faa51447a8d0d1dc0d68052cb21d2542213015661eb527a4c1e9dd3`  
		Last Modified: Mon, 16 Mar 2026 22:39:57 GMT  
		Size: 24.5 KB (24520 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:67e1816539e9a8be804df46ff78ba7516bd2ced3266955e63835f72ec5cda23c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155360103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f4cc0c51afbbeacc94515778d92a8c9303f0f755b7e340387b138c379516de4`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:41:30 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 16 Mar 2026 22:41:30 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Mon, 16 Mar 2026 22:41:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:41:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:41:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 16 Mar 2026 22:41:46 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 16 Mar 2026 22:41:51 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:41:51 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 16 Mar 2026 22:41:57 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Mon, 16 Mar 2026 22:41:57 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Mon, 16 Mar 2026 22:41:57 GMT
VOLUME [/opt/nouveau/data]
# Mon, 16 Mar 2026 22:41:57 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Mon, 16 Mar 2026 22:41:57 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647d502d24ceda4a9ffb5ba91dd37ec0c9faabcc9618ab5c05cb2dba3b60632c`  
		Last Modified: Mon, 16 Mar 2026 22:42:12 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be31a244f834e522c326842143ed6cfa249c7db1a7ad28d8fdf9192965a613a3`  
		Last Modified: Mon, 16 Mar 2026 22:42:13 GMT  
		Size: 7.7 MB (7692625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57187c9b797f2e598ee9448b32073c5c1ca3d0508e27f8fb57622240eb1109ea`  
		Last Modified: Mon, 16 Mar 2026 22:42:14 GMT  
		Size: 76.7 MB (76718106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbbdf92a381ba8dc15e5f09435196852c0820ee2f6de754cea8dffe4081bbd2f`  
		Last Modified: Mon, 16 Mar 2026 22:42:12 GMT  
		Size: 392.8 KB (392782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402d5668fa0902310e61a2d8abb9373fc0fa404fd91addec453e3282ab95263a`  
		Last Modified: Mon, 16 Mar 2026 22:42:13 GMT  
		Size: 99.5 KB (99526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3645681b17e5838ee92375f15a60a4f1ef038f23b6e273950e3a49a1f2359fef`  
		Last Modified: Mon, 16 Mar 2026 22:42:14 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6207cf8be8d10e457f3ba1b5d68f232c38dde96ae4453b4d485fc9aa70968bf6`  
		Last Modified: Mon, 16 Mar 2026 22:42:15 GMT  
		Size: 42.3 MB (42339121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df304f4d7099faf91a38aafaac4eb4edec144058bf368bf89beac3bb5c5925ab`  
		Last Modified: Mon, 16 Mar 2026 22:42:15 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:4f75ad6c12897da3b90c2534dc61a7dc30f333e364f8c79b6f62c8a3f14fc53f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1bf1f8e59d851fb471b307823cf69a2307e87f7b2cf453b3ab54abb1e90a7b0`

```dockerfile
```

-	Layers:
	-	`sha256:b708fd00f30db03ad2eaa0a7446b6ba620d01c8e94725fa5465cc77875e9d926`  
		Last Modified: Mon, 16 Mar 2026 22:42:13 GMT  
		Size: 3.7 MB (3656771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e07e1d954c28520f75a7a85638e23d0d5ffb0459d9ee16ad25c431136230356`  
		Last Modified: Mon, 16 Mar 2026 22:42:12 GMT  
		Size: 24.7 KB (24702 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:c00d3875277b6386cdf7709ca2808d800fb368b48efb5554ae90791960a16c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150104353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be86fde285318abe8d08d14cd350066922fd5cfa9187b3ea2e8b8b6e09416983`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:45:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 16 Mar 2026 23:45:40 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Mon, 16 Mar 2026 23:45:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:45:57 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:46:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 16 Mar 2026 23:46:00 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 16 Mar 2026 23:46:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:46:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 16 Mar 2026 23:46:15 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Mon, 16 Mar 2026 23:46:15 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Mon, 16 Mar 2026 23:46:15 GMT
VOLUME [/opt/nouveau/data]
# Mon, 16 Mar 2026 23:46:15 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Mon, 16 Mar 2026 23:46:15 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c57d0d4d67f1b7850461e58b4dbc1b6771cbb6147287762efe57e268eefa050`  
		Last Modified: Mon, 16 Mar 2026 23:46:39 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead2b9e87fa033ef3a2c809f138a3052ce37861b4688f7de9a8fa4f6a0a85673`  
		Last Modified: Mon, 16 Mar 2026 23:46:39 GMT  
		Size: 7.4 MB (7398874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42cf98c81f3f7f12e2ffe62c5e1009f2f79bb77b12f552059a00f02ee2235ec1`  
		Last Modified: Mon, 16 Mar 2026 23:46:41 GMT  
		Size: 73.2 MB (73153258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926820605d727ee3e3118c3b7cc60f95c71c38e82ab803660985ccfde8df7fc9`  
		Last Modified: Mon, 16 Mar 2026 23:46:39 GMT  
		Size: 394.5 KB (394495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fd6c34999dfa17d424cb6622b58e1355e1cca15aec39c35d9ace220404926e`  
		Last Modified: Mon, 16 Mar 2026 23:46:40 GMT  
		Size: 99.7 KB (99652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659c4d047264922ab946f0e2895c568726f22aa892106cb1dc63e2e3f9b90bca`  
		Last Modified: Mon, 16 Mar 2026 23:46:40 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86411987cdffa1ddbd11e9751ce270b79d11b6170e51c091f182a67bbe6da44a`  
		Last Modified: Mon, 16 Mar 2026 23:46:41 GMT  
		Size: 42.2 MB (42164685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0f2c7986c542887266ca0ff8fac9ef11ec63bdd6cb943fc3a25a977628e287`  
		Last Modified: Mon, 16 Mar 2026 23:46:41 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:48ce01a40fbd76d4cd6f015fbbeccd5b933781944eccbd7b8580a01025947bca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b43ef97c599286611639239310304ed8d633682b51d4d1e87a9d336d23c582dc`

```dockerfile
```

-	Layers:
	-	`sha256:ff359d876897ced71471bd3d9e3ef094e7ff5eebe1444aa9fe63846e04ecdfcc`  
		Last Modified: Mon, 16 Mar 2026 23:46:39 GMT  
		Size: 3.6 MB (3648624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:116509699b8a1419ddb07c9a0f6792df743f8f6c8a99e00c77a7a3cd5a5807c5`  
		Last Modified: Mon, 16 Mar 2026 23:46:39 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4`

```console
$ docker pull couchdb@sha256:2641368fd06ff44da69262933b3fbaa3e326ba70416efb99fa5872ec8d123412
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
$ docker pull couchdb@sha256:926fad9ca6fc86b37d8bfe560190581ce9597b6fc84190a628b0a64290a366a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139023177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df9738c5322a779f3e0dbc82276f339dbc94b5ad624024ad8c0543080a70253`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:39:28 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 16 Mar 2026 22:39:28 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Mon, 16 Mar 2026 22:39:35 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:39:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 16 Mar 2026 22:39:37 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 16 Mar 2026 22:39:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:39:42 GMT
ENV COUCHDB_VERSION=3.4.3
# Mon, 16 Mar 2026 22:39:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 16 Mar 2026 22:39:56 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 16 Mar 2026 22:39:56 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Mon, 16 Mar 2026 22:39:56 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Mon, 16 Mar 2026 22:39:56 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 16 Mar 2026 22:39:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 16 Mar 2026 22:39:56 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:39:56 GMT
VOLUME [/opt/couchdb/data]
# Mon, 16 Mar 2026 22:39:56 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Mon, 16 Mar 2026 22:39:56 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7f6d43ffd06f8d0ea0811a9d23ab6744279844f13189595e2fbf1f0305ea6c`  
		Last Modified: Mon, 16 Mar 2026 22:40:08 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6a8933278ed56372e9bcc404756f13dac4917a77fa36fad17b8a731b371f28`  
		Last Modified: Mon, 16 Mar 2026 22:40:08 GMT  
		Size: 7.9 MB (7883127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a330e842dbc8791ea2735db8301ac44eeb3b238a29ea74579358fdcecad5db6b`  
		Last Modified: Mon, 16 Mar 2026 22:40:08 GMT  
		Size: 401.8 KB (401789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a5c9f0ee4a93751dc5b2e1cc20d49257884404b381370715664f8838542213`  
		Last Modified: Mon, 16 Mar 2026 22:40:08 GMT  
		Size: 76.5 KB (76520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c054aeeb6f6662a9b6b376245dc67d64b37365357f01bd640e59eafce494e623`  
		Last Modified: Mon, 16 Mar 2026 22:40:09 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecdbac21ca19f10329d3f2079af74f8ec7169d02bfa8777c0f9b15f196205e0c`  
		Last Modified: Mon, 16 Mar 2026 22:40:12 GMT  
		Size: 102.4 MB (102420086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17379dbc4fa662f2dcd1d2a45cc7649d4b06c921ad662766343edd205605a7b2`  
		Last Modified: Mon, 16 Mar 2026 22:40:09 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1516d3baf0db9da95da3e5786c00ca8b3518f61cf0e257be153816a7b1bc2557`  
		Last Modified: Mon, 16 Mar 2026 22:40:10 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e056e3878c49f29950849bbdee404f330c1442726c98138299517e5f0ffefe7`  
		Last Modified: Mon, 16 Mar 2026 22:40:11 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab32146bccdff32f0a355f5cf2a2a16085f536e64b231f6617c302f6c8d39ed5`  
		Last Modified: Mon, 16 Mar 2026 22:40:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:2948d9da3e88d2142536b8efbfa3217f9f94134beb636a7d0bd03b118fe7b8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc97339586c75fe90e907a3639698d5cac22cc6361facd33d05287bdea5f564`

```dockerfile
```

-	Layers:
	-	`sha256:e8d15221f8cca57f33e24506d0cec3fcc0595c90298ec6b38140fa18f7f445c6`  
		Last Modified: Mon, 16 Mar 2026 22:40:08 GMT  
		Size: 4.1 MB (4125395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a4822f5fb9ff08384db66d558842c1c99110f3d4505fbc099ef605439e149f5`  
		Last Modified: Mon, 16 Mar 2026 22:40:08 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:4237acf4ff3b6db177d98c04904abbfcc20ed026e96516bf616e1f390e0add3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138430138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ff8b8952d79fa26c72f62e99d9be271c0691b10300e523192eff1f578a55d9`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:41:24 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 16 Mar 2026 22:41:24 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Mon, 16 Mar 2026 22:41:30 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:41:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 16 Mar 2026 22:41:33 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 16 Mar 2026 22:41:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:41:39 GMT
ENV COUCHDB_VERSION=3.4.3
# Mon, 16 Mar 2026 22:41:39 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 16 Mar 2026 22:41:51 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 16 Mar 2026 22:41:51 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Mon, 16 Mar 2026 22:41:51 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Mon, 16 Mar 2026 22:41:52 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 16 Mar 2026 22:41:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 16 Mar 2026 22:41:52 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:41:52 GMT
VOLUME [/opt/couchdb/data]
# Mon, 16 Mar 2026 22:41:52 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Mon, 16 Mar 2026 22:41:52 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2d61e7d6b6680bdca5959014c9264c3873376dc6c3e6a1db20804f39672583`  
		Last Modified: Mon, 16 Mar 2026 22:42:04 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38cfcce32e0125ef1b5a9ebc0c6412e601fc8d87ea0dd0388c45ae11e3bdf834`  
		Last Modified: Mon, 16 Mar 2026 22:42:05 GMT  
		Size: 7.7 MB (7692600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8982ae8e2ae8444f423626f7771b1d11db46454520e225c167f3b4670e6be3`  
		Last Modified: Mon, 16 Mar 2026 22:42:04 GMT  
		Size: 370.5 KB (370535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783b273feb4c8e3dbc80c9b51815d9d186275d3270774d96cd42ecbfa5cdf96c`  
		Last Modified: Mon, 16 Mar 2026 22:42:04 GMT  
		Size: 76.5 KB (76479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02cec2e74b106340767d53ec5c71731e946a629685402574850c3763d72401e8`  
		Last Modified: Mon, 16 Mar 2026 22:42:05 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d452147d11d0de8b1ca4463e75d0ca588b765b2f53a5db00feb147a53206bd`  
		Last Modified: Mon, 16 Mar 2026 22:42:08 GMT  
		Size: 102.2 MB (102169033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d740654cafcccf06d25a63530e804c527555d463b0d6a1fe53c080d6ec8ed1`  
		Last Modified: Mon, 16 Mar 2026 22:42:06 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59c07832ddfb4eb5d288dc4afc4125eba201922e0259a83eda5480b1adfc90e`  
		Last Modified: Mon, 16 Mar 2026 22:42:07 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3973f57ca37e7c36d988db27840e0854b0e588d615c8069d929c1364df05722`  
		Last Modified: Mon, 16 Mar 2026 22:42:07 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8956a38725079b7b8ccd04bf98196eedb7bbdd2366935089cf8cd845cd830d`  
		Last Modified: Mon, 16 Mar 2026 22:42:07 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:cd5ac7707fd71953231cfb4d5d639e5e054a00541520f55cf7e5183f356ea7a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a14d2b7872f368f60637d8dc46e9988bf839439ecfd700e35733f740568b25e`

```dockerfile
```

-	Layers:
	-	`sha256:ca414d682a4fb75885d86e52a98b99d6f7dc0a55ae45dc6b3a729b22ccfa9c36`  
		Last Modified: Mon, 16 Mar 2026 22:42:04 GMT  
		Size: 4.1 MB (4125664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:185a81e0152b676ee6236093754dac1d071287035b7271d0d4055a877a313162`  
		Last Modified: Mon, 16 Mar 2026 22:42:04 GMT  
		Size: 31.3 KB (31318 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4` - linux; s390x

```console
$ docker pull couchdb@sha256:b9d25298907e4e8d57425de1c680f5b37a7bad610d9b8c7207c7793d88153d2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135801039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd2e1944666ab1a13b982c68847d1e62b98c28aa4582cc9a4288ade4e71adb5`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:45:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 16 Mar 2026 23:45:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Mon, 16 Mar 2026 23:45:41 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:45:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 16 Mar 2026 23:45:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 16 Mar 2026 23:45:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:45:50 GMT
ENV COUCHDB_VERSION=3.4.3
# Mon, 16 Mar 2026 23:46:10 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 16 Mar 2026 23:46:31 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 16 Mar 2026 23:46:31 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Mon, 16 Mar 2026 23:46:31 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Mon, 16 Mar 2026 23:46:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 16 Mar 2026 23:46:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 16 Mar 2026 23:46:31 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:46:31 GMT
VOLUME [/opt/couchdb/data]
# Mon, 16 Mar 2026 23:46:31 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Mon, 16 Mar 2026 23:46:31 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc166a58c1fecf673f62f4091d42d02f4c1a894c2ed565839038726ebc18da34`  
		Last Modified: Mon, 16 Mar 2026 23:46:31 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ea42a57cb5bb763d81d353dd9b7f2a13324471f99e3ddbe45a2e2989c4ce94`  
		Last Modified: Mon, 16 Mar 2026 23:46:32 GMT  
		Size: 7.4 MB (7398917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c95fef27f09197a9d00c0cd752b8c6c2625641c9b1ae06a9f3b65ce561a241`  
		Last Modified: Mon, 16 Mar 2026 23:46:32 GMT  
		Size: 372.1 KB (372134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ee185bb90f593b326ce3a58df49f4242fc146fbd6bccaa5934d7b7f4c387ec`  
		Last Modified: Mon, 16 Mar 2026 23:46:32 GMT  
		Size: 76.5 KB (76531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50438832476f9590e313874bf32c6d3dd7a56bf4cea02b320ad530aaeeb1ef6c`  
		Last Modified: Mon, 16 Mar 2026 23:46:53 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab0df748a76ff644f9928e218a7e4b42bfc4b0400268566dd3aaab0bdd3931a`  
		Last Modified: Mon, 16 Mar 2026 23:46:55 GMT  
		Size: 101.1 MB (101056511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac63f9039d6119d239a6ce6cd86cb5e58695a66f2a3e5edbe44a628f930d6e0`  
		Last Modified: Mon, 16 Mar 2026 23:46:53 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca954fb3bc9ebba2b67e63674b3bbe0b6e1fc36028e6be089c2688e7f2b1b02c`  
		Last Modified: Mon, 16 Mar 2026 23:46:53 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7261cdc9eb4ef9ccc3f3527571d8b016258e85697a2a04270754572069ff9525`  
		Last Modified: Mon, 16 Mar 2026 23:46:54 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7596e010743783aaca3aa84bff240975307327bb9bfe77fe2b0abb18b732732`  
		Last Modified: Mon, 16 Mar 2026 23:46:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4` - unknown; unknown

```console
$ docker pull couchdb@sha256:807eebc1bbc2df93dac2d39514b1675cd1d0774b9464ad9d1a96cba4cd29c2aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd99094057ec10c8f3f698f32a49fb19cdbef1d6d9d4bfc8a6bf138484be689c`

```dockerfile
```

-	Layers:
	-	`sha256:d82310ed89e53786481bc9765cb2879cc3d23739bee01643533a53a5d90ec4b1`  
		Last Modified: Mon, 16 Mar 2026 23:46:53 GMT  
		Size: 4.1 MB (4121591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bae12379b7ca756888747962bc0adce7a3d812dd75fe3c6d474ed32bd8d3fe9`  
		Last Modified: Mon, 16 Mar 2026 23:46:53 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4-nouveau`

```console
$ docker pull couchdb@sha256:db7d0cf6b00c02c664773ce5c30384db9a41a4dcd4eab7fa80a2e0ca5155bde7
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
$ docker pull couchdb@sha256:a48c56a33b7ff8abb111a9e70d963b0c8d8f5a3eb22f494f1640ba007c6effcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156462091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df780bb069f43116e810e177148314c6493e728b5f53fcd79ed128c8526e31b6`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:39:33 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 16 Mar 2026 22:39:33 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Mon, 16 Mar 2026 22:39:39 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:39:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:39:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 16 Mar 2026 22:39:50 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 16 Mar 2026 22:39:54 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:39:54 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
VOLUME [/opt/nouveau/data]
# Mon, 16 Mar 2026 22:39:59 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Mon, 16 Mar 2026 22:39:59 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b329fb32c5536437f8e32472e82cd9badfb76316c6ac9aff647a26ff999ec3`  
		Last Modified: Mon, 16 Mar 2026 22:40:15 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6942320a49a9c7c46a6e2da4944b4cdb6bf471174a45d43f325aef1a427813c6`  
		Last Modified: Mon, 16 Mar 2026 22:40:15 GMT  
		Size: 7.9 MB (7883159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd189a624b871cdaa59b7b82f5de281244acb2b203e59e539a399107c91db3`  
		Last Modified: Mon, 16 Mar 2026 22:40:17 GMT  
		Size: 77.4 MB (77380918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e570bbdc668e1e0c01bceed8cec6cdee309bb3d4179ab28fc74a5bd1e92063`  
		Last Modified: Mon, 16 Mar 2026 22:40:15 GMT  
		Size: 424.2 KB (424182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e76ce018e738a88ae944fbd1098e0661a56da16e7ec7f046a97ef9616fe5ce5`  
		Last Modified: Mon, 16 Mar 2026 22:40:16 GMT  
		Size: 99.6 KB (99596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004d151e1fd5bb12743b222d6b06f8fd831a730f291415add31460c037e1b361`  
		Last Modified: Mon, 16 Mar 2026 22:40:16 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71dbccacb9e674a31322ed46e36132c9a9be2f6a6a6db9fe16ecb906aaf5f316`  
		Last Modified: Mon, 16 Mar 2026 22:40:18 GMT  
		Size: 42.4 MB (42436133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa55979e1105fde4d8878765d8fae14f59157620babf9207b7217cb822a2306`  
		Last Modified: Mon, 16 Mar 2026 22:40:17 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:e0306e94f35a8680ebd9a21b95870cd42f86e7575d29ac257067503584f9c94b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1188be2c2c8c170212e2e4f78edbdf4c7a3447df3497deb36a520ced0dd0a371`

```dockerfile
```

-	Layers:
	-	`sha256:fb28122faa45d205d189133e242c7b479b9be0dcad319cb456c431243d1b167b`  
		Last Modified: Mon, 16 Mar 2026 22:40:15 GMT  
		Size: 3.7 MB (3657789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:724ccad8d0cc5b3ef58c9fa25a380f70142ccc0188a5bb55179da73361060fbb`  
		Last Modified: Mon, 16 Mar 2026 22:40:15 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:496142c24e906d909b641bad53ff6c0cab5f642d55cd311fce2cd87207a04c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155359074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed00ae91e1015f8540718247448727fb5446d315202beaf53e2268823085b2d`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:41:54 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 16 Mar 2026 22:41:54 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Mon, 16 Mar 2026 22:42:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:42:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:42:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 16 Mar 2026 22:42:10 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 16 Mar 2026 22:42:15 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:42:15 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 16 Mar 2026 22:42:27 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Mon, 16 Mar 2026 22:42:27 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Mon, 16 Mar 2026 22:42:27 GMT
VOLUME [/opt/nouveau/data]
# Mon, 16 Mar 2026 22:42:27 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Mon, 16 Mar 2026 22:42:27 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527f92b0cf38b93ab0f729f59ef1cfa5a618689189639512b035ee06abb3e398`  
		Last Modified: Mon, 16 Mar 2026 22:42:43 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6fb02e30e1fbb0e7f9f5d9dbb5f865e12e32fe9c80b2c15a31259c11a890b1e`  
		Last Modified: Mon, 16 Mar 2026 22:42:43 GMT  
		Size: 7.7 MB (7692667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929812bfb95d55a99158bdb2c2716143074f07c4c10a80584e81267956798be3`  
		Last Modified: Mon, 16 Mar 2026 22:42:45 GMT  
		Size: 76.7 MB (76718080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7475bbc273be6dd1cf1d1dbfd00e0f17a70b238d908e144d50a7c5fe25f24c`  
		Last Modified: Mon, 16 Mar 2026 22:42:43 GMT  
		Size: 392.8 KB (392778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa62316e33a7fdf6b42088503724a89a9fd294cd750bc6d82f3dc7b54caf9355`  
		Last Modified: Mon, 16 Mar 2026 22:42:44 GMT  
		Size: 99.5 KB (99515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1722d5d0e4a82da0f8a133ca1ad2b226714747621581f943ccdd4900e083aed7`  
		Last Modified: Mon, 16 Mar 2026 22:42:44 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97f4289cd81cddd890422380cdc8b6edc001e8129661c659877e96bd59255b4`  
		Last Modified: Mon, 16 Mar 2026 22:42:45 GMT  
		Size: 42.3 MB (42338090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c86f1701de7537f70e01ecd36baa93ec21e20cf538d8f07d283103d346f8da6`  
		Last Modified: Mon, 16 Mar 2026 22:42:45 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:dc6e647de92c2aaed159fa082eb52dc4f922f7ed1ef6e593af7c5cc9933d5c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3680838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3204b878f61de21d2cd42c208478b9af8646d8af1244c6ce146e9fb1e2f8339`

```dockerfile
```

-	Layers:
	-	`sha256:389b6052318e4f2b39492da36a3becca45ac3878edb85aebcf9cccd0244e5569`  
		Last Modified: Mon, 16 Mar 2026 22:42:43 GMT  
		Size: 3.7 MB (3656453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55b88ae5c72501bb8c829c557014afa02189253d30c7269c2c36a2e27de48e43`  
		Last Modified: Mon, 16 Mar 2026 22:42:43 GMT  
		Size: 24.4 KB (24385 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:17eef9bf826dc6d727eec4895fa5a3ae0339eb7df853c22bd66779805a9b9144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150102675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6220e22236a640fd9096573ace12a3cd512cc07bbc3a1be0b44f517270338d8f`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:46:57 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 16 Mar 2026 23:46:57 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Mon, 16 Mar 2026 23:47:04 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:47:13 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:47:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 16 Mar 2026 23:47:16 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 16 Mar 2026 23:47:22 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:47:22 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 16 Mar 2026 23:47:31 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Mon, 16 Mar 2026 23:47:31 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Mon, 16 Mar 2026 23:47:31 GMT
VOLUME [/opt/nouveau/data]
# Mon, 16 Mar 2026 23:47:31 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Mon, 16 Mar 2026 23:47:31 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e98f43d430848e87e5d7e60f2e567a57605442e27999cc53c9e3f18c1a48af8`  
		Last Modified: Mon, 16 Mar 2026 23:47:57 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3573e7276856d9ca05d35b596c8c4ad6a1782850ada079e59fd8c077a7cdd8`  
		Last Modified: Mon, 16 Mar 2026 23:47:57 GMT  
		Size: 7.4 MB (7398894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed280b867f6d3bfa21800706e6a2bc7f23a133f820dc12cd5f6e373002b16934`  
		Last Modified: Mon, 16 Mar 2026 23:47:59 GMT  
		Size: 73.2 MB (73153303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab30776f4a5e54b053534bce840176fadc444fa618f002e5f17f4927159e5bdf`  
		Last Modified: Mon, 16 Mar 2026 23:47:57 GMT  
		Size: 394.5 KB (394485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0fbc6cedb2b56f6864f422bb6aa00bb609ed27dd5f514c9e402051ec7131ff`  
		Last Modified: Mon, 16 Mar 2026 23:47:58 GMT  
		Size: 99.6 KB (99638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f4d65b9f39f4f2d8f6bd7165fbb16ef668d3dde146bb215c5383cef1c0a24f`  
		Last Modified: Mon, 16 Mar 2026 23:47:58 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a8dc6fdd94510465ee4f31f80cfc6ad355f0244844bfc38bd9d0ba3be31391`  
		Last Modified: Mon, 16 Mar 2026 23:47:59 GMT  
		Size: 42.2 MB (42162962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a7fa0339fb6450a6e021a36108459912b3ee0e6bd08140a20a092b05bd3277`  
		Last Modified: Mon, 16 Mar 2026 23:47:59 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:a2e389f2d31fdaf4311f6d940e0bffedcd8af95f9a38c2c010c9461065e2f0bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3672533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ced39999c40494493e1687ed42ae2ae3203ca26617eb2ec9aaed5eb452ae9a0`

```dockerfile
```

-	Layers:
	-	`sha256:85c128c6e14963ff3f94759ccab3cc0df574b6675e1c226c28965ae01d9c454c`  
		Last Modified: Mon, 16 Mar 2026 23:47:57 GMT  
		Size: 3.6 MB (3648318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c4411b6ce809bac74b382e6d32f277fbb01f525b3173e7ece8ad3717a8198bc`  
		Last Modified: Mon, 16 Mar 2026 23:47:57 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3`

```console
$ docker pull couchdb@sha256:2641368fd06ff44da69262933b3fbaa3e326ba70416efb99fa5872ec8d123412
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
$ docker pull couchdb@sha256:926fad9ca6fc86b37d8bfe560190581ce9597b6fc84190a628b0a64290a366a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139023177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df9738c5322a779f3e0dbc82276f339dbc94b5ad624024ad8c0543080a70253`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:39:28 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 16 Mar 2026 22:39:28 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Mon, 16 Mar 2026 22:39:35 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:39:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 16 Mar 2026 22:39:37 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 16 Mar 2026 22:39:42 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:39:42 GMT
ENV COUCHDB_VERSION=3.4.3
# Mon, 16 Mar 2026 22:39:43 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 16 Mar 2026 22:39:56 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 16 Mar 2026 22:39:56 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Mon, 16 Mar 2026 22:39:56 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Mon, 16 Mar 2026 22:39:56 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 16 Mar 2026 22:39:56 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 16 Mar 2026 22:39:56 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:39:56 GMT
VOLUME [/opt/couchdb/data]
# Mon, 16 Mar 2026 22:39:56 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Mon, 16 Mar 2026 22:39:56 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7f6d43ffd06f8d0ea0811a9d23ab6744279844f13189595e2fbf1f0305ea6c`  
		Last Modified: Mon, 16 Mar 2026 22:40:08 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6a8933278ed56372e9bcc404756f13dac4917a77fa36fad17b8a731b371f28`  
		Last Modified: Mon, 16 Mar 2026 22:40:08 GMT  
		Size: 7.9 MB (7883127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a330e842dbc8791ea2735db8301ac44eeb3b238a29ea74579358fdcecad5db6b`  
		Last Modified: Mon, 16 Mar 2026 22:40:08 GMT  
		Size: 401.8 KB (401789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a5c9f0ee4a93751dc5b2e1cc20d49257884404b381370715664f8838542213`  
		Last Modified: Mon, 16 Mar 2026 22:40:08 GMT  
		Size: 76.5 KB (76520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c054aeeb6f6662a9b6b376245dc67d64b37365357f01bd640e59eafce494e623`  
		Last Modified: Mon, 16 Mar 2026 22:40:09 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecdbac21ca19f10329d3f2079af74f8ec7169d02bfa8777c0f9b15f196205e0c`  
		Last Modified: Mon, 16 Mar 2026 22:40:12 GMT  
		Size: 102.4 MB (102420086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17379dbc4fa662f2dcd1d2a45cc7649d4b06c921ad662766343edd205605a7b2`  
		Last Modified: Mon, 16 Mar 2026 22:40:09 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1516d3baf0db9da95da3e5786c00ca8b3518f61cf0e257be153816a7b1bc2557`  
		Last Modified: Mon, 16 Mar 2026 22:40:10 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e056e3878c49f29950849bbdee404f330c1442726c98138299517e5f0ffefe7`  
		Last Modified: Mon, 16 Mar 2026 22:40:11 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab32146bccdff32f0a355f5cf2a2a16085f536e64b231f6617c302f6c8d39ed5`  
		Last Modified: Mon, 16 Mar 2026 22:40:11 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:2948d9da3e88d2142536b8efbfa3217f9f94134beb636a7d0bd03b118fe7b8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc97339586c75fe90e907a3639698d5cac22cc6361facd33d05287bdea5f564`

```dockerfile
```

-	Layers:
	-	`sha256:e8d15221f8cca57f33e24506d0cec3fcc0595c90298ec6b38140fa18f7f445c6`  
		Last Modified: Mon, 16 Mar 2026 22:40:08 GMT  
		Size: 4.1 MB (4125395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a4822f5fb9ff08384db66d558842c1c99110f3d4505fbc099ef605439e149f5`  
		Last Modified: Mon, 16 Mar 2026 22:40:08 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:4237acf4ff3b6db177d98c04904abbfcc20ed026e96516bf616e1f390e0add3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138430138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ff8b8952d79fa26c72f62e99d9be271c0691b10300e523192eff1f578a55d9`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:41:24 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 16 Mar 2026 22:41:24 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Mon, 16 Mar 2026 22:41:30 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:41:33 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 16 Mar 2026 22:41:33 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 16 Mar 2026 22:41:39 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:41:39 GMT
ENV COUCHDB_VERSION=3.4.3
# Mon, 16 Mar 2026 22:41:39 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 16 Mar 2026 22:41:51 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 16 Mar 2026 22:41:51 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Mon, 16 Mar 2026 22:41:51 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Mon, 16 Mar 2026 22:41:52 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 16 Mar 2026 22:41:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 16 Mar 2026 22:41:52 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:41:52 GMT
VOLUME [/opt/couchdb/data]
# Mon, 16 Mar 2026 22:41:52 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Mon, 16 Mar 2026 22:41:52 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2d61e7d6b6680bdca5959014c9264c3873376dc6c3e6a1db20804f39672583`  
		Last Modified: Mon, 16 Mar 2026 22:42:04 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38cfcce32e0125ef1b5a9ebc0c6412e601fc8d87ea0dd0388c45ae11e3bdf834`  
		Last Modified: Mon, 16 Mar 2026 22:42:05 GMT  
		Size: 7.7 MB (7692600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8982ae8e2ae8444f423626f7771b1d11db46454520e225c167f3b4670e6be3`  
		Last Modified: Mon, 16 Mar 2026 22:42:04 GMT  
		Size: 370.5 KB (370535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783b273feb4c8e3dbc80c9b51815d9d186275d3270774d96cd42ecbfa5cdf96c`  
		Last Modified: Mon, 16 Mar 2026 22:42:04 GMT  
		Size: 76.5 KB (76479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02cec2e74b106340767d53ec5c71731e946a629685402574850c3763d72401e8`  
		Last Modified: Mon, 16 Mar 2026 22:42:05 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d452147d11d0de8b1ca4463e75d0ca588b765b2f53a5db00feb147a53206bd`  
		Last Modified: Mon, 16 Mar 2026 22:42:08 GMT  
		Size: 102.2 MB (102169033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d740654cafcccf06d25a63530e804c527555d463b0d6a1fe53c080d6ec8ed1`  
		Last Modified: Mon, 16 Mar 2026 22:42:06 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59c07832ddfb4eb5d288dc4afc4125eba201922e0259a83eda5480b1adfc90e`  
		Last Modified: Mon, 16 Mar 2026 22:42:07 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3973f57ca37e7c36d988db27840e0854b0e588d615c8069d929c1364df05722`  
		Last Modified: Mon, 16 Mar 2026 22:42:07 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8956a38725079b7b8ccd04bf98196eedb7bbdd2366935089cf8cd845cd830d`  
		Last Modified: Mon, 16 Mar 2026 22:42:07 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:cd5ac7707fd71953231cfb4d5d639e5e054a00541520f55cf7e5183f356ea7a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4156982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a14d2b7872f368f60637d8dc46e9988bf839439ecfd700e35733f740568b25e`

```dockerfile
```

-	Layers:
	-	`sha256:ca414d682a4fb75885d86e52a98b99d6f7dc0a55ae45dc6b3a729b22ccfa9c36`  
		Last Modified: Mon, 16 Mar 2026 22:42:04 GMT  
		Size: 4.1 MB (4125664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:185a81e0152b676ee6236093754dac1d071287035b7271d0d4055a877a313162`  
		Last Modified: Mon, 16 Mar 2026 22:42:04 GMT  
		Size: 31.3 KB (31318 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3` - linux; s390x

```console
$ docker pull couchdb@sha256:b9d25298907e4e8d57425de1c680f5b37a7bad610d9b8c7207c7793d88153d2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135801039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd2e1944666ab1a13b982c68847d1e62b98c28aa4582cc9a4288ade4e71adb5`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:45:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 16 Mar 2026 23:45:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Mon, 16 Mar 2026 23:45:41 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:45:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 16 Mar 2026 23:45:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 16 Mar 2026 23:45:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:45:50 GMT
ENV COUCHDB_VERSION=3.4.3
# Mon, 16 Mar 2026 23:46:10 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 16 Mar 2026 23:46:31 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 16 Mar 2026 23:46:31 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Mon, 16 Mar 2026 23:46:31 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Mon, 16 Mar 2026 23:46:31 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 16 Mar 2026 23:46:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 16 Mar 2026 23:46:31 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:46:31 GMT
VOLUME [/opt/couchdb/data]
# Mon, 16 Mar 2026 23:46:31 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Mon, 16 Mar 2026 23:46:31 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc166a58c1fecf673f62f4091d42d02f4c1a894c2ed565839038726ebc18da34`  
		Last Modified: Mon, 16 Mar 2026 23:46:31 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ea42a57cb5bb763d81d353dd9b7f2a13324471f99e3ddbe45a2e2989c4ce94`  
		Last Modified: Mon, 16 Mar 2026 23:46:32 GMT  
		Size: 7.4 MB (7398917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c95fef27f09197a9d00c0cd752b8c6c2625641c9b1ae06a9f3b65ce561a241`  
		Last Modified: Mon, 16 Mar 2026 23:46:32 GMT  
		Size: 372.1 KB (372134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ee185bb90f593b326ce3a58df49f4242fc146fbd6bccaa5934d7b7f4c387ec`  
		Last Modified: Mon, 16 Mar 2026 23:46:32 GMT  
		Size: 76.5 KB (76531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50438832476f9590e313874bf32c6d3dd7a56bf4cea02b320ad530aaeeb1ef6c`  
		Last Modified: Mon, 16 Mar 2026 23:46:53 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab0df748a76ff644f9928e218a7e4b42bfc4b0400268566dd3aaab0bdd3931a`  
		Last Modified: Mon, 16 Mar 2026 23:46:55 GMT  
		Size: 101.1 MB (101056511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac63f9039d6119d239a6ce6cd86cb5e58695a66f2a3e5edbe44a628f930d6e0`  
		Last Modified: Mon, 16 Mar 2026 23:46:53 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca954fb3bc9ebba2b67e63674b3bbe0b6e1fc36028e6be089c2688e7f2b1b02c`  
		Last Modified: Mon, 16 Mar 2026 23:46:53 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7261cdc9eb4ef9ccc3f3527571d8b016258e85697a2a04270754572069ff9525`  
		Last Modified: Mon, 16 Mar 2026 23:46:54 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7596e010743783aaca3aa84bff240975307327bb9bfe77fe2b0abb18b732732`  
		Last Modified: Mon, 16 Mar 2026 23:46:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3` - unknown; unknown

```console
$ docker pull couchdb@sha256:807eebc1bbc2df93dac2d39514b1675cd1d0774b9464ad9d1a96cba4cd29c2aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4152739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd99094057ec10c8f3f698f32a49fb19cdbef1d6d9d4bfc8a6bf138484be689c`

```dockerfile
```

-	Layers:
	-	`sha256:d82310ed89e53786481bc9765cb2879cc3d23739bee01643533a53a5d90ec4b1`  
		Last Modified: Mon, 16 Mar 2026 23:46:53 GMT  
		Size: 4.1 MB (4121591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bae12379b7ca756888747962bc0adce7a3d812dd75fe3c6d474ed32bd8d3fe9`  
		Last Modified: Mon, 16 Mar 2026 23:46:53 GMT  
		Size: 31.1 KB (31148 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.4.3-nouveau`

```console
$ docker pull couchdb@sha256:db7d0cf6b00c02c664773ce5c30384db9a41a4dcd4eab7fa80a2e0ca5155bde7
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
$ docker pull couchdb@sha256:a48c56a33b7ff8abb111a9e70d963b0c8d8f5a3eb22f494f1640ba007c6effcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156462091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df780bb069f43116e810e177148314c6493e728b5f53fcd79ed128c8526e31b6`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:39:33 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 16 Mar 2026 22:39:33 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Mon, 16 Mar 2026 22:39:39 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:39:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:39:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 16 Mar 2026 22:39:50 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 16 Mar 2026 22:39:54 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:39:54 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Mon, 16 Mar 2026 22:39:59 GMT
VOLUME [/opt/nouveau/data]
# Mon, 16 Mar 2026 22:39:59 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Mon, 16 Mar 2026 22:39:59 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b329fb32c5536437f8e32472e82cd9badfb76316c6ac9aff647a26ff999ec3`  
		Last Modified: Mon, 16 Mar 2026 22:40:15 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6942320a49a9c7c46a6e2da4944b4cdb6bf471174a45d43f325aef1a427813c6`  
		Last Modified: Mon, 16 Mar 2026 22:40:15 GMT  
		Size: 7.9 MB (7883159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd189a624b871cdaa59b7b82f5de281244acb2b203e59e539a399107c91db3`  
		Last Modified: Mon, 16 Mar 2026 22:40:17 GMT  
		Size: 77.4 MB (77380918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e570bbdc668e1e0c01bceed8cec6cdee309bb3d4179ab28fc74a5bd1e92063`  
		Last Modified: Mon, 16 Mar 2026 22:40:15 GMT  
		Size: 424.2 KB (424182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e76ce018e738a88ae944fbd1098e0661a56da16e7ec7f046a97ef9616fe5ce5`  
		Last Modified: Mon, 16 Mar 2026 22:40:16 GMT  
		Size: 99.6 KB (99596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004d151e1fd5bb12743b222d6b06f8fd831a730f291415add31460c037e1b361`  
		Last Modified: Mon, 16 Mar 2026 22:40:16 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71dbccacb9e674a31322ed46e36132c9a9be2f6a6a6db9fe16ecb906aaf5f316`  
		Last Modified: Mon, 16 Mar 2026 22:40:18 GMT  
		Size: 42.4 MB (42436133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa55979e1105fde4d8878765d8fae14f59157620babf9207b7217cb822a2306`  
		Last Modified: Mon, 16 Mar 2026 22:40:17 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:e0306e94f35a8680ebd9a21b95870cd42f86e7575d29ac257067503584f9c94b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1188be2c2c8c170212e2e4f78edbdf4c7a3447df3497deb36a520ced0dd0a371`

```dockerfile
```

-	Layers:
	-	`sha256:fb28122faa45d205d189133e242c7b479b9be0dcad319cb456c431243d1b167b`  
		Last Modified: Mon, 16 Mar 2026 22:40:15 GMT  
		Size: 3.7 MB (3657789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:724ccad8d0cc5b3ef58c9fa25a380f70142ccc0188a5bb55179da73361060fbb`  
		Last Modified: Mon, 16 Mar 2026 22:40:15 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:496142c24e906d909b641bad53ff6c0cab5f642d55cd311fce2cd87207a04c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155359074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed00ae91e1015f8540718247448727fb5446d315202beaf53e2268823085b2d`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:41:54 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 16 Mar 2026 22:41:54 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Mon, 16 Mar 2026 22:42:01 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:42:08 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:42:10 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 16 Mar 2026 22:42:10 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 16 Mar 2026 22:42:15 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:42:15 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 16 Mar 2026 22:42:27 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Mon, 16 Mar 2026 22:42:27 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Mon, 16 Mar 2026 22:42:27 GMT
VOLUME [/opt/nouveau/data]
# Mon, 16 Mar 2026 22:42:27 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Mon, 16 Mar 2026 22:42:27 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:527f92b0cf38b93ab0f729f59ef1cfa5a618689189639512b035ee06abb3e398`  
		Last Modified: Mon, 16 Mar 2026 22:42:43 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6fb02e30e1fbb0e7f9f5d9dbb5f865e12e32fe9c80b2c15a31259c11a890b1e`  
		Last Modified: Mon, 16 Mar 2026 22:42:43 GMT  
		Size: 7.7 MB (7692667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929812bfb95d55a99158bdb2c2716143074f07c4c10a80584e81267956798be3`  
		Last Modified: Mon, 16 Mar 2026 22:42:45 GMT  
		Size: 76.7 MB (76718080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7475bbc273be6dd1cf1d1dbfd00e0f17a70b238d908e144d50a7c5fe25f24c`  
		Last Modified: Mon, 16 Mar 2026 22:42:43 GMT  
		Size: 392.8 KB (392778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa62316e33a7fdf6b42088503724a89a9fd294cd750bc6d82f3dc7b54caf9355`  
		Last Modified: Mon, 16 Mar 2026 22:42:44 GMT  
		Size: 99.5 KB (99515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1722d5d0e4a82da0f8a133ca1ad2b226714747621581f943ccdd4900e083aed7`  
		Last Modified: Mon, 16 Mar 2026 22:42:44 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97f4289cd81cddd890422380cdc8b6edc001e8129661c659877e96bd59255b4`  
		Last Modified: Mon, 16 Mar 2026 22:42:45 GMT  
		Size: 42.3 MB (42338090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c86f1701de7537f70e01ecd36baa93ec21e20cf538d8f07d283103d346f8da6`  
		Last Modified: Mon, 16 Mar 2026 22:42:45 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:dc6e647de92c2aaed159fa082eb52dc4f922f7ed1ef6e593af7c5cc9933d5c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3680838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3204b878f61de21d2cd42c208478b9af8646d8af1244c6ce146e9fb1e2f8339`

```dockerfile
```

-	Layers:
	-	`sha256:389b6052318e4f2b39492da36a3becca45ac3878edb85aebcf9cccd0244e5569`  
		Last Modified: Mon, 16 Mar 2026 22:42:43 GMT  
		Size: 3.7 MB (3656453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55b88ae5c72501bb8c829c557014afa02189253d30c7269c2c36a2e27de48e43`  
		Last Modified: Mon, 16 Mar 2026 22:42:43 GMT  
		Size: 24.4 KB (24385 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.4.3-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:17eef9bf826dc6d727eec4895fa5a3ae0339eb7df853c22bd66779805a9b9144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150102675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6220e22236a640fd9096573ace12a3cd512cc07bbc3a1be0b44f517270338d8f`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:46:57 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 16 Mar 2026 23:46:57 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Mon, 16 Mar 2026 23:47:04 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:47:13 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:47:16 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 16 Mar 2026 23:47:16 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 16 Mar 2026 23:47:22 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:47:22 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 16 Mar 2026 23:47:31 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.4.3~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Mon, 16 Mar 2026 23:47:31 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Mon, 16 Mar 2026 23:47:31 GMT
VOLUME [/opt/nouveau/data]
# Mon, 16 Mar 2026 23:47:31 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Mon, 16 Mar 2026 23:47:31 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e98f43d430848e87e5d7e60f2e567a57605442e27999cc53c9e3f18c1a48af8`  
		Last Modified: Mon, 16 Mar 2026 23:47:57 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3573e7276856d9ca05d35b596c8c4ad6a1782850ada079e59fd8c077a7cdd8`  
		Last Modified: Mon, 16 Mar 2026 23:47:57 GMT  
		Size: 7.4 MB (7398894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed280b867f6d3bfa21800706e6a2bc7f23a133f820dc12cd5f6e373002b16934`  
		Last Modified: Mon, 16 Mar 2026 23:47:59 GMT  
		Size: 73.2 MB (73153303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab30776f4a5e54b053534bce840176fadc444fa618f002e5f17f4927159e5bdf`  
		Last Modified: Mon, 16 Mar 2026 23:47:57 GMT  
		Size: 394.5 KB (394485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0fbc6cedb2b56f6864f422bb6aa00bb609ed27dd5f514c9e402051ec7131ff`  
		Last Modified: Mon, 16 Mar 2026 23:47:58 GMT  
		Size: 99.6 KB (99638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f4d65b9f39f4f2d8f6bd7165fbb16ef668d3dde146bb215c5383cef1c0a24f`  
		Last Modified: Mon, 16 Mar 2026 23:47:58 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a8dc6fdd94510465ee4f31f80cfc6ad355f0244844bfc38bd9d0ba3be31391`  
		Last Modified: Mon, 16 Mar 2026 23:47:59 GMT  
		Size: 42.2 MB (42162962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a7fa0339fb6450a6e021a36108459912b3ee0e6bd08140a20a092b05bd3277`  
		Last Modified: Mon, 16 Mar 2026 23:47:59 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.4.3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:a2e389f2d31fdaf4311f6d940e0bffedcd8af95f9a38c2c010c9461065e2f0bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3672533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ced39999c40494493e1687ed42ae2ae3203ca26617eb2ec9aaed5eb452ae9a0`

```dockerfile
```

-	Layers:
	-	`sha256:85c128c6e14963ff3f94759ccab3cc0df574b6675e1c226c28965ae01d9c454c`  
		Last Modified: Mon, 16 Mar 2026 23:47:57 GMT  
		Size: 3.6 MB (3648318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c4411b6ce809bac74b382e6d32f277fbb01f525b3173e7ece8ad3717a8198bc`  
		Last Modified: Mon, 16 Mar 2026 23:47:57 GMT  
		Size: 24.2 KB (24215 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5`

```console
$ docker pull couchdb@sha256:24c854639f2f14f346caa10c80f9f246c656b869020bb171b3afd375c02098f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.5` - linux; amd64

```console
$ docker pull couchdb@sha256:414799d7a687c714246d1d6c8033b00e34fff4060a7b9ff92cdb82669d532a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142059762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:595b13672075944f8455e1500533e469a7208c52d8b432abeb86afd1afabffaa`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:38:58 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 16 Mar 2026 22:38:58 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Mon, 16 Mar 2026 22:39:04 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:39:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 16 Mar 2026 22:39:06 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 16 Mar 2026 22:39:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:39:11 GMT
ENV COUCHDB_VERSION=3.5.1
# Mon, 16 Mar 2026 22:39:11 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 16 Mar 2026 22:39:25 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 16 Mar 2026 22:39:26 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Mon, 16 Mar 2026 22:39:26 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Mon, 16 Mar 2026 22:39:26 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 16 Mar 2026 22:39:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 16 Mar 2026 22:39:26 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:39:26 GMT
VOLUME [/opt/couchdb/data]
# Mon, 16 Mar 2026 22:39:26 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Mon, 16 Mar 2026 22:39:26 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef9f6538a75b47d65696d8725a4856d08435f55fb49544f7d5765fdd2fe9f21`  
		Last Modified: Mon, 16 Mar 2026 22:39:39 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1d4c09467ad6a157a8fc64695003e96208a72cbb3f879feb6f75389e9c79d0`  
		Last Modified: Mon, 16 Mar 2026 22:39:39 GMT  
		Size: 7.9 MB (7883135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1923c6e324517621c74d21a82203c23bfcf8688ad7244d63fa1f1230c21971`  
		Last Modified: Mon, 16 Mar 2026 22:39:39 GMT  
		Size: 401.8 KB (401785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2ab6b8f282ff901e21be15bceb055824bb30a8bbc59ce8186e78c6ef512d64`  
		Last Modified: Mon, 16 Mar 2026 22:39:39 GMT  
		Size: 76.5 KB (76540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c837407581c764041f008e2ec54e18db3174a03e2c8949d8c09c8ce91c64cb`  
		Last Modified: Mon, 16 Mar 2026 22:39:40 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bf3899d4ad55fa4b2b0974dc50d0df3ac2f650ead5ee7a8a67d5a6ac360b5f`  
		Last Modified: Mon, 16 Mar 2026 22:39:42 GMT  
		Size: 105.5 MB (105456645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8a0298689508852560a9b43e262470b1a74cc3ccff8a3d14a31ee75498d6d8`  
		Last Modified: Mon, 16 Mar 2026 22:39:40 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ad287e587a659f04865cf56e1c25c2429089f6c1f52a165dac9b5fcbd8c900`  
		Last Modified: Mon, 16 Mar 2026 22:39:40 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880f56f9032fbc2271389d30b0bdc1b1bf570f47676d478433ce3ab7a166a466`  
		Last Modified: Mon, 16 Mar 2026 22:39:41 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ba2ed9334cc296114edf25811e1da5f2b8bc0bbc9fcdb211cdf22409aafb5b`  
		Last Modified: Mon, 16 Mar 2026 22:39:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:6afc4563ac34384961c9de16a1cc849ce87e8911105a2ef15a3b30c4080ab030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236a4110a5a3dc5bb082c6413b7e3f6342a46f877be58042079fdcc40c3fc797`

```dockerfile
```

-	Layers:
	-	`sha256:50d91288bdf8dbefe8d82af16a41d1155445ed47499a386e3cb855ca17bf445e`  
		Last Modified: Mon, 16 Mar 2026 22:39:39 GMT  
		Size: 4.2 MB (4184421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eee46221c3433800b2766ed95c9678823c45e95ea106e1d4fec6a2f459021a4e`  
		Last Modified: Mon, 16 Mar 2026 22:39:39 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:bd747ed44d406d384f33363bbaaad0d9ccda0acfbeabd73718e3db9892346c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141419542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:920df9f28ec471d86800c350b48526603b535e18988460c0b86def9a79ab08ec`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:41:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 16 Mar 2026 22:41:19 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Mon, 16 Mar 2026 22:41:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:41:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 16 Mar 2026 22:41:29 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 16 Mar 2026 22:41:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:41:34 GMT
ENV COUCHDB_VERSION=3.5.1
# Mon, 16 Mar 2026 22:41:34 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 16 Mar 2026 22:41:49 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 16 Mar 2026 22:41:49 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Mon, 16 Mar 2026 22:41:49 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Mon, 16 Mar 2026 22:41:49 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 16 Mar 2026 22:41:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 16 Mar 2026 22:41:49 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:41:49 GMT
VOLUME [/opt/couchdb/data]
# Mon, 16 Mar 2026 22:41:49 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Mon, 16 Mar 2026 22:41:49 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa0cede3e0f2feab974ae02f2598d3cf7a37a98de00dc8ca77a1aa1d8788212`  
		Last Modified: Mon, 16 Mar 2026 22:42:02 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab95ec8b9934b5998f305c64a030e2057c1be214a4aefc4531f3ace3823985c4`  
		Last Modified: Mon, 16 Mar 2026 22:42:03 GMT  
		Size: 7.7 MB (7692626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247749839ec175fd2a5832e25afe9657afa5cd019baec5473f36d6d1e26eae8f`  
		Last Modified: Mon, 16 Mar 2026 22:42:03 GMT  
		Size: 370.5 KB (370540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051efd7db244ccf55863f859f8d20493333ca87363c0c74747b6120a7e0ee126`  
		Last Modified: Mon, 16 Mar 2026 22:42:03 GMT  
		Size: 76.5 KB (76497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b637b3e217e5f0c59e445e8f5e4bb003c989cb223ee76a84d92a63ff6d0ad433`  
		Last Modified: Mon, 16 Mar 2026 22:42:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926d3d79e57918a1a7be1747233fc784944a4d627798ff5761be52eae4a39699`  
		Last Modified: Mon, 16 Mar 2026 22:42:06 GMT  
		Size: 105.2 MB (105158381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdcd6eb0ed723eacd9c7cc3abd0b3417ce5d9d9347240981340f6b315dc71f08`  
		Last Modified: Mon, 16 Mar 2026 22:42:04 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916be7e299bc935d7a1cbb1d26db7b76dfe339cd959447ae913c8337a451e55c`  
		Last Modified: Mon, 16 Mar 2026 22:42:04 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c369c463533f5530fb59e35bbc53495e1f2e9947cf76f8c1d20a2a2478f6da0`  
		Last Modified: Mon, 16 Mar 2026 22:42:05 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498e0ac80a1e4b597724b8d3c18b0c4c0d5e8750d6508e6c0f14878cc25d769e`  
		Last Modified: Mon, 16 Mar 2026 22:42:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:5928b2369a9e9031686de5954d21abf01b838ff103feb5fc9127a2587f2f735d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d004aa4f1fdb43f8fcc2cd2f4aa6c1a8089ebe3a71d43f9a46b69874775146b7`

```dockerfile
```

-	Layers:
	-	`sha256:0dbe5aa4df470af5d65145a5a772ee21b194622a9777309a1ecee94be8b065f9`  
		Last Modified: Mon, 16 Mar 2026 22:42:03 GMT  
		Size: 4.2 MB (4184714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89213b5f6c98eb7f62ad0bade139c868ea00c06d2d41c0f61756193e303c5b82`  
		Last Modified: Mon, 16 Mar 2026 22:42:02 GMT  
		Size: 31.9 KB (31932 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5` - linux; s390x

```console
$ docker pull couchdb@sha256:af5747db0f4972ca2fc79f4503e409147de823df2bccff1cf422c52f2aada6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138772796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77c530165a69d2ab9249c0c74f0246e42b9fd11ca3cae2a096bd25ef915c0299`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:45:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 16 Mar 2026 23:45:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Mon, 16 Mar 2026 23:45:41 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:45:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 16 Mar 2026 23:45:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 16 Mar 2026 23:45:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:45:50 GMT
ENV COUCHDB_VERSION=3.5.1
# Mon, 16 Mar 2026 23:45:50 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 16 Mar 2026 23:46:09 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 16 Mar 2026 23:46:09 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Mon, 16 Mar 2026 23:46:09 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Mon, 16 Mar 2026 23:46:09 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 16 Mar 2026 23:46:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 16 Mar 2026 23:46:09 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:46:09 GMT
VOLUME [/opt/couchdb/data]
# Mon, 16 Mar 2026 23:46:09 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Mon, 16 Mar 2026 23:46:09 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc166a58c1fecf673f62f4091d42d02f4c1a894c2ed565839038726ebc18da34`  
		Last Modified: Mon, 16 Mar 2026 23:46:31 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ea42a57cb5bb763d81d353dd9b7f2a13324471f99e3ddbe45a2e2989c4ce94`  
		Last Modified: Mon, 16 Mar 2026 23:46:32 GMT  
		Size: 7.4 MB (7398917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c95fef27f09197a9d00c0cd752b8c6c2625641c9b1ae06a9f3b65ce561a241`  
		Last Modified: Mon, 16 Mar 2026 23:46:32 GMT  
		Size: 372.1 KB (372134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ee185bb90f593b326ce3a58df49f4242fc146fbd6bccaa5934d7b7f4c387ec`  
		Last Modified: Mon, 16 Mar 2026 23:46:32 GMT  
		Size: 76.5 KB (76531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2e75ce37eda500f02cad45c83748a647b05c95f5414948e891d98743032bbe`  
		Last Modified: Mon, 16 Mar 2026 23:46:32 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5935131b751bb1611b8f3bd484db9b35fdd626b426f3bf75395a7378f667d2a3`  
		Last Modified: Mon, 16 Mar 2026 23:46:35 GMT  
		Size: 104.0 MB (104028262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd32eeff5fdce3a2fb3ba53b84f9fb55da2206400831970d75fb298be8acc89`  
		Last Modified: Mon, 16 Mar 2026 23:46:33 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2463cbce9627643b9ad93c3e025e804d27b5ac30d1605ad2e2c97424c4499365`  
		Last Modified: Mon, 16 Mar 2026 23:46:33 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575d09b033ac2de54b68066760e536851b48162e3df744ac0001e894032fd44c`  
		Last Modified: Mon, 16 Mar 2026 23:46:33 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0bb59c495c83c952fe0e50cd5e58508526dc1423883150d6b275601cc870384`  
		Last Modified: Mon, 16 Mar 2026 23:46:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5` - unknown; unknown

```console
$ docker pull couchdb@sha256:e99bb4a3846df8987d45c6651c16de26dcea9ce7a293c279a0995fca6ea98026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1aad3b61d898ba3de99497a8ad2f81915ae32f297b34bc3c48e9609ceff0055`

```dockerfile
```

-	Layers:
	-	`sha256:fe1e2f4e222df784e3b44f9027b43a7885c62b96326dbce298ce196e495a01ee`  
		Last Modified: Mon, 16 Mar 2026 23:46:32 GMT  
		Size: 4.2 MB (4180617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f7e76a1f23c3f7c2e57afbcb85e5fe646786f593b79909f10a0494b9b95e6d6`  
		Last Modified: Mon, 16 Mar 2026 23:46:32 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5-nouveau`

```console
$ docker pull couchdb@sha256:9131624a2131e47988a97a31896b16bf1846128eada06797a9ed9da89490857d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.5-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:66905a5091a2cb2d8faa52dcf9b3f425436511a400948185a6324b145a3ead93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156462320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9198f3fae5b768ddc9db9cb20ecc30e590d0601ecbb530f430866b9300a855bb`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:39:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 16 Mar 2026 22:39:12 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Mon, 16 Mar 2026 22:39:19 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:39:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:39:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 16 Mar 2026 22:39:29 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 16 Mar 2026 22:39:33 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:39:34 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 16 Mar 2026 22:39:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Mon, 16 Mar 2026 22:39:42 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Mon, 16 Mar 2026 22:39:42 GMT
VOLUME [/opt/nouveau/data]
# Mon, 16 Mar 2026 22:39:42 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Mon, 16 Mar 2026 22:39:42 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731285356d8ffd8aedfad1aed43867e332b75e30bfdf9681aefcca45338d8896`  
		Last Modified: Mon, 16 Mar 2026 22:39:57 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a26c8268c825aab0756aeeb3481f797d234b1e286e6c28b4265e13119cb893b`  
		Last Modified: Mon, 16 Mar 2026 22:39:58 GMT  
		Size: 7.9 MB (7883132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9703690c74d9b76a45a46284d2ee88525d362745cf641ccd169b32311cca003e`  
		Last Modified: Mon, 16 Mar 2026 22:39:59 GMT  
		Size: 77.4 MB (77380945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ca46e15625a6d3698f9968da1380d36b091e2b7144e45553163060d15b8119`  
		Last Modified: Mon, 16 Mar 2026 22:39:57 GMT  
		Size: 424.2 KB (424171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf181de51e309059919ad2ad9383104015306ce0d2ee3807e9688cf2dfed83d9`  
		Last Modified: Mon, 16 Mar 2026 22:39:58 GMT  
		Size: 99.6 KB (99571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1b194683ffb9128556d678c203b7fd4888b2f101a80cbb618345b3d5d28e98`  
		Last Modified: Mon, 16 Mar 2026 22:39:59 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd12494842a1c1b590f98078b31baa917f2578e09bef508117c40ab3d357c60`  
		Last Modified: Mon, 16 Mar 2026 22:40:00 GMT  
		Size: 42.4 MB (42436398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a1f74366cfdea0c9c80e6b3b1560bfef9502eec9d692d8ab66caeabcac50b0`  
		Last Modified: Mon, 16 Mar 2026 22:39:59 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:02ac1ee8b5495efa2305d9047b1531e1456414e822f913652f3aad3f00b0e89b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc3877860a24054a3732394082c42fe3060878ce3dbcf7536b916429209628e1`

```dockerfile
```

-	Layers:
	-	`sha256:8151da2ee8b4c9aac062d9f41dfb6598b3711e4371025976470e84eacf2d6a1e`  
		Last Modified: Mon, 16 Mar 2026 22:39:58 GMT  
		Size: 3.7 MB (3658095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfebd7cf8faa51447a8d0d1dc0d68052cb21d2542213015661eb527a4c1e9dd3`  
		Last Modified: Mon, 16 Mar 2026 22:39:57 GMT  
		Size: 24.5 KB (24520 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:67e1816539e9a8be804df46ff78ba7516bd2ced3266955e63835f72ec5cda23c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155360103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f4cc0c51afbbeacc94515778d92a8c9303f0f755b7e340387b138c379516de4`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:41:30 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 16 Mar 2026 22:41:30 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Mon, 16 Mar 2026 22:41:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:41:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:41:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 16 Mar 2026 22:41:46 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 16 Mar 2026 22:41:51 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:41:51 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 16 Mar 2026 22:41:57 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Mon, 16 Mar 2026 22:41:57 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Mon, 16 Mar 2026 22:41:57 GMT
VOLUME [/opt/nouveau/data]
# Mon, 16 Mar 2026 22:41:57 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Mon, 16 Mar 2026 22:41:57 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647d502d24ceda4a9ffb5ba91dd37ec0c9faabcc9618ab5c05cb2dba3b60632c`  
		Last Modified: Mon, 16 Mar 2026 22:42:12 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be31a244f834e522c326842143ed6cfa249c7db1a7ad28d8fdf9192965a613a3`  
		Last Modified: Mon, 16 Mar 2026 22:42:13 GMT  
		Size: 7.7 MB (7692625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57187c9b797f2e598ee9448b32073c5c1ca3d0508e27f8fb57622240eb1109ea`  
		Last Modified: Mon, 16 Mar 2026 22:42:14 GMT  
		Size: 76.7 MB (76718106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbbdf92a381ba8dc15e5f09435196852c0820ee2f6de754cea8dffe4081bbd2f`  
		Last Modified: Mon, 16 Mar 2026 22:42:12 GMT  
		Size: 392.8 KB (392782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402d5668fa0902310e61a2d8abb9373fc0fa404fd91addec453e3282ab95263a`  
		Last Modified: Mon, 16 Mar 2026 22:42:13 GMT  
		Size: 99.5 KB (99526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3645681b17e5838ee92375f15a60a4f1ef038f23b6e273950e3a49a1f2359fef`  
		Last Modified: Mon, 16 Mar 2026 22:42:14 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6207cf8be8d10e457f3ba1b5d68f232c38dde96ae4453b4d485fc9aa70968bf6`  
		Last Modified: Mon, 16 Mar 2026 22:42:15 GMT  
		Size: 42.3 MB (42339121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df304f4d7099faf91a38aafaac4eb4edec144058bf368bf89beac3bb5c5925ab`  
		Last Modified: Mon, 16 Mar 2026 22:42:15 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:4f75ad6c12897da3b90c2534dc61a7dc30f333e364f8c79b6f62c8a3f14fc53f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1bf1f8e59d851fb471b307823cf69a2307e87f7b2cf453b3ab54abb1e90a7b0`

```dockerfile
```

-	Layers:
	-	`sha256:b708fd00f30db03ad2eaa0a7446b6ba620d01c8e94725fa5465cc77875e9d926`  
		Last Modified: Mon, 16 Mar 2026 22:42:13 GMT  
		Size: 3.7 MB (3656771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e07e1d954c28520f75a7a85638e23d0d5ffb0459d9ee16ad25c431136230356`  
		Last Modified: Mon, 16 Mar 2026 22:42:12 GMT  
		Size: 24.7 KB (24702 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:c00d3875277b6386cdf7709ca2808d800fb368b48efb5554ae90791960a16c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150104353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be86fde285318abe8d08d14cd350066922fd5cfa9187b3ea2e8b8b6e09416983`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:45:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 16 Mar 2026 23:45:40 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Mon, 16 Mar 2026 23:45:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:45:57 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:46:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 16 Mar 2026 23:46:00 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 16 Mar 2026 23:46:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:46:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 16 Mar 2026 23:46:15 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Mon, 16 Mar 2026 23:46:15 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Mon, 16 Mar 2026 23:46:15 GMT
VOLUME [/opt/nouveau/data]
# Mon, 16 Mar 2026 23:46:15 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Mon, 16 Mar 2026 23:46:15 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c57d0d4d67f1b7850461e58b4dbc1b6771cbb6147287762efe57e268eefa050`  
		Last Modified: Mon, 16 Mar 2026 23:46:39 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead2b9e87fa033ef3a2c809f138a3052ce37861b4688f7de9a8fa4f6a0a85673`  
		Last Modified: Mon, 16 Mar 2026 23:46:39 GMT  
		Size: 7.4 MB (7398874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42cf98c81f3f7f12e2ffe62c5e1009f2f79bb77b12f552059a00f02ee2235ec1`  
		Last Modified: Mon, 16 Mar 2026 23:46:41 GMT  
		Size: 73.2 MB (73153258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926820605d727ee3e3118c3b7cc60f95c71c38e82ab803660985ccfde8df7fc9`  
		Last Modified: Mon, 16 Mar 2026 23:46:39 GMT  
		Size: 394.5 KB (394495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fd6c34999dfa17d424cb6622b58e1355e1cca15aec39c35d9ace220404926e`  
		Last Modified: Mon, 16 Mar 2026 23:46:40 GMT  
		Size: 99.7 KB (99652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659c4d047264922ab946f0e2895c568726f22aa892106cb1dc63e2e3f9b90bca`  
		Last Modified: Mon, 16 Mar 2026 23:46:40 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86411987cdffa1ddbd11e9751ce270b79d11b6170e51c091f182a67bbe6da44a`  
		Last Modified: Mon, 16 Mar 2026 23:46:41 GMT  
		Size: 42.2 MB (42164685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0f2c7986c542887266ca0ff8fac9ef11ec63bdd6cb943fc3a25a977628e287`  
		Last Modified: Mon, 16 Mar 2026 23:46:41 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:48ce01a40fbd76d4cd6f015fbbeccd5b933781944eccbd7b8580a01025947bca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b43ef97c599286611639239310304ed8d633682b51d4d1e87a9d336d23c582dc`

```dockerfile
```

-	Layers:
	-	`sha256:ff359d876897ced71471bd3d9e3ef094e7ff5eebe1444aa9fe63846e04ecdfcc`  
		Last Modified: Mon, 16 Mar 2026 23:46:39 GMT  
		Size: 3.6 MB (3648624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:116509699b8a1419ddb07c9a0f6792df743f8f6c8a99e00c77a7a3cd5a5807c5`  
		Last Modified: Mon, 16 Mar 2026 23:46:39 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.1`

```console
$ docker pull couchdb@sha256:24c854639f2f14f346caa10c80f9f246c656b869020bb171b3afd375c02098f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.5.1` - linux; amd64

```console
$ docker pull couchdb@sha256:414799d7a687c714246d1d6c8033b00e34fff4060a7b9ff92cdb82669d532a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142059762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:595b13672075944f8455e1500533e469a7208c52d8b432abeb86afd1afabffaa`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:38:58 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 16 Mar 2026 22:38:58 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Mon, 16 Mar 2026 22:39:04 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:39:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 16 Mar 2026 22:39:06 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 16 Mar 2026 22:39:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:39:11 GMT
ENV COUCHDB_VERSION=3.5.1
# Mon, 16 Mar 2026 22:39:11 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 16 Mar 2026 22:39:25 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 16 Mar 2026 22:39:26 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Mon, 16 Mar 2026 22:39:26 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Mon, 16 Mar 2026 22:39:26 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 16 Mar 2026 22:39:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 16 Mar 2026 22:39:26 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:39:26 GMT
VOLUME [/opt/couchdb/data]
# Mon, 16 Mar 2026 22:39:26 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Mon, 16 Mar 2026 22:39:26 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef9f6538a75b47d65696d8725a4856d08435f55fb49544f7d5765fdd2fe9f21`  
		Last Modified: Mon, 16 Mar 2026 22:39:39 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1d4c09467ad6a157a8fc64695003e96208a72cbb3f879feb6f75389e9c79d0`  
		Last Modified: Mon, 16 Mar 2026 22:39:39 GMT  
		Size: 7.9 MB (7883135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1923c6e324517621c74d21a82203c23bfcf8688ad7244d63fa1f1230c21971`  
		Last Modified: Mon, 16 Mar 2026 22:39:39 GMT  
		Size: 401.8 KB (401785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2ab6b8f282ff901e21be15bceb055824bb30a8bbc59ce8186e78c6ef512d64`  
		Last Modified: Mon, 16 Mar 2026 22:39:39 GMT  
		Size: 76.5 KB (76540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c837407581c764041f008e2ec54e18db3174a03e2c8949d8c09c8ce91c64cb`  
		Last Modified: Mon, 16 Mar 2026 22:39:40 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bf3899d4ad55fa4b2b0974dc50d0df3ac2f650ead5ee7a8a67d5a6ac360b5f`  
		Last Modified: Mon, 16 Mar 2026 22:39:42 GMT  
		Size: 105.5 MB (105456645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8a0298689508852560a9b43e262470b1a74cc3ccff8a3d14a31ee75498d6d8`  
		Last Modified: Mon, 16 Mar 2026 22:39:40 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ad287e587a659f04865cf56e1c25c2429089f6c1f52a165dac9b5fcbd8c900`  
		Last Modified: Mon, 16 Mar 2026 22:39:40 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880f56f9032fbc2271389d30b0bdc1b1bf570f47676d478433ce3ab7a166a466`  
		Last Modified: Mon, 16 Mar 2026 22:39:41 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ba2ed9334cc296114edf25811e1da5f2b8bc0bbc9fcdb211cdf22409aafb5b`  
		Last Modified: Mon, 16 Mar 2026 22:39:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:6afc4563ac34384961c9de16a1cc849ce87e8911105a2ef15a3b30c4080ab030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236a4110a5a3dc5bb082c6413b7e3f6342a46f877be58042079fdcc40c3fc797`

```dockerfile
```

-	Layers:
	-	`sha256:50d91288bdf8dbefe8d82af16a41d1155445ed47499a386e3cb855ca17bf445e`  
		Last Modified: Mon, 16 Mar 2026 22:39:39 GMT  
		Size: 4.2 MB (4184421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eee46221c3433800b2766ed95c9678823c45e95ea106e1d4fec6a2f459021a4e`  
		Last Modified: Mon, 16 Mar 2026 22:39:39 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:bd747ed44d406d384f33363bbaaad0d9ccda0acfbeabd73718e3db9892346c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141419542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:920df9f28ec471d86800c350b48526603b535e18988460c0b86def9a79ab08ec`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:41:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 16 Mar 2026 22:41:19 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Mon, 16 Mar 2026 22:41:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:41:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 16 Mar 2026 22:41:29 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 16 Mar 2026 22:41:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:41:34 GMT
ENV COUCHDB_VERSION=3.5.1
# Mon, 16 Mar 2026 22:41:34 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 16 Mar 2026 22:41:49 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 16 Mar 2026 22:41:49 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Mon, 16 Mar 2026 22:41:49 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Mon, 16 Mar 2026 22:41:49 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 16 Mar 2026 22:41:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 16 Mar 2026 22:41:49 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:41:49 GMT
VOLUME [/opt/couchdb/data]
# Mon, 16 Mar 2026 22:41:49 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Mon, 16 Mar 2026 22:41:49 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa0cede3e0f2feab974ae02f2598d3cf7a37a98de00dc8ca77a1aa1d8788212`  
		Last Modified: Mon, 16 Mar 2026 22:42:02 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab95ec8b9934b5998f305c64a030e2057c1be214a4aefc4531f3ace3823985c4`  
		Last Modified: Mon, 16 Mar 2026 22:42:03 GMT  
		Size: 7.7 MB (7692626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247749839ec175fd2a5832e25afe9657afa5cd019baec5473f36d6d1e26eae8f`  
		Last Modified: Mon, 16 Mar 2026 22:42:03 GMT  
		Size: 370.5 KB (370540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051efd7db244ccf55863f859f8d20493333ca87363c0c74747b6120a7e0ee126`  
		Last Modified: Mon, 16 Mar 2026 22:42:03 GMT  
		Size: 76.5 KB (76497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b637b3e217e5f0c59e445e8f5e4bb003c989cb223ee76a84d92a63ff6d0ad433`  
		Last Modified: Mon, 16 Mar 2026 22:42:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926d3d79e57918a1a7be1747233fc784944a4d627798ff5761be52eae4a39699`  
		Last Modified: Mon, 16 Mar 2026 22:42:06 GMT  
		Size: 105.2 MB (105158381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdcd6eb0ed723eacd9c7cc3abd0b3417ce5d9d9347240981340f6b315dc71f08`  
		Last Modified: Mon, 16 Mar 2026 22:42:04 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916be7e299bc935d7a1cbb1d26db7b76dfe339cd959447ae913c8337a451e55c`  
		Last Modified: Mon, 16 Mar 2026 22:42:04 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c369c463533f5530fb59e35bbc53495e1f2e9947cf76f8c1d20a2a2478f6da0`  
		Last Modified: Mon, 16 Mar 2026 22:42:05 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498e0ac80a1e4b597724b8d3c18b0c4c0d5e8750d6508e6c0f14878cc25d769e`  
		Last Modified: Mon, 16 Mar 2026 22:42:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:5928b2369a9e9031686de5954d21abf01b838ff103feb5fc9127a2587f2f735d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d004aa4f1fdb43f8fcc2cd2f4aa6c1a8089ebe3a71d43f9a46b69874775146b7`

```dockerfile
```

-	Layers:
	-	`sha256:0dbe5aa4df470af5d65145a5a772ee21b194622a9777309a1ecee94be8b065f9`  
		Last Modified: Mon, 16 Mar 2026 22:42:03 GMT  
		Size: 4.2 MB (4184714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89213b5f6c98eb7f62ad0bade139c868ea00c06d2d41c0f61756193e303c5b82`  
		Last Modified: Mon, 16 Mar 2026 22:42:02 GMT  
		Size: 31.9 KB (31932 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.1` - linux; s390x

```console
$ docker pull couchdb@sha256:af5747db0f4972ca2fc79f4503e409147de823df2bccff1cf422c52f2aada6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138772796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77c530165a69d2ab9249c0c74f0246e42b9fd11ca3cae2a096bd25ef915c0299`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:45:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 16 Mar 2026 23:45:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Mon, 16 Mar 2026 23:45:41 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:45:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 16 Mar 2026 23:45:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 16 Mar 2026 23:45:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:45:50 GMT
ENV COUCHDB_VERSION=3.5.1
# Mon, 16 Mar 2026 23:45:50 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 16 Mar 2026 23:46:09 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 16 Mar 2026 23:46:09 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Mon, 16 Mar 2026 23:46:09 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Mon, 16 Mar 2026 23:46:09 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 16 Mar 2026 23:46:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 16 Mar 2026 23:46:09 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:46:09 GMT
VOLUME [/opt/couchdb/data]
# Mon, 16 Mar 2026 23:46:09 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Mon, 16 Mar 2026 23:46:09 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc166a58c1fecf673f62f4091d42d02f4c1a894c2ed565839038726ebc18da34`  
		Last Modified: Mon, 16 Mar 2026 23:46:31 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ea42a57cb5bb763d81d353dd9b7f2a13324471f99e3ddbe45a2e2989c4ce94`  
		Last Modified: Mon, 16 Mar 2026 23:46:32 GMT  
		Size: 7.4 MB (7398917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c95fef27f09197a9d00c0cd752b8c6c2625641c9b1ae06a9f3b65ce561a241`  
		Last Modified: Mon, 16 Mar 2026 23:46:32 GMT  
		Size: 372.1 KB (372134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ee185bb90f593b326ce3a58df49f4242fc146fbd6bccaa5934d7b7f4c387ec`  
		Last Modified: Mon, 16 Mar 2026 23:46:32 GMT  
		Size: 76.5 KB (76531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2e75ce37eda500f02cad45c83748a647b05c95f5414948e891d98743032bbe`  
		Last Modified: Mon, 16 Mar 2026 23:46:32 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5935131b751bb1611b8f3bd484db9b35fdd626b426f3bf75395a7378f667d2a3`  
		Last Modified: Mon, 16 Mar 2026 23:46:35 GMT  
		Size: 104.0 MB (104028262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd32eeff5fdce3a2fb3ba53b84f9fb55da2206400831970d75fb298be8acc89`  
		Last Modified: Mon, 16 Mar 2026 23:46:33 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2463cbce9627643b9ad93c3e025e804d27b5ac30d1605ad2e2c97424c4499365`  
		Last Modified: Mon, 16 Mar 2026 23:46:33 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575d09b033ac2de54b68066760e536851b48162e3df744ac0001e894032fd44c`  
		Last Modified: Mon, 16 Mar 2026 23:46:33 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0bb59c495c83c952fe0e50cd5e58508526dc1423883150d6b275601cc870384`  
		Last Modified: Mon, 16 Mar 2026 23:46:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1` - unknown; unknown

```console
$ docker pull couchdb@sha256:e99bb4a3846df8987d45c6651c16de26dcea9ce7a293c279a0995fca6ea98026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1aad3b61d898ba3de99497a8ad2f81915ae32f297b34bc3c48e9609ceff0055`

```dockerfile
```

-	Layers:
	-	`sha256:fe1e2f4e222df784e3b44f9027b43a7885c62b96326dbce298ce196e495a01ee`  
		Last Modified: Mon, 16 Mar 2026 23:46:32 GMT  
		Size: 4.2 MB (4180617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f7e76a1f23c3f7c2e57afbcb85e5fe646786f593b79909f10a0494b9b95e6d6`  
		Last Modified: Mon, 16 Mar 2026 23:46:32 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:3.5.1-nouveau`

```console
$ docker pull couchdb@sha256:9131624a2131e47988a97a31896b16bf1846128eada06797a9ed9da89490857d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `couchdb:3.5.1-nouveau` - linux; amd64

```console
$ docker pull couchdb@sha256:66905a5091a2cb2d8faa52dcf9b3f425436511a400948185a6324b145a3ead93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156462320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9198f3fae5b768ddc9db9cb20ecc30e590d0601ecbb530f430866b9300a855bb`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:39:12 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 16 Mar 2026 22:39:12 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Mon, 16 Mar 2026 22:39:19 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:39:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:39:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 16 Mar 2026 22:39:29 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 16 Mar 2026 22:39:33 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:39:34 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 16 Mar 2026 22:39:42 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Mon, 16 Mar 2026 22:39:42 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Mon, 16 Mar 2026 22:39:42 GMT
VOLUME [/opt/nouveau/data]
# Mon, 16 Mar 2026 22:39:42 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Mon, 16 Mar 2026 22:39:42 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731285356d8ffd8aedfad1aed43867e332b75e30bfdf9681aefcca45338d8896`  
		Last Modified: Mon, 16 Mar 2026 22:39:57 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a26c8268c825aab0756aeeb3481f797d234b1e286e6c28b4265e13119cb893b`  
		Last Modified: Mon, 16 Mar 2026 22:39:58 GMT  
		Size: 7.9 MB (7883132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9703690c74d9b76a45a46284d2ee88525d362745cf641ccd169b32311cca003e`  
		Last Modified: Mon, 16 Mar 2026 22:39:59 GMT  
		Size: 77.4 MB (77380945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ca46e15625a6d3698f9968da1380d36b091e2b7144e45553163060d15b8119`  
		Last Modified: Mon, 16 Mar 2026 22:39:57 GMT  
		Size: 424.2 KB (424171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf181de51e309059919ad2ad9383104015306ce0d2ee3807e9688cf2dfed83d9`  
		Last Modified: Mon, 16 Mar 2026 22:39:58 GMT  
		Size: 99.6 KB (99571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1b194683ffb9128556d678c203b7fd4888b2f101a80cbb618345b3d5d28e98`  
		Last Modified: Mon, 16 Mar 2026 22:39:59 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd12494842a1c1b590f98078b31baa917f2578e09bef508117c40ab3d357c60`  
		Last Modified: Mon, 16 Mar 2026 22:40:00 GMT  
		Size: 42.4 MB (42436398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a1f74366cfdea0c9c80e6b3b1560bfef9502eec9d692d8ab66caeabcac50b0`  
		Last Modified: Mon, 16 Mar 2026 22:39:59 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:02ac1ee8b5495efa2305d9047b1531e1456414e822f913652f3aad3f00b0e89b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3682615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc3877860a24054a3732394082c42fe3060878ce3dbcf7536b916429209628e1`

```dockerfile
```

-	Layers:
	-	`sha256:8151da2ee8b4c9aac062d9f41dfb6598b3711e4371025976470e84eacf2d6a1e`  
		Last Modified: Mon, 16 Mar 2026 22:39:58 GMT  
		Size: 3.7 MB (3658095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfebd7cf8faa51447a8d0d1dc0d68052cb21d2542213015661eb527a4c1e9dd3`  
		Last Modified: Mon, 16 Mar 2026 22:39:57 GMT  
		Size: 24.5 KB (24520 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.1-nouveau` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:67e1816539e9a8be804df46ff78ba7516bd2ced3266955e63835f72ec5cda23c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155360103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f4cc0c51afbbeacc94515778d92a8c9303f0f755b7e340387b138c379516de4`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:41:30 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 16 Mar 2026 22:41:30 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Mon, 16 Mar 2026 22:41:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:41:44 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:41:46 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 16 Mar 2026 22:41:46 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 16 Mar 2026 22:41:51 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:41:51 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 16 Mar 2026 22:41:57 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Mon, 16 Mar 2026 22:41:57 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Mon, 16 Mar 2026 22:41:57 GMT
VOLUME [/opt/nouveau/data]
# Mon, 16 Mar 2026 22:41:57 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Mon, 16 Mar 2026 22:41:57 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647d502d24ceda4a9ffb5ba91dd37ec0c9faabcc9618ab5c05cb2dba3b60632c`  
		Last Modified: Mon, 16 Mar 2026 22:42:12 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be31a244f834e522c326842143ed6cfa249c7db1a7ad28d8fdf9192965a613a3`  
		Last Modified: Mon, 16 Mar 2026 22:42:13 GMT  
		Size: 7.7 MB (7692625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57187c9b797f2e598ee9448b32073c5c1ca3d0508e27f8fb57622240eb1109ea`  
		Last Modified: Mon, 16 Mar 2026 22:42:14 GMT  
		Size: 76.7 MB (76718106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbbdf92a381ba8dc15e5f09435196852c0820ee2f6de754cea8dffe4081bbd2f`  
		Last Modified: Mon, 16 Mar 2026 22:42:12 GMT  
		Size: 392.8 KB (392782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402d5668fa0902310e61a2d8abb9373fc0fa404fd91addec453e3282ab95263a`  
		Last Modified: Mon, 16 Mar 2026 22:42:13 GMT  
		Size: 99.5 KB (99526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3645681b17e5838ee92375f15a60a4f1ef038f23b6e273950e3a49a1f2359fef`  
		Last Modified: Mon, 16 Mar 2026 22:42:14 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6207cf8be8d10e457f3ba1b5d68f232c38dde96ae4453b4d485fc9aa70968bf6`  
		Last Modified: Mon, 16 Mar 2026 22:42:15 GMT  
		Size: 42.3 MB (42339121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df304f4d7099faf91a38aafaac4eb4edec144058bf368bf89beac3bb5c5925ab`  
		Last Modified: Mon, 16 Mar 2026 22:42:15 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:4f75ad6c12897da3b90c2534dc61a7dc30f333e364f8c79b6f62c8a3f14fc53f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1bf1f8e59d851fb471b307823cf69a2307e87f7b2cf453b3ab54abb1e90a7b0`

```dockerfile
```

-	Layers:
	-	`sha256:b708fd00f30db03ad2eaa0a7446b6ba620d01c8e94725fa5465cc77875e9d926`  
		Last Modified: Mon, 16 Mar 2026 22:42:13 GMT  
		Size: 3.7 MB (3656771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e07e1d954c28520f75a7a85638e23d0d5ffb0459d9ee16ad25c431136230356`  
		Last Modified: Mon, 16 Mar 2026 22:42:12 GMT  
		Size: 24.7 KB (24702 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:3.5.1-nouveau` - linux; s390x

```console
$ docker pull couchdb@sha256:c00d3875277b6386cdf7709ca2808d800fb368b48efb5554ae90791960a16c85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150104353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be86fde285318abe8d08d14cd350066922fd5cfa9187b3ea2e8b8b6e09416983`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:45:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 16 Mar 2026 23:45:40 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Mon, 16 Mar 2026 23:45:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:45:57 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-17-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:46:00 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 16 Mar 2026 23:46:00 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 16 Mar 2026 23:46:05 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt-key list;    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:46:05 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ bookworm main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 16 Mar 2026 23:46:15 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages --no-install-recommends             couchdb-nouveau=3.5.1~bookworm;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Mon, 16 Mar 2026 23:46:15 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Mon, 16 Mar 2026 23:46:15 GMT
VOLUME [/opt/nouveau/data]
# Mon, 16 Mar 2026 23:46:15 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Mon, 16 Mar 2026 23:46:15 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c57d0d4d67f1b7850461e58b4dbc1b6771cbb6147287762efe57e268eefa050`  
		Last Modified: Mon, 16 Mar 2026 23:46:39 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead2b9e87fa033ef3a2c809f138a3052ce37861b4688f7de9a8fa4f6a0a85673`  
		Last Modified: Mon, 16 Mar 2026 23:46:39 GMT  
		Size: 7.4 MB (7398874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42cf98c81f3f7f12e2ffe62c5e1009f2f79bb77b12f552059a00f02ee2235ec1`  
		Last Modified: Mon, 16 Mar 2026 23:46:41 GMT  
		Size: 73.2 MB (73153258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926820605d727ee3e3118c3b7cc60f95c71c38e82ab803660985ccfde8df7fc9`  
		Last Modified: Mon, 16 Mar 2026 23:46:39 GMT  
		Size: 394.5 KB (394495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fd6c34999dfa17d424cb6622b58e1355e1cca15aec39c35d9ace220404926e`  
		Last Modified: Mon, 16 Mar 2026 23:46:40 GMT  
		Size: 99.7 KB (99652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659c4d047264922ab946f0e2895c568726f22aa892106cb1dc63e2e3f9b90bca`  
		Last Modified: Mon, 16 Mar 2026 23:46:40 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86411987cdffa1ddbd11e9751ce270b79d11b6170e51c091f182a67bbe6da44a`  
		Last Modified: Mon, 16 Mar 2026 23:46:41 GMT  
		Size: 42.2 MB (42164685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0f2c7986c542887266ca0ff8fac9ef11ec63bdd6cb943fc3a25a977628e287`  
		Last Modified: Mon, 16 Mar 2026 23:46:41 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3.5.1-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:48ce01a40fbd76d4cd6f015fbbeccd5b933781944eccbd7b8580a01025947bca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b43ef97c599286611639239310304ed8d633682b51d4d1e87a9d336d23c582dc`

```dockerfile
```

-	Layers:
	-	`sha256:ff359d876897ced71471bd3d9e3ef094e7ff5eebe1444aa9fe63846e04ecdfcc`  
		Last Modified: Mon, 16 Mar 2026 23:46:39 GMT  
		Size: 3.6 MB (3648624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:116509699b8a1419ddb07c9a0f6792df743f8f6c8a99e00c77a7a3cd5a5807c5`  
		Last Modified: Mon, 16 Mar 2026 23:46:39 GMT  
		Size: 24.5 KB (24521 bytes)  
		MIME: application/vnd.in-toto+json

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:24c854639f2f14f346caa10c80f9f246c656b869020bb171b3afd375c02098f0
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
$ docker pull couchdb@sha256:414799d7a687c714246d1d6c8033b00e34fff4060a7b9ff92cdb82669d532a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142059762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:595b13672075944f8455e1500533e469a7208c52d8b432abeb86afd1afabffaa`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:38:58 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 16 Mar 2026 22:38:58 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Mon, 16 Mar 2026 22:39:04 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:39:06 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 16 Mar 2026 22:39:06 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 16 Mar 2026 22:39:11 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:39:11 GMT
ENV COUCHDB_VERSION=3.5.1
# Mon, 16 Mar 2026 22:39:11 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 16 Mar 2026 22:39:25 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 16 Mar 2026 22:39:26 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Mon, 16 Mar 2026 22:39:26 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Mon, 16 Mar 2026 22:39:26 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 16 Mar 2026 22:39:26 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 16 Mar 2026 22:39:26 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:39:26 GMT
VOLUME [/opt/couchdb/data]
# Mon, 16 Mar 2026 22:39:26 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Mon, 16 Mar 2026 22:39:26 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef9f6538a75b47d65696d8725a4856d08435f55fb49544f7d5765fdd2fe9f21`  
		Last Modified: Mon, 16 Mar 2026 22:39:39 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1d4c09467ad6a157a8fc64695003e96208a72cbb3f879feb6f75389e9c79d0`  
		Last Modified: Mon, 16 Mar 2026 22:39:39 GMT  
		Size: 7.9 MB (7883135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1923c6e324517621c74d21a82203c23bfcf8688ad7244d63fa1f1230c21971`  
		Last Modified: Mon, 16 Mar 2026 22:39:39 GMT  
		Size: 401.8 KB (401785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2ab6b8f282ff901e21be15bceb055824bb30a8bbc59ce8186e78c6ef512d64`  
		Last Modified: Mon, 16 Mar 2026 22:39:39 GMT  
		Size: 76.5 KB (76540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c837407581c764041f008e2ec54e18db3174a03e2c8949d8c09c8ce91c64cb`  
		Last Modified: Mon, 16 Mar 2026 22:39:40 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bf3899d4ad55fa4b2b0974dc50d0df3ac2f650ead5ee7a8a67d5a6ac360b5f`  
		Last Modified: Mon, 16 Mar 2026 22:39:42 GMT  
		Size: 105.5 MB (105456645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8a0298689508852560a9b43e262470b1a74cc3ccff8a3d14a31ee75498d6d8`  
		Last Modified: Mon, 16 Mar 2026 22:39:40 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ad287e587a659f04865cf56e1c25c2429089f6c1f52a165dac9b5fcbd8c900`  
		Last Modified: Mon, 16 Mar 2026 22:39:40 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880f56f9032fbc2271389d30b0bdc1b1bf570f47676d478433ce3ab7a166a466`  
		Last Modified: Mon, 16 Mar 2026 22:39:41 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ba2ed9334cc296114edf25811e1da5f2b8bc0bbc9fcdb211cdf22409aafb5b`  
		Last Modified: Mon, 16 Mar 2026 22:39:41 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:6afc4563ac34384961c9de16a1cc849ce87e8911105a2ef15a3b30c4080ab030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236a4110a5a3dc5bb082c6413b7e3f6342a46f877be58042079fdcc40c3fc797`

```dockerfile
```

-	Layers:
	-	`sha256:50d91288bdf8dbefe8d82af16a41d1155445ed47499a386e3cb855ca17bf445e`  
		Last Modified: Mon, 16 Mar 2026 22:39:39 GMT  
		Size: 4.2 MB (4184421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eee46221c3433800b2766ed95c9678823c45e95ea106e1d4fec6a2f459021a4e`  
		Last Modified: Mon, 16 Mar 2026 22:39:39 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:bd747ed44d406d384f33363bbaaad0d9ccda0acfbeabd73718e3db9892346c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141419542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:920df9f28ec471d86800c350b48526603b535e18988460c0b86def9a79ab08ec`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:41:19 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 16 Mar 2026 22:41:19 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Mon, 16 Mar 2026 22:41:26 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:41:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 16 Mar 2026 22:41:29 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 16 Mar 2026 22:41:34 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:41:34 GMT
ENV COUCHDB_VERSION=3.5.1
# Mon, 16 Mar 2026 22:41:34 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 16 Mar 2026 22:41:49 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 16 Mar 2026 22:41:49 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Mon, 16 Mar 2026 22:41:49 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Mon, 16 Mar 2026 22:41:49 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 16 Mar 2026 22:41:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 16 Mar 2026 22:41:49 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:41:49 GMT
VOLUME [/opt/couchdb/data]
# Mon, 16 Mar 2026 22:41:49 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Mon, 16 Mar 2026 22:41:49 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa0cede3e0f2feab974ae02f2598d3cf7a37a98de00dc8ca77a1aa1d8788212`  
		Last Modified: Mon, 16 Mar 2026 22:42:02 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab95ec8b9934b5998f305c64a030e2057c1be214a4aefc4531f3ace3823985c4`  
		Last Modified: Mon, 16 Mar 2026 22:42:03 GMT  
		Size: 7.7 MB (7692626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247749839ec175fd2a5832e25afe9657afa5cd019baec5473f36d6d1e26eae8f`  
		Last Modified: Mon, 16 Mar 2026 22:42:03 GMT  
		Size: 370.5 KB (370540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051efd7db244ccf55863f859f8d20493333ca87363c0c74747b6120a7e0ee126`  
		Last Modified: Mon, 16 Mar 2026 22:42:03 GMT  
		Size: 76.5 KB (76497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b637b3e217e5f0c59e445e8f5e4bb003c989cb223ee76a84d92a63ff6d0ad433`  
		Last Modified: Mon, 16 Mar 2026 22:42:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926d3d79e57918a1a7be1747233fc784944a4d627798ff5761be52eae4a39699`  
		Last Modified: Mon, 16 Mar 2026 22:42:06 GMT  
		Size: 105.2 MB (105158381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdcd6eb0ed723eacd9c7cc3abd0b3417ce5d9d9347240981340f6b315dc71f08`  
		Last Modified: Mon, 16 Mar 2026 22:42:04 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916be7e299bc935d7a1cbb1d26db7b76dfe339cd959447ae913c8337a451e55c`  
		Last Modified: Mon, 16 Mar 2026 22:42:04 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c369c463533f5530fb59e35bbc53495e1f2e9947cf76f8c1d20a2a2478f6da0`  
		Last Modified: Mon, 16 Mar 2026 22:42:05 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498e0ac80a1e4b597724b8d3c18b0c4c0d5e8750d6508e6c0f14878cc25d769e`  
		Last Modified: Mon, 16 Mar 2026 22:42:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:5928b2369a9e9031686de5954d21abf01b838ff103feb5fc9127a2587f2f735d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4216646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d004aa4f1fdb43f8fcc2cd2f4aa6c1a8089ebe3a71d43f9a46b69874775146b7`

```dockerfile
```

-	Layers:
	-	`sha256:0dbe5aa4df470af5d65145a5a772ee21b194622a9777309a1ecee94be8b065f9`  
		Last Modified: Mon, 16 Mar 2026 22:42:03 GMT  
		Size: 4.2 MB (4184714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89213b5f6c98eb7f62ad0bade139c868ea00c06d2d41c0f61756193e303c5b82`  
		Last Modified: Mon, 16 Mar 2026 22:42:02 GMT  
		Size: 31.9 KB (31932 bytes)  
		MIME: application/vnd.in-toto+json

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:af5747db0f4972ca2fc79f4503e409147de823df2bccff1cf422c52f2aada6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138772796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77c530165a69d2ab9249c0c74f0246e42b9fd11ca3cae2a096bd25ef915c0299`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 23:45:35 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Mon, 16 Mar 2026 23:45:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb # buildkit
# Mon, 16 Mar 2026 23:45:41 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:45:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Mon, 16 Mar 2026 23:45:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Mon, 16 Mar 2026 23:45:50 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:45:50 GMT
ENV COUCHDB_VERSION=3.5.1
# Mon, 16 Mar 2026 23:45:50 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Mon, 16 Mar 2026 23:46:09 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bookworm     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*; # buildkit
# Mon, 16 Mar 2026 23:46:09 GMT
COPY --chown=couchdb:couchdb 10-docker-default.ini /opt/couchdb/etc/default.d/ # buildkit
# Mon, 16 Mar 2026 23:46:09 GMT
COPY --chown=couchdb:couchdb vm.args /opt/couchdb/etc/ # buildkit
# Mon, 16 Mar 2026 23:46:09 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 16 Mar 2026 23:46:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat # buildkit
# Mon, 16 Mar 2026 23:46:09 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:46:09 GMT
VOLUME [/opt/couchdb/data]
# Mon, 16 Mar 2026 23:46:09 GMT
EXPOSE map[4369/tcp:{} 5984/tcp:{} 9100/tcp:{}]
# Mon, 16 Mar 2026 23:46:09 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:3814d1a754476ec8db22d31a68bf8b939774ab72a69dcd1b72cff2f3b9a06022`  
		Last Modified: Mon, 16 Mar 2026 21:51:33 GMT  
		Size: 26.9 MB (26891515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc166a58c1fecf673f62f4091d42d02f4c1a894c2ed565839038726ebc18da34`  
		Last Modified: Mon, 16 Mar 2026 23:46:31 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ea42a57cb5bb763d81d353dd9b7f2a13324471f99e3ddbe45a2e2989c4ce94`  
		Last Modified: Mon, 16 Mar 2026 23:46:32 GMT  
		Size: 7.4 MB (7398917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c95fef27f09197a9d00c0cd752b8c6c2625641c9b1ae06a9f3b65ce561a241`  
		Last Modified: Mon, 16 Mar 2026 23:46:32 GMT  
		Size: 372.1 KB (372134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ee185bb90f593b326ce3a58df49f4242fc146fbd6bccaa5934d7b7f4c387ec`  
		Last Modified: Mon, 16 Mar 2026 23:46:32 GMT  
		Size: 76.5 KB (76531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2e75ce37eda500f02cad45c83748a647b05c95f5414948e891d98743032bbe`  
		Last Modified: Mon, 16 Mar 2026 23:46:32 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5935131b751bb1611b8f3bd484db9b35fdd626b426f3bf75395a7378f667d2a3`  
		Last Modified: Mon, 16 Mar 2026 23:46:35 GMT  
		Size: 104.0 MB (104028262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd32eeff5fdce3a2fb3ba53b84f9fb55da2206400831970d75fb298be8acc89`  
		Last Modified: Mon, 16 Mar 2026 23:46:33 GMT  
		Size: 380.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2463cbce9627643b9ad93c3e025e804d27b5ac30d1605ad2e2c97424c4499365`  
		Last Modified: Mon, 16 Mar 2026 23:46:33 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575d09b033ac2de54b68066760e536851b48162e3df744ac0001e894032fd44c`  
		Last Modified: Mon, 16 Mar 2026 23:46:33 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0bb59c495c83c952fe0e50cd5e58508526dc1423883150d6b275601cc870384`  
		Last Modified: Mon, 16 Mar 2026 23:46:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:latest` - unknown; unknown

```console
$ docker pull couchdb@sha256:e99bb4a3846df8987d45c6651c16de26dcea9ce7a293c279a0995fca6ea98026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4212355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1aad3b61d898ba3de99497a8ad2f81915ae32f297b34bc3c48e9609ceff0055`

```dockerfile
```

-	Layers:
	-	`sha256:fe1e2f4e222df784e3b44f9027b43a7885c62b96326dbce298ce196e495a01ee`  
		Last Modified: Mon, 16 Mar 2026 23:46:32 GMT  
		Size: 4.2 MB (4180617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f7e76a1f23c3f7c2e57afbcb85e5fe646786f593b79909f10a0494b9b95e6d6`  
		Last Modified: Mon, 16 Mar 2026 23:46:32 GMT  
		Size: 31.7 KB (31738 bytes)  
		MIME: application/vnd.in-toto+json
