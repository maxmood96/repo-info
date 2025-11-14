## `clojure:temurin-21-tools-deps-1.12.3.1577-bullseye-slim`

```console
$ docker pull clojure@sha256:93d8b879db1b4f9e3906644864d708574f0c8909e07209d5883448766e3aeb3f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.3.1577-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:51b54878bcb466f0c4d149cd24888ed58b22dbc7a272a28a5f198056c930288b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247237721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83f3ae50c080c47e20d482ebed5ca9ba0a1d0fd41a13e959f8818fe725b46d94`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Fri, 14 Nov 2025 00:54:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:54:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:54:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:54:37 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:54:37 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:54:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:54:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:54:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:54:50 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:54:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66dfe5240b377be5a4986f529c3b1a22b70a6cc5c5dcc0d3f1413233e8323ce9`  
		Last Modified: Fri, 14 Nov 2025 07:52:16 GMT  
		Size: 157.8 MB (157825975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e4d8c0b8b7e2251066de20a855a98663635cf1e2ab24d7fccefee47d817866`  
		Last Modified: Fri, 14 Nov 2025 00:55:30 GMT  
		Size: 59.2 MB (59152108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6dedabb7b350c2ee2fbaeb6ef7a89ccbedfef2b6c7e5ffc586526d6d7869ffe`  
		Last Modified: Fri, 14 Nov 2025 00:55:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a924a99cdbc127db990d0e2ff42362e20de5197867c109f289cb65167e07dbf1`  
		Last Modified: Fri, 14 Nov 2025 00:55:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b2504a4a617cf9bae7b0ab466d62019f393812a61e93ded7c229abcdd6233e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5327007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:867f593cc5d79228588b2700ab3ada388eb3f0662d2f475077e34564f105c887`

```dockerfile
```

-	Layers:
	-	`sha256:4fabd8b553e7c36a2524caa49decbe1c57648b3b08272c6edbb7240b5555808c`  
		Last Modified: Fri, 14 Nov 2025 04:38:58 GMT  
		Size: 5.3 MB (5311171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b2a01673e0819c08f7e8ebbcfe1606fdc1e59474fbf93992323c1670eda38b7`  
		Last Modified: Fri, 14 Nov 2025 04:38:59 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.3.1577-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9aa82fec7c5eed0d53c154a75aff0cd31b18972eb0e6022c8349fd17893d1fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244144875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5850e1f9edf208ae4c02472b5d7cf80405d654833e39b98522f78a5239ab66b1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Fri, 14 Nov 2025 00:56:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:56:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:56:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:56:57 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:56:57 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:57:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:57:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:57:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:57:10 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:57:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4140d63e32a86ccf80b3cf9477bf6c0ec75970c36930b3731fe6ec17cb2a9e`  
		Last Modified: Fri, 14 Nov 2025 00:57:35 GMT  
		Size: 156.1 MB (156107645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291592bb08a5ba53b30a5ab7f247fae4a98e76084744d9711f9f73c62f4d92a3`  
		Last Modified: Fri, 14 Nov 2025 00:57:47 GMT  
		Size: 59.3 MB (59287634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b21a9685e627b05fa2834ef377aa0a7b7b7955eef6cdcdd1efbe974cbe46e53f`  
		Last Modified: Fri, 14 Nov 2025 00:57:41 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60dd821542b03ade19e128959a3405eeff6d65bafd295a2f501ffc2ff8dd6f4`  
		Last Modified: Fri, 14 Nov 2025 00:57:41 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d77ffb4499b0de0e7067413cde0bad48e6666d97fc45e9e55118b8f8f7ba6f8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5332857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8aeeaa5050207a37df66e673be16a9a8f3feaa5188f90a02fe1174e14423997`

```dockerfile
```

-	Layers:
	-	`sha256:6fb924f892c910891fc4c9db800d079b04ce5ca0bf20fd1d87d1a4963b31d566`  
		Last Modified: Fri, 14 Nov 2025 04:39:03 GMT  
		Size: 5.3 MB (5316903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86d857bbc52a0adb491fa97575c0e6b7f50fbccfe56a57febd539c6ad3500f4f`  
		Last Modified: Fri, 14 Nov 2025 04:39:04 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json
