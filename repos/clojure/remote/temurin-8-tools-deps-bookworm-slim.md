## `clojure:temurin-8-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:ceff420316382226962aebb08122bbb163c09f716db7b92a53acdbc0fd7f4fa4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2ce70c85ad17a6775e8718b0ee33332e53777006d59b5c1efb32d1888204d58d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152451297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c9f07a188f87006f2c02dd7a3bc7a0dd30ff850e8bf2c2790f30e1d9a70b1ae`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d66a3e6f11a991c8bcfb09a85fea173739d463b17747bf44f4b63687ab39906`  
		Last Modified: Wed, 22 Jan 2025 19:41:37 GMT  
		Size: 54.7 MB (54711757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44d24947f56b339438b8b482013811273f5f5c497e0b0200698ed7a793517f6`  
		Last Modified: Wed, 22 Jan 2025 19:41:38 GMT  
		Size: 69.5 MB (69526482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413baa9e9441252fcdb77cf4d2950a4cdb3e1fe41d5815703f652a12c2b35f51`  
		Last Modified: Wed, 22 Jan 2025 19:41:36 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:de6008a70d4b54af0f3ce52b1bc9a1cc1e607ffdfdaefab96292b3b35199d32b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5048468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0079c9c5cb2455e114f70bdfca6bddcf417a9e6c3f202470e4dacde819eed75`

```dockerfile
```

-	Layers:
	-	`sha256:37f37056eaaef6ab722f46de2dc8274978eaa66674f56b6380001bd625c787a1`  
		Last Modified: Wed, 22 Jan 2025 19:41:36 GMT  
		Size: 5.0 MB (5034177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75a07d8eac05857e1db1070050f070dd1a91fc0003d440cb99d51e5aa143a694`  
		Last Modified: Wed, 22 Jan 2025 19:41:36 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c2e05d895c7ea34704acf20729fa13a7ee8d2fbd643c6f493be30e5862205297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.2 MB (200163635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ee4fc98885d3e51364aca388d5413e9516edba9328e96b475fcdae8e03748e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b83bb1fef68478b6d0dd97b3acb6cff6ee3d23805e652dee5532d597769fa4`  
		Last Modified: Tue, 14 Jan 2025 12:14:10 GMT  
		Size: 102.7 MB (102747716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80df508aa71d44b83f591de8cf026278390fc0cec0ac64929ab3cdfb0c993eb`  
		Last Modified: Tue, 14 Jan 2025 12:17:52 GMT  
		Size: 69.4 MB (69374242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c498a0b5337859a552c6f1153e368b9c32a2ec60a224139e4a340b3eaf7923b`  
		Last Modified: Tue, 14 Jan 2025 12:17:50 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5b73fe67a67cf9159ce38364819f3f8419952170a177d007c8818af5dd68cfd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5055660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92d7a7a8ab5eac74189f7647c79c1d95e22b7874eaaa67b5b2d7e7663e943581`

```dockerfile
```

-	Layers:
	-	`sha256:beabd75739d9292757fce18b7ae51330ee5a801569a819ce4694bc6c650b0147`  
		Last Modified: Tue, 14 Jan 2025 12:17:50 GMT  
		Size: 5.0 MB (5041246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07a12513a119ce45fdf0755d5a4739b25e488c8aae97ac3851d6e1d8603aa830`  
		Last Modified: Tue, 14 Jan 2025 12:17:50 GMT  
		Size: 14.4 KB (14414 bytes)  
		MIME: application/vnd.in-toto+json
