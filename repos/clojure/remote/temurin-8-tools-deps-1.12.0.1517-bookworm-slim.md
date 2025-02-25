## `clojure:temurin-8-tools-deps-1.12.0.1517-bookworm-slim`

```console
$ docker pull clojure@sha256:319cd1f813b1d94ed348442840d2a6e1799dbf57b7a738209e7ade29db666164
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
$ docker pull clojure@sha256:3b58935c93a98052bccf5616a65e4f9a82b22568e995a2eaabcc85fb9f9e9af4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151243606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:021e8e748261d0287502a7169e025ebcc69b6ee6988d75287222ec7c38063b4c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369cc069c8bd5d579d827d5defd418fea2cc6c0b401c91c66c1194709652d556`  
		Last Modified: Tue, 04 Feb 2025 23:25:04 GMT  
		Size: 53.8 MB (53822735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f897e51b789247d39e01cc3589a08e5be90074749ff78929deec319e18e4140b`  
		Last Modified: Thu, 20 Feb 2025 03:39:50 GMT  
		Size: 69.4 MB (69379347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f081864cb9196c62f26d5d499bb36890fd8a2d826bdde0c29a31cc1ba19339c`  
		Last Modified: Thu, 20 Feb 2025 03:39:47 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1517-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1fb94f946084d9f07fdffaf0c9023fac2975ae38cc543a2bf4732aa7f3d109b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5055045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9da3ffd5eda9424b6599d9fd659223a5d9d03789e12716b6f83b36d4285820f`

```dockerfile
```

-	Layers:
	-	`sha256:ebf1e72914bf2554353dbf5256ea70ab9a31cb8de7cbecb1694189e6fba0dd77`  
		Last Modified: Thu, 20 Feb 2025 03:39:48 GMT  
		Size: 5.0 MB (5040636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c92cdfc36961f27d477f69304aa46530fb2c5414da3ee473219b67d23a769b8f`  
		Last Modified: Thu, 20 Feb 2025 03:39:47 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json
