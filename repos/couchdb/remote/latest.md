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
