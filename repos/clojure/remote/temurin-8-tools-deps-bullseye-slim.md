## `clojure:temurin-8-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:b002e322fdb119116041f75dc3e2612d46d48df985d0e9b4d1f5230c0d6e6c3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e93e5b08e41de7450a947e7f1d5f9ee149704c65c71fce4b64031b4b0336318f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193612754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf3878391ad030f5f74c1b7459ba76ea65ef74e8d332ac4b80ee647e2f814f9c`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f910d171ca7f43ccca8f8849b7ef036b8e0a6dfbe2d11ba0f3add224945ac90c`  
		Last Modified: Fri, 23 Aug 2024 20:02:10 GMT  
		Size: 103.6 MB (103611892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d820096016df9617abfe4246ce722fbd5ce59ce5252937aed16b9f75bd9a921d`  
		Last Modified: Fri, 23 Aug 2024 20:02:08 GMT  
		Size: 58.6 MB (58571930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a2244d86508f2a26a871170a04faa952add431cf589177cef83ebe3f91a827`  
		Last Modified: Fri, 23 Aug 2024 20:02:06 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cf6a957b6a4345483db35482d1d14ba7a8534a0b7f441ea54f949ec0197fad1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4989238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b445cdc9b6b83692c3bbf9d9b5829ddbab37613a61c3e727d855151c4fd2a4cd`

```dockerfile
```

-	Layers:
	-	`sha256:cf84558110a56647657ab9ccbbe356c4c3da34b592c2858e21bc02123408d9c1`  
		Last Modified: Fri, 23 Aug 2024 20:02:07 GMT  
		Size: 5.0 MB (4975317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5772a0d97e62ae7ad65499d07538add55bc4706f8b69a5dfb27227a31aeda68`  
		Last Modified: Fri, 23 Aug 2024 20:02:06 GMT  
		Size: 13.9 KB (13921 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b93ab45fad6bef38536c1589d71aacd607a5adee3678e1e2b97b2134eb57fca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191505651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91ff139674a4e639346821da86ad84570033c74bd84a3379131358cd754ef53`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb51859b870a1fb12b81d80a40fc8b349baf98ee32dc9205b1701fc6ba1ea395`  
		Last Modified: Sat, 17 Aug 2024 05:53:33 GMT  
		Size: 102.7 MB (102729220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f107d32853514815ec8e281201e01b5b74d6da5f5ab106e8ad9d0cf2e1517a2`  
		Last Modified: Sat, 17 Aug 2024 05:58:44 GMT  
		Size: 58.7 MB (58699698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818f8270c7375e3a1e2228a3176ba4259f4965ba1264a748515eb365d1b6e291`  
		Last Modified: Sat, 17 Aug 2024 05:58:41 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:356d18de3be51998acc6388256c1423ec80bdbf23df589c462579f21f97c5bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4996134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b832339afb98a2d71024e6ae5b89eded6f69fe8af50845c8b4cf3a82cda638ac`

```dockerfile
```

-	Layers:
	-	`sha256:7c7f4f1b42c375a305b144335bfcc8c5d27fadd6e676838c0225cc642d266a35`  
		Last Modified: Fri, 23 Aug 2024 20:48:23 GMT  
		Size: 5.0 MB (4981673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a14a13f4d245a0c6c28a1742dfad55fef153333c359743919bdc4539b97faece`  
		Last Modified: Fri, 23 Aug 2024 20:48:23 GMT  
		Size: 14.5 KB (14461 bytes)  
		MIME: application/vnd.in-toto+json
