## `clojure:temurin-11-tools-deps-1.12.4.1612-bullseye-slim`

```console
$ docker pull clojure@sha256:c6baec0a655808cab0b7478e2db5488571b9ce84615dcd853891053dfe948e38
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.4.1612-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2a3afbab1f47f1de8f44c7fcb2a60a9a2fca21f992204146acba7fd3c2a04934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235249031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7736d61571897002ced1b247b68689dc46137fe95d26ed02a79e46e36c5140`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Wed, 04 Mar 2026 17:49:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:49:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:49:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:49:35 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:49:35 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:49:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:49:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:49:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:34f0642d22440b5813561cd4375937013bfb556bec8ff3b0e208699b786282a7`  
		Last Modified: Tue, 24 Feb 2026 18:43:06 GMT  
		Size: 30.3 MB (30258379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f2983c96e75a326445531fb5c5921f85ef3b9b67c0ad90879aad6d24358499`  
		Last Modified: Wed, 04 Mar 2026 17:50:10 GMT  
		Size: 145.8 MB (145806756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b80d4e10e759a2d842885d242f097fab88c6890d355345aa297d8ebf7485f3`  
		Last Modified: Wed, 04 Mar 2026 17:50:08 GMT  
		Size: 59.2 MB (59183250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a61e22fc91c0abe39661468664ed3f161ed2dbb85f796737262ddef9b55dc5`  
		Last Modified: Wed, 04 Mar 2026 17:50:05 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1612-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0d3f91807c860eaec33fd23c1d862d39a51abcfb90b07800362965a0c500a8de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5356085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d737f01595441e8e133641978ab8de705338e2121aae9b25991b42b2acccfc10`

```dockerfile
```

-	Layers:
	-	`sha256:94a0e6e91fd547c67605596b4c5b1d4fa268acb9132ff1d3767303fd65de4c17`  
		Last Modified: Wed, 04 Mar 2026 17:50:05 GMT  
		Size: 5.3 MB (5341818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88221d3e65460e69e99daabade29bea3f49440d4004a7ae727673ee95e88e1f7`  
		Last Modified: Wed, 04 Mar 2026 17:50:05 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1612-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:355ecea34acd863b22e5ff8122d5c1d87cee612250493ca599f7099700ad5a41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230570064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6db91c77bb0d63d6d2ebaff1eaf38f17412b205001672226bb222036b2979db`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Wed, 04 Mar 2026 17:48:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:48:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:48:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:48:59 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:48:59 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:49:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:49:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:49:13 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:018c0693c4a2532e5636d6115333db6d882da8f33f1f40cb3e88dbe62da21aac`  
		Last Modified: Tue, 24 Feb 2026 18:42:36 GMT  
		Size: 28.7 MB (28744470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cfaf7cf19474dee8f500bff71610ab91bdcbdc84f708cdf6fdd2d7ea6bd8bb`  
		Last Modified: Wed, 04 Mar 2026 17:49:34 GMT  
		Size: 142.5 MB (142501423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3a987e260ce2fd55e94fc2d66b8333d40cee080c83adad7491a5eaa7038e66`  
		Last Modified: Wed, 04 Mar 2026 17:49:32 GMT  
		Size: 59.3 MB (59323526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b7aa07cb7a2dea39bc8bde255d6696781035a5190455b80283c284ca676f6b`  
		Last Modified: Wed, 04 Mar 2026 17:49:30 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1612-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:100aa22d592a8aad95814c29fd0c23d2e59c317a01d2aa06c82fd6c36c84b051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5362553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a4be2d8cd77c75ad1d0cf34a343dfe9f910ccf3a633264d944d88ccc1f1664`

```dockerfile
```

-	Layers:
	-	`sha256:449fc427a23b5bd6722046a2c24720e25f35a168760e58e971e76c5e90932c2e`  
		Last Modified: Wed, 04 Mar 2026 17:49:31 GMT  
		Size: 5.3 MB (5348168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfdcc466ba3d7cee7410de9e1c774f40853701d8609560474c34b53b5b46bd46`  
		Last Modified: Wed, 04 Mar 2026 17:49:30 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json
