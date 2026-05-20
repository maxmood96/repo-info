## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:7aa225d91469353e924c6dd49fce4156b07ce8989c19c66d2a181cd5a8a44528
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2d63afe6b2b511f2e93b6db58f3638af4ef6528fada5daca11b45e6f525253a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.3 MB (235335133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:649b40c943e9e91eb00a8f47b6229fc7b20580155e84fbae19c82cc82ffbf3c0`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:58:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:58:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:58:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:58:06 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Tue, 19 May 2026 23:58:06 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:58:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 19 May 2026 23:58:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 19 May 2026 23:58:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8419f4a27c97b0c111ab0dc77e0159bd3abfadcb948d4a49cf6dd6670703b84e`  
		Last Modified: Tue, 19 May 2026 22:36:35 GMT  
		Size: 30.3 MB (30257598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7ecd66494d308b312bb9ecf36b0b9fa1b74329f84ea66a13fcdf2574342442`  
		Last Modified: Tue, 19 May 2026 23:58:42 GMT  
		Size: 145.9 MB (145886262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056047fe48630552fc583807e05a800e94a3e0415c1bd59939b314108ab4be80`  
		Last Modified: Tue, 19 May 2026 23:58:41 GMT  
		Size: 59.2 MB (59190627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb692236841675c6c92e77af63da67b17783137efa6ab865f22ad982511e1aee`  
		Last Modified: Tue, 19 May 2026 23:58:38 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:81a4dd375356b23654c19b056e447fe280ec448e45f7c658ae098914ffab94da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5354615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0785dd803a388f2c820ebcf2f7cbaf7e90d5e3799a016b83259e159958dc5bb9`

```dockerfile
```

-	Layers:
	-	`sha256:22a7481678c4a6f5f40b1ebeb049c64dad834ad7f98d0204aec7d7302c25956d`  
		Last Modified: Tue, 19 May 2026 23:58:38 GMT  
		Size: 5.3 MB (5340194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83f4fc0e28e293a0777604d1390f6479a9bf1dcc16a71b6a43f5b1cdeaa4c46b`  
		Last Modified: Tue, 19 May 2026 23:58:38 GMT  
		Size: 14.4 KB (14421 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d06f7df2ad803e0f26fa4edf0c1afa41d5e6f68ae9ca52945e6051d3b5451c54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230686025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c17a97cddeb4ee54754e5b3aabfc9ca7bca46e64bb313fcec40d954a70fbfa95`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 00:05:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:05:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:05:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:05:14 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:05:14 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:05:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:05:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:05:28 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2b99ba6638377be8e7e1e9a328ebb001513ab9f700c8168d404eed03437c7ce5`  
		Last Modified: Tue, 19 May 2026 22:36:47 GMT  
		Size: 28.7 MB (28742972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d746bed89de5e55972ea7c725a36e78ff735fc3bf4e75c80b79aa624e363cba`  
		Last Modified: Wed, 20 May 2026 00:05:50 GMT  
		Size: 142.6 MB (142582223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f834ed729382d5b27be03daab8fb93aa63b73b8f63a20da023198c60baba8a`  
		Last Modified: Wed, 20 May 2026 00:05:48 GMT  
		Size: 59.4 MB (59360184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2e20674d99207723297db71a9d8d38bad8af044c8d066211019b86dd449c94`  
		Last Modified: Wed, 20 May 2026 00:05:46 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bfb19939e278aea82998cf790ba6e486ad0d265da58ba9690bb4c5db4a7a8668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5361083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bed8d6f6f28379ff74e24ea7d0d868965f050d3a795f7e237ce37d951f39e04`

```dockerfile
```

-	Layers:
	-	`sha256:fd5356e2ee6847564efbcb7f035ca4e80e7f9eeb2f46c6dbdac902902c6ad7f7`  
		Last Modified: Wed, 20 May 2026 00:05:46 GMT  
		Size: 5.3 MB (5346544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e7829e35fab7ecd61c76f86d69f834a1384862fa98f3354711bf48a95665540`  
		Last Modified: Wed, 20 May 2026 00:05:46 GMT  
		Size: 14.5 KB (14539 bytes)  
		MIME: application/vnd.in-toto+json
