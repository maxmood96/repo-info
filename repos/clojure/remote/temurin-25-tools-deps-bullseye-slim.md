## `clojure:temurin-25-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:9b3d96aa7982a65243534731239cd7b3e31ecf45fcdf4b0c276b73e28a569e22
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:278eb67c0a682e339544e26688219c2039e52a52258676d7e425849aec361bd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181447730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53f1219097a296a1166d3e47cc2ee285937b6775b2fd2f6e5a1c12f59d8a79ae`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:56:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:56:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:56:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:56:51 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:56:51 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:57:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:57:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:57:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:57:04 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:57:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42da1f79fc35e33600a4a4efe2e38c90731177d29ba94f9c477f56d05c3e7130`  
		Last Modified: Tue, 04 Nov 2025 00:57:58 GMT  
		Size: 92.0 MB (92036031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec49ad255370921be0fb04d7f7a3e848dce900fd6dc0908649a2c96bfb46d73`  
		Last Modified: Tue, 04 Nov 2025 00:57:48 GMT  
		Size: 59.2 MB (59152064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34fc453e52628269b30381a3b6fed2e81b4aafc8e3d79f223bc18422fa0bbf48`  
		Last Modified: Tue, 04 Nov 2025 00:57:36 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b99163d171af119b2d291ff6175d6f562d9d4fc6176f30a9b9b1dd5cd7c6ef6`  
		Last Modified: Tue, 04 Nov 2025 00:57:36 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cd5d807d3360b3af2dbb5f2fba1aae8323574cbe4edad8f017c36ca34e783482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30db9ad9fbf86ba7c6dd42e16624a372e880ef278aa299ae2e7a1cf43dffc42b`

```dockerfile
```

-	Layers:
	-	`sha256:6d3da04b30bc795ae7a26da8fc803c1bc520c47f7e3b46888f8de473bbdb8b89`  
		Last Modified: Tue, 04 Nov 2025 10:45:46 GMT  
		Size: 5.3 MB (5259413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bbca111707ff555b7b3eb00941f637b73b479643545601cc01ea90dc3cccc5b`  
		Last Modified: Tue, 04 Nov 2025 10:45:47 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bc44e6f2efe0af280f41e51ae1ef53724fa665208d100aaaea7646668c17a6f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179082567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b78fe5f4e09d6bb41f2fce77c426f1835b0fea604d82ba8402635ed0c2a69bd3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:57:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:57:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:57:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:57:25 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:57:25 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:57:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:57:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:57:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:57:38 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:57:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df12a77c1b467fa2b83424bdd07b0a4b24a9866667b5169e5a038a69528c584`  
		Last Modified: Tue, 04 Nov 2025 00:58:16 GMT  
		Size: 91.0 MB (91045237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dec18d7e0963507dbada221f8c66ed3f6978850f243d97db2d9a9d6aa7520a8`  
		Last Modified: Tue, 04 Nov 2025 00:58:11 GMT  
		Size: 59.3 MB (59287737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e4a8a913e84f46ec73864fdaf65acd0d84f6941b37220c81bea5b6bbd38046`  
		Last Modified: Tue, 04 Nov 2025 00:58:05 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27df1b3cbfec55f51fc2f1dfc971d8d4fe0c66e5e3cb8244a96fa4ac875c46e3`  
		Last Modified: Tue, 04 Nov 2025 00:58:05 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c7cd17d150cfefedc784403552b3082caf5733f233e69dc1e57d1055b0f138c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce9e04356797c70ef43f2de94b3c3128eccd814a3039ab2697fe0ace4ea200a8`

```dockerfile
```

-	Layers:
	-	`sha256:a0111294b86ebd3b266c09c13f0e02795870883273d5ab9fc3c02e6182eba69e`  
		Last Modified: Tue, 04 Nov 2025 10:45:52 GMT  
		Size: 5.3 MB (5265166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6c70997ec6d78db97a23b08ee12d03d659932fc8f9368d9a65cbd008a08826f`  
		Last Modified: Tue, 04 Nov 2025 10:45:53 GMT  
		Size: 16.7 KB (16667 bytes)  
		MIME: application/vnd.in-toto+json
