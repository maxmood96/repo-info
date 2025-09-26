## `clojure:temurin-25-bullseye-slim`

```console
$ docker pull clojure@sha256:5069e6de3fcdae8e5684af53ba370ea8deb1ceba36c13726182435624ac1d3d3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9f88620dd6f7c057c79e16fb736f2a5f9b8d4317a39eb52fe93c4381cdcdb038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181445353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014614b18e4d2856eddaa689add16b0ad58125bc730bcceee35bb0a1ad8f1026`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:456a3213e1b1f193dc759cd05f6f8422428b8c4bd45ef40fbf41ba43bdce8570`  
		Last Modified: Mon, 08 Sep 2025 21:12:48 GMT  
		Size: 30.3 MB (30256068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8fa0043b5d4c32e50b323069e2bfce3c4db656a253cf0c766652b0aee102a2`  
		Last Modified: Fri, 26 Sep 2025 17:59:31 GMT  
		Size: 92.0 MB (92036038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7919edc9f0298805d74159959c2d719ac16e1ad9b90ac86a882dc344cd55ab`  
		Last Modified: Fri, 26 Sep 2025 17:59:27 GMT  
		Size: 59.2 MB (59152206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8dcf4efd5e5f9c9eb88233128a77e220bc38d5c9bed4304238728655ad8cd5`  
		Last Modified: Fri, 26 Sep 2025 17:59:21 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bff6aaafe93df4d1cd8906f12e4dc08eb4017e68883d7a95625156a8b7b6554`  
		Last Modified: Fri, 26 Sep 2025 17:59:21 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:283bc8ae80bfcb30e6766678744c027dc32de943491f1acbf9c8163e984ac105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656daed9b18a9bca074ec5f7992ef8500877e8d6531c38a5e18f265788f3e4cb`

```dockerfile
```

-	Layers:
	-	`sha256:f36bd1e2f2608bb6ef090bc81e25888235e132f9e4740027fb78183657178114`  
		Last Modified: Fri, 26 Sep 2025 18:44:06 GMT  
		Size: 5.3 MB (5259413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b20836cbcf0438b6a92428a019393970b68ca1fe88e34a4b7390c72f92b362c5`  
		Last Modified: Fri, 26 Sep 2025 18:44:07 GMT  
		Size: 16.6 KB (16568 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bca2fa77c1be23d24f87e7c55b34bf0c6dd4d7ffef18ddfb9bf6f2a808f1b21e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179082910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986aa85d20964b79967d11e9befd76a8083b32461708e8de9c5047484029b408`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8568e9af3ab25a29d98aac9a07896467a19253e72e5be0cf09cd3982ac4444d0`  
		Last Modified: Mon, 08 Sep 2025 21:15:52 GMT  
		Size: 28.8 MB (28750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8512b4d19483aff21cf861d6f0d787b18e6372c56144a87d5cf28fc22e3e95`  
		Last Modified: Fri, 26 Sep 2025 17:57:11 GMT  
		Size: 91.0 MB (91045231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ce619ab4f3ddb1cf7005731fc7f67cdda15bc18c1468d34891e1cf275cbc7c`  
		Last Modified: Fri, 26 Sep 2025 17:57:11 GMT  
		Size: 59.3 MB (59286181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a963c81ea1a424a8b794397f830df3c96abc0983077a261a9acf623033d6ce`  
		Last Modified: Fri, 26 Sep 2025 17:56:59 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb12b37b5f1f02777a785af88652d11c2aab5d25f0b542cf5d4b6af2f206c41`  
		Last Modified: Fri, 26 Sep 2025 17:56:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1a00d2a0932c9e990c62086fc41d27ea853258c22b5b6faa904512f294806b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:559dafbdc567374fb6f3e07f8d2003c7f169aa6b8604473a0b608f849ef54444`

```dockerfile
```

-	Layers:
	-	`sha256:4d0ff9cfae2efbe5f850d20cc6720947adab736906be982a6611abc8afb7f1cb`  
		Last Modified: Fri, 26 Sep 2025 18:44:12 GMT  
		Size: 5.3 MB (5265166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5130dc6120c454f9daace4a46ef0a135177547e4238b9d02c45c8130eac7a18a`  
		Last Modified: Fri, 26 Sep 2025 18:44:13 GMT  
		Size: 16.7 KB (16710 bytes)  
		MIME: application/vnd.in-toto+json
