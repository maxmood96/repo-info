## `clojure:temurin-25-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:c3ead9b6cc1cd81068815b22f3f130c08b1013f6aabedd8b135ba1c90ba6e319
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:25ffbf02b2c85eba6fe53222d4ef0f6d0cf3a290faba09458cfe0c8c8623b94e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181457422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b28ca97cdc49493766ad17e74ce3040880c8c635d123b9cc7ccf8e2f4aef9f5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Sat, 08 Nov 2025 18:46:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:46:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:46:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:46:17 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:46:17 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:46:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:46:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:46:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:46:30 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:46:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a0678a9d2bf7948f678158df660cc386347b940718b7434d5ac623850eac14`  
		Last Modified: Sat, 08 Nov 2025 18:47:07 GMT  
		Size: 92.0 MB (92045314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343abca0bb27cd67f14e194bee8c65c9d7e7bfe2dacf04d77d6f54696ecb6394`  
		Last Modified: Sat, 08 Nov 2025 18:47:04 GMT  
		Size: 59.2 MB (59152467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a174bc420c08f69d84281529dacc04f2b2b6f334a3f535d0c0d6353f083cf38`  
		Last Modified: Sat, 08 Nov 2025 18:46:57 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9396970872be8c5f534c4163ebc9ca9f9a761b3dfafbc3de0f305989d577dd87`  
		Last Modified: Sat, 08 Nov 2025 18:46:57 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dfe2b4f8615346c91c4e77061c5bfacba36802e5146f1d327f8daac9de4518a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:964f6a115f02cd04b2abc083d556acd8cd1de959fda48d4831c27937c640dca0`

```dockerfile
```

-	Layers:
	-	`sha256:e971a09bd3a24442e0aebf37b76913731949fe46dcdebd8cbc96ecd5f325451e`  
		Last Modified: Sat, 08 Nov 2025 22:51:25 GMT  
		Size: 5.3 MB (5259427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cfa27d2a0a599715583761e939ef9481e0b079256bd5a942511882a15c9f909`  
		Last Modified: Sat, 08 Nov 2025 22:51:26 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ddcea7a6d0796a7629d3890c784b07451e8dfd8cd887d3d04856a8bdd7f3ef39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179089813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d70a62af088c1590a9c2c16eb895d914b4de3faf06b607f97069142cc74b56e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Sat, 08 Nov 2025 18:45:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:45:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:45:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:45:54 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:45:54 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:46:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:46:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:46:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:46:08 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:46:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cacfb62ed498012b9b3b6853ac92aeb76489ba2ca3d9c924116e26f7ec99df9`  
		Last Modified: Sat, 08 Nov 2025 18:46:58 GMT  
		Size: 91.1 MB (91052530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c792bbe941a22838b4b6789e1fa4141f584ee1062d2c6589bc3d06a729f945`  
		Last Modified: Sat, 08 Nov 2025 18:46:56 GMT  
		Size: 59.3 MB (59287688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91bcf95ed1dd6e83979f71bb5c98597519be029016b4b27a7b44ed1a4b8643a`  
		Last Modified: Sat, 08 Nov 2025 18:46:53 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb888c39d9788dbefe293327d26b4fbad12092f1d0adbe7399254ea5563560ef`  
		Last Modified: Sat, 08 Nov 2025 18:46:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:98fb20a9092e8ca737351fccc71523f1ac78a159d994c677322d48562d84584a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f798bbc67121623f60bd687ed89ff9440365ee859d95d6f24fdcf00c571e0b`

```dockerfile
```

-	Layers:
	-	`sha256:8386b7cd8adbcb8c16fb20db190e9a6c492b8efc813f91d36591a5793f4dbed8`  
		Last Modified: Sat, 08 Nov 2025 22:51:48 GMT  
		Size: 5.3 MB (5265180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adebd22854f9487859a76fb1b178c3e036d1b4c4211cb3a23dd8f9b651dcbc0b`  
		Last Modified: Sat, 08 Nov 2025 22:51:48 GMT  
		Size: 16.7 KB (16667 bytes)  
		MIME: application/vnd.in-toto+json
