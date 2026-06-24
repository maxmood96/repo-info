## `couchdb:3-nouveau`

```console
$ docker pull couchdb@sha256:8da84c776c43a47c41d97cec331c096d279774db11cf5f6d62c57aea6d22b981
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
$ docker pull couchdb@sha256:b58614245c5f6861f59c37c7370a9be54fc61087a96a9ffb9f2b712a273da2f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150060763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:410645668157d46958b1415602b102a7ab2a5128ec41b8b426df94922d5dcb93`
-	Default Command: `["\/usr\/bin\/java","-server","-Djava.awt.headless=true","-Xmx2g","-jar","\/opt\/nouveau\/lib\/nouveau-1.0-SNAPSHOT.jar","server","\/opt\/nouveau\/etc\/nouveau.yaml"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Tue, 23 Jun 2026 23:32:40 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Tue, 23 Jun 2026 23:32:40 GMT
RUN groupadd -g 5984 -r nouveau && useradd -u 5984 -d /opt/nouveau -g nouveau nouveau # buildkit
# Tue, 23 Jun 2026 23:32:47 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:53 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         openjdk-21-jre-headless      ;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:32:56 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version # buildkit
# Tue, 23 Jun 2026 23:32:56 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Tue, 23 Jun 2026 23:33:02 GMT
RUN set -eux;    apt-get update;    apt-get install -y curl;    export GNUPGHOME="$(mktemp -d)";    curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;    gpg --batch --import keys.asc;    gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;    command -v gpgconf && gpgconf --kill all || :;    rm -rf "$GNUPGHOME";    apt purge -y --autoremove curl;    rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Jun 2026 23:33:02 GMT
RUN . /etc/os-release;    echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ trixie main" |        tee /etc/apt/sources.list.d/couchdb.list >/dev/null # buildkit
# Tue, 23 Jun 2026 23:33:15 GMT
RUN set -eux;     apt-get update;         echo "couchdb-nouveau couchdb-nouveau/enable select false" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive COUCHDB_NOUVEAU_ENABLE=1 apt-get install -y --no-install-recommends couchdb-nouveau=3.5.2.1~trixie;     rm -rf /var/lib/apt/lists/*;     chown -R nouveau:nouveau /opt/nouveau # buildkit
# Tue, 23 Jun 2026 23:33:15 GMT
COPY --chown=nouveau:nouveau nouveau.yaml /opt/nouveau/etc/nouveau.yaml # buildkit
# Tue, 23 Jun 2026 23:33:15 GMT
VOLUME [/opt/nouveau/data]
# Tue, 23 Jun 2026 23:33:15 GMT
EXPOSE map[5987/tcp:{} 5988/tcp:{}]
# Tue, 23 Jun 2026 23:33:15 GMT
CMD ["/usr/bin/java" "-server" "-Djava.awt.headless=true" "-Xmx2g" "-jar" "/opt/nouveau/lib/nouveau-1.0-SNAPSHOT.jar" "server" "/opt/nouveau/etc/nouveau.yaml"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5313ce6db74f98627afe0c7e4d43f8b57a0ad77d4d3184ea9e0d01253abd33c8`  
		Last Modified: Tue, 23 Jun 2026 23:33:30 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40836ca234bd40b8c4295cd5a94a7f4a82f682c8f33844bae255d7a478d7dc4a`  
		Last Modified: Tue, 23 Jun 2026 23:33:31 GMT  
		Size: 7.3 MB (7261179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a9848ec6c2ee307d8714baeec49e7bf5425762816245c9b0fb5f279c422a3f`  
		Last Modified: Tue, 23 Jun 2026 23:33:32 GMT  
		Size: 69.2 MB (69179730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7010cf1c1c6d1a1900757033c5552425409fc6a2ca148b95da9821808d0c7b`  
		Last Modified: Tue, 23 Jun 2026 23:33:30 GMT  
		Size: 390.2 KB (390249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce482bfa8391c85475e9b9f5c31fc168fc5ed90ad518340b7f4d25f8d6fec8b2`  
		Last Modified: Tue, 23 Jun 2026 23:33:31 GMT  
		Size: 347.4 KB (347418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8dc170d66d6619a3baeb573638bde792eb024ff90158a35042dfe10130708ef`  
		Last Modified: Tue, 23 Jun 2026 23:33:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fcb5ef627136ba3bcfdfeb04eaf3befa8df1179de18c09851623e49eb1ee6ca`  
		Last Modified: Tue, 23 Jun 2026 23:33:33 GMT  
		Size: 42.7 MB (42731780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e19d0ccfba4ad18823eb374f84b7eda28d7d3febcf012f3d0a055e344190e2e`  
		Last Modified: Tue, 23 Jun 2026 23:33:33 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchdb:3-nouveau` - unknown; unknown

```console
$ docker pull couchdb@sha256:1a3070bb6674fbd4130b503a1ea4f1b33ef83e3c1f047f52e375976113bd771b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3388017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a85de82f4abfe2b8fb1830a1dff75fcf62b7badf54c28672ddef151f1f9922ea`

```dockerfile
```

-	Layers:
	-	`sha256:7b7e3cf0d0456eb003b663814fc3d531897a1574d956b425fa5151d48d39b3aa`  
		Last Modified: Tue, 23 Jun 2026 23:33:30 GMT  
		Size: 3.4 MB (3363308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b577a1dc55bd252562e26292b066fa2b53cfbb445788988c8f0fdba069317ce`  
		Last Modified: Tue, 23 Jun 2026 23:33:30 GMT  
		Size: 24.7 KB (24709 bytes)  
		MIME: application/vnd.in-toto+json
