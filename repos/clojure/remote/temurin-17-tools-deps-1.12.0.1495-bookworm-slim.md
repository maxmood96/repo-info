## `clojure:temurin-17-tools-deps-1.12.0.1495-bookworm-slim`

```console
$ docker pull clojure@sha256:4c312d243cc6baf7865b552fe56423504117dd654aa8c63b871ca89b9bf66acc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1495-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3af55b96e691f3c7dcbad8d88902f8394765d833b08d9262b06780b2b8458e96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.1 MB (242081447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa1fcea639be6becb4d5d56793f28e8417f22985a03aaeda1d5a0acac4ad125`
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
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca30158abbec3b5ece744d5bd2a0cac015012b7d5c807f2e9bbb6427a482d05`  
		Last Modified: Tue, 07 Jan 2025 02:29:29 GMT  
		Size: 144.5 MB (144536666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac634878311b9c98406ce42b47752ba54f914bda59e25355c32a095c912533d`  
		Last Modified: Tue, 07 Jan 2025 02:29:28 GMT  
		Size: 69.3 MB (69312160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9ba52f3202736bb11965d59e56144ec2ca5b690a6a455139de5a635413ace5`  
		Last Modified: Tue, 07 Jan 2025 02:29:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372c1204b297bf759703fc9ac063764f5e0974d6cb00da94322d541800b0eb5b`  
		Last Modified: Tue, 07 Jan 2025 02:29:27 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1495-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:071799d01e347b93ef2aad3f6a7b6fc67e396dee1fa11f2e58bf386d35d2f9cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4928448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7933bfb8c41909603b3e20af0d3e0794405c465ca2a8a034c707ab65ebea25`

```dockerfile
```

-	Layers:
	-	`sha256:664b94bcefed45f1155f14a07fc1056ea0fd8af563641c639d117b15a641e9b5`  
		Last Modified: Tue, 07 Jan 2025 02:29:27 GMT  
		Size: 4.9 MB (4912569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10949cfac9316f3f2a4cd809fef65e1755833d8a7dc3b6b0a948c8a570f592e8`  
		Last Modified: Tue, 07 Jan 2025 02:29:27 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json
