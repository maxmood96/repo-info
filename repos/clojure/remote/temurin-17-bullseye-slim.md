## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:e0b2a17620082ac63a8ab7496a7ab699e68cea14f66b7c5e7fcab48cb4c16e25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e50bdefb08d99cd0fe109b6048bd4ba648991e586d5f77d6c09c7a6867a0833a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235354744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7db37f2dabafd0da4930c18148b5356d83b63f4ddceda73a1719deb5df9f3eb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:58:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:58:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:58:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:58:56 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Tue, 19 May 2026 23:58:56 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:59:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 19 May 2026 23:59:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 19 May 2026 23:59:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 19 May 2026 23:59:09 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 May 2026 23:59:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8419f4a27c97b0c111ab0dc77e0159bd3abfadcb948d4a49cf6dd6670703b84e`  
		Last Modified: Tue, 19 May 2026 22:36:35 GMT  
		Size: 30.3 MB (30257598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a585ed0844e65030e6439305979d463e640b0da9c7a47b5e6effc3b8d012695`  
		Last Modified: Tue, 19 May 2026 23:59:31 GMT  
		Size: 145.9 MB (145905454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42fbca94cf87685444418ca385ed61babe8f3c34e611a79f334206ffccb8177b`  
		Last Modified: Tue, 19 May 2026 23:59:29 GMT  
		Size: 59.2 MB (59190649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62aa5600719f60e720b6780dd6836175c29c12e7e7e3d639d8c2130d366e2359`  
		Last Modified: Tue, 19 May 2026 23:59:27 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139d66c0b49d23c8739c87c47516df356682764c5379c299a9fc9fa04bf4c68a`  
		Last Modified: Tue, 19 May 2026 23:59:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5df055bee3abd37178b4440751dd13f5d02d32e13fc9efe17c3b64f8a354b40b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5336667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab93b570f0ee420ef530819abe24922b179abc04939221c5386a55782963474`

```dockerfile
```

-	Layers:
	-	`sha256:b57b4fe05685472d4754c6d405e9a2544111a714bca678cbb2073460e38c7b65`  
		Last Modified: Tue, 19 May 2026 23:59:27 GMT  
		Size: 5.3 MB (5320678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a34ad815f6a43b08f61023fec6d5ecfbc33b0dfffa666cb129df8b9bad9602c3`  
		Last Modified: Tue, 19 May 2026 23:59:26 GMT  
		Size: 16.0 KB (15989 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7a43a50c588ea6a8251f17e00b0e4b0bef404a1eb1fc098e6b63d8e4ff98f4e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232828256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69255aec051c7b4b1ae13964abcde7891024906c70be45e7ab5ba672676988a4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 00:06:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:06:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:06:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:06:11 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:06:11 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:06:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:06:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:06:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:06:24 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:06:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2b99ba6638377be8e7e1e9a328ebb001513ab9f700c8168d404eed03437c7ce5`  
		Last Modified: Tue, 19 May 2026 22:36:47 GMT  
		Size: 28.7 MB (28742972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628cddc4f0a6448c1d2e8101705a957e5183a1891e2a07e6e3c16973af60be06`  
		Last Modified: Wed, 20 May 2026 00:06:47 GMT  
		Size: 144.7 MB (144724358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206cf9aaadade9553dbc7844c680e615c8425353e49167f805433f9e83c75cc7`  
		Last Modified: Wed, 20 May 2026 00:06:45 GMT  
		Size: 59.4 MB (59359884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30868a546db60dc1c9a20c31b9cd114d9c33b3061f17c4ae001d893526d7228`  
		Last Modified: Wed, 20 May 2026 00:06:43 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c3f8ad36cb89471169d4dc4de079ce92891120e3cf8ca4b49dd106fe28b604`  
		Last Modified: Wed, 20 May 2026 00:06:43 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0fd18df5031ae90bf70ac46181119b0895785eabc0e2e4894b36e0beb8fe2e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5342518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a89077c6529f586ee6d85c8c08f5d91af748d6e85ed43e50b5543bfe25fc2335`

```dockerfile
```

-	Layers:
	-	`sha256:8dd20408b7ac266719d65da99e5f605077858f4c1618a761e94d3f3b34168e6c`  
		Last Modified: Wed, 20 May 2026 00:06:43 GMT  
		Size: 5.3 MB (5326410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:194e47ed5022ad11c81cfdafe0680a40659687e389ab488ff8eb3c1e520780c0`  
		Last Modified: Wed, 20 May 2026 00:06:42 GMT  
		Size: 16.1 KB (16108 bytes)  
		MIME: application/vnd.in-toto+json
