## `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye-slim`

```console
$ docker pull clojure@sha256:90cc88c21bc07df184a6408a67ba78fb1516eaa6cd0c256e1476afda84170688
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:07d4919375a71e17b44f0a9190f956bd51139be7e465540cfbbbe69b2d3b9fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234886798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ec0aec61531ed6b92db9c8e5020c0e6f96725505f365ebf3abb8fbfb5c26f53`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
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
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8847c5ed550c64ba92291b75ae1d442d0ee4921c3860ed2e925e16a0eb435c83`  
		Last Modified: Wed, 23 Apr 2025 17:15:35 GMT  
		Size: 145.6 MB (145635872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd9fd84548478ec69833ef8ce6d6da056f634fa507acd5aa4719e4211a31bc9`  
		Last Modified: Wed, 23 Apr 2025 17:15:33 GMT  
		Size: 59.0 MB (58992859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd411524c8d912d1e6fdaeb6e52e04483e460300332eb505f4c684c0b131c54`  
		Last Modified: Wed, 23 Apr 2025 17:15:32 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e94e8716cd205b5319fe33a55187882f2f5bcb7442aa7f82309ac738fc62fc68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5153464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:725efcfd708ce3e58a23de4501ae7cb88e5b29d4ff7bc8b04893fef79cb29ed7`

```dockerfile
```

-	Layers:
	-	`sha256:a09c69e6d4ac681e5bab268fceccc22caa4c41de57bcc94238af4bccd4e8171b`  
		Last Modified: Wed, 23 Apr 2025 17:15:32 GMT  
		Size: 5.1 MB (5139154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ba40bcf1e31f725a84d233168e098ae138c9680b39d46e399fdeb4c866bda96`  
		Last Modified: Wed, 23 Apr 2025 17:15:32 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e926bee436a6a720e35876d5cf9dbc094b5b98e64b0411dd791effe52dd93f68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230299492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd54f6c1951f353b24d827dea1210b098d9bc6cdd4df44c90f8da543a565fa3`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
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
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad1d14317d3a031e80061d38befa6227f9338c259b60edd4197d1dc2a8a7f1d`  
		Last Modified: Wed, 23 Apr 2025 18:14:17 GMT  
		Size: 142.4 MB (142422063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2a788faff615f6cb36adb4080398617c5f9684ba6090cc8cf3a6a9f51bc326`  
		Last Modified: Wed, 23 Apr 2025 19:43:09 GMT  
		Size: 59.1 MB (59127283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c629dea2a1e197fc82aed81f71a209a926b7b3407773f0a2e81dbb52156f4b3`  
		Last Modified: Wed, 23 Apr 2025 19:43:07 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5b545165f8ba14c9388710fdcb686f4d7e729cbcad5189c0a74c13081012f49e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5159932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4596d2544fff7c2113b2092728901afe81e1ce0df859334d2252e80b10f7a220`

```dockerfile
```

-	Layers:
	-	`sha256:f5d221947acae98e927fbda9f9e5c261ff7347eb189e179278793bfd30720511`  
		Last Modified: Wed, 23 Apr 2025 19:43:07 GMT  
		Size: 5.1 MB (5145504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:624ced7807d0be3e607557aa81daf5ce4e9773312389f834dd74b03560e15c49`  
		Last Modified: Wed, 23 Apr 2025 19:43:07 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
