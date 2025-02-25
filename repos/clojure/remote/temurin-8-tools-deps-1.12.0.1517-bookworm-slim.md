## `clojure:temurin-8-tools-deps-1.12.0.1517-bookworm-slim`

```console
$ docker pull clojure@sha256:f39a756f5d861ece2768ba861f5c9d282a9008297adbf7b1622aab7176e65a70
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1517-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4dc96a56171fb17b26d9cdce8126a11ded2c672a648884e8d8692c4adf1d01e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152471598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27af2d0041698e468b6369b43b24766d43df250d03b2f402fedaf58f823ea1d1`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bdb4fec2658a39c7df07d80264d50ef4eb238b7d7d7d4e9311b7edfceca6bca`  
		Last Modified: Tue, 25 Feb 2025 02:15:07 GMT  
		Size: 54.7 MB (54721249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc08753020930c34130b0f9949a528d16c5183109d50a478f9603aea93e68982`  
		Last Modified: Tue, 25 Feb 2025 02:15:08 GMT  
		Size: 69.5 MB (69530403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ba7a97d35185cdb8f8ec100e0026e121890d25b38fd7e56fb40dc9f97e7381`  
		Last Modified: Tue, 25 Feb 2025 02:15:06 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1517-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d9a4d9bd1036bed60bf53e4ea1a9c5eef2d8c11a877c7b7de7a567d2f9aac5b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5048486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:448131a81e11d161cfbaebaa0ad1ecc59270674877f94a969a888dccad685feb`

```dockerfile
```

-	Layers:
	-	`sha256:350cf0f25fd951b5e75cdaf695df1e66c474d09e19783243cd6422eebebd6732`  
		Last Modified: Tue, 25 Feb 2025 02:15:06 GMT  
		Size: 5.0 MB (5034195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:174355127a94f7a08c44e0e827fa1b66222b51a87324399cb69cee9f319a6c5e`  
		Last Modified: Tue, 25 Feb 2025 02:15:06 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1517-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2b2d4a9d9e4763b07d16c06fa45696a42f20abee1fd556219bc299f733ebeadf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151251189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a5eade9023daf23b29655e0ef7ad298d7d2185256e9fdec3965458bb8428f68`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f3692fd38222e9c6b1d7291e502651d3034399b2fb165a4370efea22893b95`  
		Last Modified: Tue, 25 Feb 2025 10:50:38 GMT  
		Size: 53.8 MB (53822770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c310891b1813df19d053c10cdc9f3c2a81d3776f0905761eac38011280bc4eea`  
		Last Modified: Tue, 25 Feb 2025 10:53:46 GMT  
		Size: 69.4 MB (69379348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf87c4984cb2978edc7bdb176269196ab9f1356b0120f8458fabc68826b24d0`  
		Last Modified: Tue, 25 Feb 2025 10:53:43 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1517-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f6957a8307c1bd6553c32f45f1537ed7f12a2f9f9ef2322b5dcf28630408d4ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5055063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71732fea5ad8d6f0a34c9961ec779521554b25db7d22413860a1869e20e0803a`

```dockerfile
```

-	Layers:
	-	`sha256:8947fee029e8340b8a989756c38c45d544ec47e18803ce8c07ab0cb7d4547664`  
		Last Modified: Tue, 25 Feb 2025 10:53:44 GMT  
		Size: 5.0 MB (5040654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0503adebf190cbfb72e22b82806f71152dfdb46c8a30de9a7ebf2d4011b319da`  
		Last Modified: Tue, 25 Feb 2025 10:53:43 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json
