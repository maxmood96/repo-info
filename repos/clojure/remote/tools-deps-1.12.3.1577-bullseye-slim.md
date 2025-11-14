## `clojure:tools-deps-1.12.3.1577-bullseye-slim`

```console
$ docker pull clojure@sha256:105c7202741a9b94832ee79c076907a853afafa6faf22e9ee09593c4e40970f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.3.1577-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0d70f2f59d2118650495bc2556871ae2d08187c7d4bb6f0fedc0009be8d31549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181457298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afc2c250e0077371d4e2d2c49df8e78fa8d0d04a63ff230bace6092a9d07b2c2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Fri, 14 Nov 2025 00:56:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:56:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:56:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:56:11 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:56:11 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:56:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:56:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:56:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:56:24 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:56:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8db9b8196cd45153138c314c5990d28e021f0616ba148748e435f03b140105d`  
		Last Modified: Fri, 14 Nov 2025 00:57:04 GMT  
		Size: 92.0 MB (92045320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1dd10b61401d1341e03d65ba87c660c3cec89fbd60edfff0b6c9335d235a980`  
		Last Modified: Fri, 14 Nov 2025 00:56:56 GMT  
		Size: 59.2 MB (59152341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0310ee6ef0fa6cf5cfb8dfb8507cbfbc7567648d8030189a215b6ad48b1ca2`  
		Last Modified: Fri, 14 Nov 2025 00:56:48 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5e615b1834bad5bdc11caa8c8593b1005306e52d00d1a8342e7c6cd3ab2d4d`  
		Last Modified: Fri, 14 Nov 2025 00:56:48 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2e80d53e82f0e1a3e36ca6de5f2a8419e26e884d7481bc4b6a7fb66aa99d95df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8631030a61e857d75d9e202776dc3ebc5bae83c7c2cb0ec15d3036d66f62f339`

```dockerfile
```

-	Layers:
	-	`sha256:d04db424f46a229289b3cbb322d982262ac71fa09fb5163dde383b5e96a6584d`  
		Last Modified: Fri, 14 Nov 2025 01:46:11 GMT  
		Size: 5.3 MB (5259427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54d82a878c511434046577161691fa6a3be3d4a766b940a19f3ea56c4183e166`  
		Last Modified: Fri, 14 Nov 2025 01:46:12 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.3.1577-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5425c36fd790d3c9ba93c142c06d8aa7edc32345466f3d0cbbc4e0f3807da396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179089732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d23ea0ef0dff4b6001d4b5b6ba014c4e69753b1d3503559ebf8557c43a630bd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Fri, 14 Nov 2025 00:59:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:59:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:59:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:59:00 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:59:00 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:59:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:59:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:59:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:59:13 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:59:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0abd3340f62c971a401a024de9c4bc60d2069af66dadcdcdfd62201ac53bb66f`  
		Last Modified: Fri, 14 Nov 2025 00:59:52 GMT  
		Size: 91.1 MB (91052521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc38b4f18b763ada954cbc3620e1152a00a7d0edceeaef035df54bea08fadb37`  
		Last Modified: Fri, 14 Nov 2025 00:59:51 GMT  
		Size: 59.3 MB (59287616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1c83f9b888c8663d8784ab747f94f0d610cf04b2c4d53d60df7e29837a241b`  
		Last Modified: Fri, 14 Nov 2025 00:59:42 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca4638d9cda71a224e472fff9395a7eea36316331cc057609a56450f6e9878d`  
		Last Modified: Fri, 14 Nov 2025 00:59:41 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5724320770e79f4de1f447a590228c602f8d064cf8cfa330362e9c7ff7999d16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56e02c024a4c90f7467c6e4dd0be2cd60d0ca9f9b97dfe75970ba891730fac8`

```dockerfile
```

-	Layers:
	-	`sha256:b16aa5f2bd106d0366196c22df4f74ad97bda2dbbad8842849b4b8dfaa19f6f2`  
		Last Modified: Fri, 14 Nov 2025 01:46:17 GMT  
		Size: 5.3 MB (5265180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d702962b7df762c9caaf2ff27885f2e4c0147fb64a7dfc51d47bd45a8a6021d`  
		Last Modified: Fri, 14 Nov 2025 01:46:18 GMT  
		Size: 16.7 KB (16667 bytes)  
		MIME: application/vnd.in-toto+json
