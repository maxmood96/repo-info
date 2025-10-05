## `clojure:temurin-8-trixie-slim`

```console
$ docker pull clojure@sha256:66001ec099adfc7b937065a3dbe87d78fb9443dc45ea5df7e232d24df9f01cab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:011775eac0888005fd4b55564f07a329067ddfda02105c6e95474aec4e6744ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.4 MB (159448313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e84902e59247460d2756a31247e4622c2576debeac9da804fad535faba7b55f`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9575b199cf37717b38ce7f1ef6b97b12b969c7d1ba7150f349b4f62b6c4e3823`  
		Last Modified: Thu, 02 Oct 2025 08:56:21 GMT  
		Size: 54.7 MB (54731307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c9bc221c2dc118aa7fbfbb831e2a2418ed76f2a876b5f1a2887ab87c9904ac`  
		Last Modified: Thu, 02 Oct 2025 08:56:19 GMT  
		Size: 74.9 MB (74938596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc63ef9130342cfb9f34cf582593f87ea7afbc372a16b85ac7f325944d061a8`  
		Last Modified: Thu, 02 Oct 2025 08:56:15 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8c5adb212e5d3da633f9a3e749cc3231911f10b0e325e4dec87ebc2899977ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5392048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc611a35ee387a40971cc94e15d1422e4bdeb95d2006302d2b72a7cc146ebad`

```dockerfile
```

-	Layers:
	-	`sha256:2ffc4665f97c5844863c87e803a2914b9d50795c6d7e0f1ca58e388a9c78ff48`  
		Last Modified: Thu, 02 Oct 2025 09:42:31 GMT  
		Size: 5.4 MB (5377777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10d421cfa0e0188a70d028695d47f98ef0847f3cf439698634d60f0fa3533a13`  
		Last Modified: Thu, 02 Oct 2025 09:42:31 GMT  
		Size: 14.3 KB (14271 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:45f58fd63a870ee84a8dbdf89fd3779c4715210396f867448e5bf8ee5f544d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.1 MB (159101675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8afc411203aa92c6942365484066bf2c4ee8e3755cc33e28614ac175ed375cf2`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdc0e862221e986d048a88742a958c6883a5404ceeb4d01aa9f9ae9206cdb03`  
		Last Modified: Thu, 02 Oct 2025 02:41:12 GMT  
		Size: 53.8 MB (53835638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e5381a321b431864a56833e2fe7ba110b89c297e5d30693f8c89b5538a94c1`  
		Last Modified: Thu, 02 Oct 2025 02:41:10 GMT  
		Size: 75.1 MB (75124552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bb053ff13bc4cc11f58357140a21e0896b0aa8024d13d0996bffbf23a2a5d3`  
		Last Modified: Thu, 02 Oct 2025 02:41:07 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e4385928ce7ef44779e7af9dc2a7c28f7b80bd7a74e2e4867f53f5e82d89799b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76b732efadb70db5b83c40fcf8e4348428475d437fac094cfa6635c39b7f18d1`

```dockerfile
```

-	Layers:
	-	`sha256:37047328cbca08646561590ba7ced1d4e5bb78dfc25352e69c699d08104234bd`  
		Last Modified: Thu, 02 Oct 2025 06:50:09 GMT  
		Size: 5.4 MB (5384244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4d64a1c316471792306cbf2f9b2cf933f7969c9b7863785355636379619d13e`  
		Last Modified: Thu, 02 Oct 2025 06:50:10 GMT  
		Size: 14.4 KB (14389 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:0a62213bd520f6ae07fab5a0974c303d2855a40702f711594d7c1ec583ff4ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.4 MB (166352677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2d59010125a52658ca456d7daeeb17a11baf34334870513f9d95056c047765`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9067aab8e732984b557828417d0de3a2d89ca2f06d89211d9ca2f289fc08f8`  
		Last Modified: Thu, 02 Oct 2025 08:06:03 GMT  
		Size: 52.2 MB (52165399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e7c3fa8d678181d5564738db276dc02a2889a3bd539060c23dd682bc609c10`  
		Last Modified: Sun, 05 Oct 2025 07:27:38 GMT  
		Size: 80.6 MB (80588179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84aad3f20c3beca240a0cad492721010f35810d037f4154ecffff4b1ccc994bb`  
		Last Modified: Thu, 02 Oct 2025 09:11:23 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e969251ef42209b709561394dabc071f8bd6d3e567701dc400f91c41b1cb1755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6b84511eb1c6ee7d1746b5ddfdd965a8e45083b332862f8b9f54b210395866`

```dockerfile
```

-	Layers:
	-	`sha256:29451a2e8a997c82b661aa303980c54fe8cc4ecbf804a9c9ea3a27aed4d1c43c`  
		Last Modified: Thu, 02 Oct 2025 09:42:42 GMT  
		Size: 5.4 MB (5382741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:239a68229e4c42010e0bdc502ab8b734aec53fc8b427ca4316a93456147afe7b`  
		Last Modified: Thu, 02 Oct 2025 09:42:43 GMT  
		Size: 14.3 KB (14319 bytes)  
		MIME: application/vnd.in-toto+json
