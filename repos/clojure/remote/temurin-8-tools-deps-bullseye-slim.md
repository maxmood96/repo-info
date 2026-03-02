## `clojure:temurin-8-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:d8374f5091c9fa6b57f3d1438edf8f95aac4d0a21baca01209b0e3a4b66a96bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:bebba8ee6bfe2dc3e7afc0b6710a21bd3c3a7d69d7d9ba28e1bd96306793b47b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144605908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c33286ed5861007aec821a521433d7440201dc798c8bbcf0ba2c7669526dc2e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Mon, 02 Mar 2026 19:45:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:45:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:45:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:45:32 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:45:32 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:45:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:45:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:45:45 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:34f0642d22440b5813561cd4375937013bfb556bec8ff3b0e208699b786282a7`  
		Last Modified: Tue, 24 Feb 2026 18:43:06 GMT  
		Size: 30.3 MB (30258379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e7f4251bc52badde0574dd41c4f850ee02fa986cccdfe9c882e3e4eabf5b69`  
		Last Modified: Mon, 02 Mar 2026 19:46:00 GMT  
		Size: 55.2 MB (55170068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb5a960956880d112393c24d2400c228fc89a24364192001e49aab92ae5e4aa`  
		Last Modified: Mon, 02 Mar 2026 19:46:00 GMT  
		Size: 59.2 MB (59176815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f38e1fbca83c2591e1bfe4ed4663d47938b1cf89208d205004555d931766795`  
		Last Modified: Mon, 02 Mar 2026 19:45:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:30d25a7306a168cce9eed18e3f26733f01401ae945d76d6c555239e3cc6c30a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5456912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e55aeabfb24eaf4c88906dd947ed34ce2d3124951cb392911085d5b2f9880f35`

```dockerfile
```

-	Layers:
	-	`sha256:58c836d72ab82ed279a2574acd371653bd0923ec07bb381711eff1519ebb9e4d`  
		Last Modified: Mon, 02 Mar 2026 19:45:58 GMT  
		Size: 5.4 MB (5442664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3686397269ebcdf506f56ac3e8df6da660a6a2fba713cc9538bf15a74bd8e85f`  
		Last Modified: Mon, 02 Mar 2026 19:45:58 GMT  
		Size: 14.2 KB (14248 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cf790e5666ce657070f4c8d90d367c0289a05a5001cc582d0e69d5c700a1bb09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142313931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6e661da4e8ea6d2c90759e70eb16d0feced510f0b0988bad6853f62bb295111`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Mon, 02 Mar 2026 19:45:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:45:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:45:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:45:40 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:45:40 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:45:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:45:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:45:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:018c0693c4a2532e5636d6115333db6d882da8f33f1f40cb3e88dbe62da21aac`  
		Last Modified: Tue, 24 Feb 2026 18:42:36 GMT  
		Size: 28.7 MB (28744470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1332c829da2b9aaeb88f5392c0ee9c6f6fb0eea0cf50c57bf366cdc5c22e7599`  
		Last Modified: Mon, 02 Mar 2026 19:46:10 GMT  
		Size: 54.3 MB (54251614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce88c9ceb9a0615397e1475b0de63b2e796d4c22ce74a260493c9bc71b201386`  
		Last Modified: Mon, 02 Mar 2026 19:46:10 GMT  
		Size: 59.3 MB (59317200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aedb7bd1741a5f3329d51cecb03fdd9af68d3850c0e8138c104814a15e348f96`  
		Last Modified: Mon, 02 Mar 2026 19:46:07 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5c12ff20f55dd65b6757e887df8e2b807f0e5d9a2edb9c8a67c53f8bd24bc4c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5463462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1065ad8946d57be32aced1d456a236c70184d2a0acdda5e6d2fc34e89b999c3c`

```dockerfile
```

-	Layers:
	-	`sha256:f53833ae7d58394aa37abb457568cce95fc0cadf5f490222e3bc949370b509c5`  
		Last Modified: Mon, 02 Mar 2026 19:46:07 GMT  
		Size: 5.4 MB (5449096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b25ead6481f33efb7fc1e359d5080768c2f7cff7fb840a245a9083b6e979d440`  
		Last Modified: Mon, 02 Mar 2026 19:46:07 GMT  
		Size: 14.4 KB (14366 bytes)  
		MIME: application/vnd.in-toto+json
