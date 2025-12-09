## `clojure:temurin-25-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:e34995bb1d44ebc37af6237efde96a134cf906c5428a9405ab0fc0c6e2484d94
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:829ebde6f91c328066de2e89a3d050a779e87f9f637f226613cb1d81a5b42ede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181457000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca45a031c625111174a6ad0761f39f8391b19849bec5950af48fa66b4da18589`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:56:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:56:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:56:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:56:37 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:56:37 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:56:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:56:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:56:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:56:50 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:56:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a88499d92e58a9f7d74dc939bd949d9c2d87abbbaaec03b5f87553e69d901a53`  
		Last Modified: Mon, 08 Dec 2025 22:17:50 GMT  
		Size: 30.3 MB (30258465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e754549a830c65fa326d4fb213e8b6820fd20b753cea39fb3a9a1c7954f27e`  
		Last Modified: Mon, 08 Dec 2025 23:57:33 GMT  
		Size: 92.0 MB (92045300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db3fba77d79eb16f83e3b8cd0507a0294b75bbe868269ceaf6f328947abf4c4`  
		Last Modified: Mon, 08 Dec 2025 23:57:27 GMT  
		Size: 59.2 MB (59152196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b750250d705079d8842bccc4018e003cceac8f61728507f516cff93e8f9f154`  
		Last Modified: Mon, 08 Dec 2025 23:57:21 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe50fc926e16b52c0cd97e0c79c81f001fdb9c4e8b516a1fcf506cdb91be9ef`  
		Last Modified: Mon, 08 Dec 2025 23:57:20 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:231f0702e4c34b99ec85cd0c0da5ac931d17beb7b3466d039aa7ac297f7cf996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc93faa8f0b5ebe6f10296ec971d6eae76792dbaf940484d2bf88d4b7677a7d`

```dockerfile
```

-	Layers:
	-	`sha256:5540e9f31be6ee343858226f90480212ede01e207b1becc7f820f6a0e16858dc`  
		Last Modified: Tue, 09 Dec 2025 04:45:57 GMT  
		Size: 5.3 MB (5259427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5893c0563f5ee36d59ed11007c7f9bcbad1ee290c65b87f1a2d69a2fc49d4c69`  
		Last Modified: Tue, 09 Dec 2025 04:45:57 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9b31c093ecacecd0d76f0fdd30748c40f42da4c44fc4bdc69e42513b5a6d97fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179089705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bebddb07f452a2f6e6da00b6c92b3ec587abc6ca99202b7c3486bc0bba24177b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Tue, 09 Dec 2025 00:03:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 00:03:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 00:03:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:03:45 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 00:03:45 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 00:03:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 00:03:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 00:03:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 00:03:59 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 00:03:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7d43510e20279c4831f5ca1d424a1d56c6c24251d7c93288a50a066dc7e72bda`  
		Last Modified: Mon, 08 Dec 2025 22:16:06 GMT  
		Size: 28.7 MB (28748482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d314d567ecd528195cf43999c3ad749a96723e437d4c2404818bbaa1bfe83a60`  
		Last Modified: Tue, 09 Dec 2025 00:04:42 GMT  
		Size: 91.1 MB (91052482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1973312a9d0f35e996a1e6c4e6747120f70da7e626fa9a7bd90b7469e864ccc4`  
		Last Modified: Tue, 09 Dec 2025 00:04:38 GMT  
		Size: 59.3 MB (59287701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8100f5af66576b537df24e8d206e270a849199ab9f05fcbe39c642212b66a18`  
		Last Modified: Tue, 09 Dec 2025 00:04:28 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f46ab32e41cf19a7e2c487b52bb9efbd39e471dcac4fc2de1b3c27a3db8246`  
		Last Modified: Tue, 09 Dec 2025 00:04:28 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:795b93f87872ac8d12e0b11427e238bb073055905dd5babfa8b35d62015f04d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a771ef6f9dad3615087614753fd09953c1edbf5b216efcf5a68ed880fca648`

```dockerfile
```

-	Layers:
	-	`sha256:f1833de2ab29bb02b956299a084f9cdc11884d636f5d68b9a0351369714dfac7`  
		Last Modified: Tue, 09 Dec 2025 04:46:02 GMT  
		Size: 5.3 MB (5265180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edb22e85256f6c95f1399deb0c6920cb0a8c6fdce958012e201bb4e2b565ebb3`  
		Last Modified: Tue, 09 Dec 2025 04:46:02 GMT  
		Size: 16.7 KB (16667 bytes)  
		MIME: application/vnd.in-toto+json
