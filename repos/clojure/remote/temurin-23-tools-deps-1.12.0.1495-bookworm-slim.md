## `clojure:temurin-23-tools-deps-1.12.0.1495-bookworm-slim`

```console
$ docker pull clojure@sha256:66fefcc713535757daf13519b026d2dada57787d59e8f017848a4e48f2cd2d80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-1.12.0.1495-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b65e7d0a8905fd05155b3af118c27adc35360021ed14f0b0502eb79cc29199d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262840056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c8ad2cd3595f46d394d921e8fdedad9fd76953c1a5b1180b585902f1c50034`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
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
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847a2699066a08d1e1412ae55cd2aad8a4818f1cc8b15b6763b6b84a07ce166d`  
		Last Modified: Tue, 07 Jan 2025 02:29:40 GMT  
		Size: 165.3 MB (165295114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84bd688239a114780cfbd00513fb0659245bd6a734e20c6f7b1f4d3add8e506c`  
		Last Modified: Tue, 07 Jan 2025 02:29:38 GMT  
		Size: 69.3 MB (69312325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa0cfb5ba6d0089c43b1a98087064b22f947b8ceca9501ea655d8941070c436`  
		Last Modified: Tue, 07 Jan 2025 02:29:36 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dca56d6109978bb6ac704538cb9fcc74df9a482314c46d5e965706187626b13`  
		Last Modified: Tue, 07 Jan 2025 02:29:36 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1495-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:835280f8420ed481ce90cba80770f91195891aaa13dcb10530fb71d6f0ee29e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4933452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9353b197046738b40e97a17973d5c489075514196206a9e3eab5f76c6c9263`

```dockerfile
```

-	Layers:
	-	`sha256:d021bff1a5bf105e2f4312366fc4c62cb4db1aa98880f8fa2892180ca42e43de`  
		Last Modified: Tue, 07 Jan 2025 02:29:36 GMT  
		Size: 4.9 MB (4917574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62d2b468290afc61992a4539af4fc49c28aac83597e84a68d343cab4b43e670e`  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json
