## `clojure:temurin-21-tools-deps-1.12.2.1565-bullseye`

```console
$ docker pull clojure@sha256:26cb7b6b1e582278a9a9ffd0a214cd3fd57ae8682d2830ca73ab40e98d743f5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.2.1565-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e390a466c57d389bfa0da1a5a8f108e84afce71d317c2b93742909c65edee3ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 MB (281118053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a5fdd7016449560259da3f05b1d15a386ecb65524dd9a6c13d894322c1a456`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:035115815e46101f9c9956e02e706f2f3ec8748e2b415f0d232b51eb76a6a779`  
		Last Modified: Mon, 08 Sep 2025 21:12:56 GMT  
		Size: 53.8 MB (53755396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edea7e4379bf1f4812c50007516e54498a9b0599f0d53839461759cf0c78ef91`  
		Last Modified: Tue, 16 Sep 2025 07:18:04 GMT  
		Size: 157.8 MB (157804768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33200ba7054950f8a7f876a3fd424adbf9d4d94cb6662bca2136d5ebe0edd91a`  
		Last Modified: Tue, 16 Sep 2025 00:33:43 GMT  
		Size: 69.6 MB (69556846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814ed68377408b6245acee75e8f8f1526f5fe64daff8afa5c5555b452a1f7bdd`  
		Last Modified: Tue, 16 Sep 2025 00:15:11 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325e953a3227221a0e51aa1c9ad46c7808e793ea52b188a37bcf4206d5745997`  
		Last Modified: Tue, 16 Sep 2025 00:15:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.2.1565-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:ec50e1278afd74660ae97388335b73d938bc38ad94d90a57019cadb01b08c76e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7415941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ec1e28264824c8263880e70d932aa0e9f6701cd1a9b084deeab02b56aa83f7`

```dockerfile
```

-	Layers:
	-	`sha256:8981938dfa83855e284fa14c3f4e40342afd7e47ff9f41b74f7d72b0d5ed8216`  
		Last Modified: Tue, 16 Sep 2025 00:42:03 GMT  
		Size: 7.4 MB (7399445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7259423ad98b42c11ec24da7ae1a2ca6f6b15f3747b381f7b19f94e6c33d291`  
		Last Modified: Tue, 16 Sep 2025 00:42:04 GMT  
		Size: 16.5 KB (16496 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.2.1565-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fa2bcafa818db2d523f19f99ca31ca33804e285a68e9c26c6d458142ff64cd10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.0 MB (278014702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a67daf20424efa57bc3c276dac551272892edac1d45c0bf3b810500bbc06df9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7df02cb4a974a4e8a9eb65ffcff7274f9dca341d29aaa763294c42e49805ca19`  
		Last Modified: Mon, 08 Sep 2025 21:15:41 GMT  
		Size: 52.2 MB (52248370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf000741baedf395d0370284460e792bd25125e34bb0c576951a0967c8dc66c`  
		Last Modified: Tue, 16 Sep 2025 07:17:57 GMT  
		Size: 156.1 MB (156081218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd44c44dea9ff41b07f7cb4736ab2a93f3cd624a53caf496421e5f8dab093299`  
		Last Modified: Tue, 16 Sep 2025 00:19:42 GMT  
		Size: 69.7 MB (69684073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2a11169bb15d4465dcd126b58de3ce8d6cff02ab7cd9454044bd19ab0b3a40`  
		Last Modified: Tue, 16 Sep 2025 00:18:16 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16974d40fdf9fd19acc24528bfdfd88ab011bd85d63da1fb71e79abdb67e742f`  
		Last Modified: Tue, 16 Sep 2025 00:18:16 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.2.1565-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2c8a2c8e3f25516c5fb1c4288f8c9f44973c849cb658c88191d98639c64d01a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7421207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a085c6a723864a4c0cc06682105ace89a157a59c3a49a93740f6f32776fe122`

```dockerfile
```

-	Layers:
	-	`sha256:771cbefa1a50a1a1029e17655b4cc15dbaed6ab69f8bc2d3eead8e03590cea03`  
		Last Modified: Tue, 16 Sep 2025 00:42:10 GMT  
		Size: 7.4 MB (7404568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6e184d058d781d317587da33a8ecfe17663a8be39a9345a327f77b1dcbda174`  
		Last Modified: Tue, 16 Sep 2025 00:42:11 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json
