## `clojure:temurin-17-tools-deps-1.12.0.1495-bullseye-slim`

```console
$ docker pull clojure@sha256:85eece906bf52374a515a42b088217c4898b7ac3ee19850569772f21d9b6fa45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1495-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:dda2b5ac888404437c609f9d8168c492d45950fa345e85ec1f07fd78ba00ff59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233571295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d62e949e322dcce907ec67010b8ee53eb65469d6a9ecac58516d1157b32b8931`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6c87eefc1f428634061bcdc9ec95ccceecd7c7475d35a777479af83f64ee6915`  
		Last Modified: Tue, 24 Dec 2024 21:32:32 GMT  
		Size: 30.3 MB (30252643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcd873a2ba404c4bb79683f56dd4c83c3c2b8c6345409bbf90ebed73b45aeed`  
		Last Modified: Tue, 07 Jan 2025 02:29:29 GMT  
		Size: 144.5 MB (144536716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f03a0282eeeb574256707ec040c44e4576f44e8a2e09032f01b8122f2bb2284`  
		Last Modified: Tue, 07 Jan 2025 02:29:26 GMT  
		Size: 58.8 MB (58780897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4130151c203d3266d2814d3c7bb63e088a74cf147b9d5a43de515b1be6b7684e`  
		Last Modified: Tue, 07 Jan 2025 02:29:25 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb3c5e9d5e2918a41b72ae1f8690f9943a237cb4be68a7ca9e64cac1987fd07`  
		Last Modified: Tue, 07 Jan 2025 02:29:25 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1495-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:eab85d4bf0377dc5b9813688d00c5c950b8fc1d17b7b0f198cb9f79f4dce668c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3477ff55760e03bb646e15cd410d785d8c4f616d1f4fa76221e0a2bf4ffc7863`

```dockerfile
```

-	Layers:
	-	`sha256:fcfba5e91c1d7747ad86848e12c64bcca0e2b1ce9effe78daa35a057371d859c`  
		Last Modified: Tue, 07 Jan 2025 02:29:25 GMT  
		Size: 5.1 MB (5117069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3c84149d0df59286416684d28dc623f91a7db868374890e8e5776a98a3c522e`  
		Last Modified: Tue, 07 Jan 2025 02:29:25 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json
