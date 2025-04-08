## `clojure:temurin-8-bookworm`

```console
$ docker pull clojure@sha256:508e061c94dc29137bacefdc9e2f3e8d1031073de96ec6eab01521199cff6499
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:c62e51db95015c831c123a7670140931a2707a2bdaf285bcb7919ffa9e1c05d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184205854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a366ea6ab00a958dd04013b01b6c1a923a03845b4ae12348c12a84bb42a1eb19`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c287d3f7330c1ddf05d2acfe79d2a3dfd3ad36ad04df90754bc4c10ed7c350`  
		Last Modified: Tue, 08 Apr 2025 01:49:01 GMT  
		Size: 54.7 MB (54721234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331513ce85fabcb5aa02b1637908eb2d30dd8a2e5da2c6306d1f5d34e40ebdd1`  
		Last Modified: Tue, 08 Apr 2025 01:49:01 GMT  
		Size: 81.0 MB (80993433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19799096d863bcff71297c2649acce02dcdaed75f2bb3a613f4653603e12636`  
		Last Modified: Tue, 08 Apr 2025 01:48:59 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:dc887f58ca81fd824ba3ca6d22ff73941636dde628ffcc0c273e4feb0aadd352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7308323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc2901503d6703cccf7c6895941b1d5c60ff314a5fb050d7f943505adf50bbd2`

```dockerfile
```

-	Layers:
	-	`sha256:0fcdb22c7bf29ed33ff26302241867175d8eef858be357ec80b2120d14509df2`  
		Last Modified: Tue, 08 Apr 2025 01:48:59 GMT  
		Size: 7.3 MB (7294086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09dc24838fdaeaccbdfd6795860e88fba3751239099995116953bff511c4f3cd`  
		Last Modified: Tue, 08 Apr 2025 01:48:59 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c409b63515b739ef05927579f2eb8073218c8fa9c5cf4f350946229eb43d6c8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (182970930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc3468f5e72a3aaad4d72b195410e8ad3a7e4fc11c4ec6208581b8329840ae8`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71e06352f37c6d0a072e8047fbee028b939a5c468a25e662d78194bd7f4e0cc`  
		Last Modified: Tue, 18 Mar 2025 00:16:09 GMT  
		Size: 53.8 MB (53822757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf58d16ab08cf851492828988b0961f64b20ed072b9d326ed3bd38ac732df8e`  
		Last Modified: Tue, 18 Mar 2025 00:16:10 GMT  
		Size: 80.8 MB (80842675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566233326d937ad79cc6669ee636d4e23fb0352ab6507a9fff19f6e5af66ab22`  
		Last Modified: Tue, 18 Mar 2025 00:16:07 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:34056a9c89e8d2f941f510a45fdfdd6f3a06f51452b2c8265f757bd515c061cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7313534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a6be3ee9eccde447355b76c7ffb9ff223ba00bac76c236a7f63f982b1c87eb`

```dockerfile
```

-	Layers:
	-	`sha256:fef98b71a502003a6b2bffce97409e2789520473e89342a43c7b40fa9ae8d873`  
		Last Modified: Tue, 18 Mar 2025 00:16:08 GMT  
		Size: 7.3 MB (7299179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6261f97b26a2afbbc653376b7ed646ffe361a07e21f00664e8bf566b177b9d5d`  
		Last Modified: Tue, 18 Mar 2025 00:16:07 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json
