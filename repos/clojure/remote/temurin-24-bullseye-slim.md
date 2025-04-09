## `clojure:temurin-24-bullseye-slim`

```console
$ docker pull clojure@sha256:a1249c74e709d0290ca9239116222ffc696e1152dd05f910c6da3af7296d66e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e3f4553e49a87f6ec6134c6391882aebcb8b16459d46c0f934d2d7a005740109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.2 MB (179200344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c8765ed415322e6c7d48871a9f3eafbb527c0b086388856899db91ce9e1f62`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8127c6409aa0da2aa077b742929fe7c4efb88475de25a5bb12f7bedc52c5a1de`  
		Last Modified: Wed, 09 Apr 2025 02:19:26 GMT  
		Size: 89.9 MB (89949101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3671161c54a808d1a8a3c98f3b442c679bc2f357bffc54b39d3ad2d325708ae8`  
		Last Modified: Wed, 09 Apr 2025 02:19:25 GMT  
		Size: 59.0 MB (58992787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13246d311e1d9d074cd52538e765f2e8645704fa689547345393fc871f7017cd`  
		Last Modified: Wed, 09 Apr 2025 02:19:25 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711df51abcd02865f57cae23aad2e659e4cf882e3abfec42fe91d95a627b17d7`  
		Last Modified: Wed, 09 Apr 2025 02:19:25 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2ed5459607b228fd79e934ae05f816b61b9512295528acc82df8a7bf7eccbf6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5085517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a9ed613c2150b7d429498c798cf2c99595093f0be4869fc24e396ecadb76c6`

```dockerfile
```

-	Layers:
	-	`sha256:78be9bc64d0b1e73dbd726bfc1c18e10ac5d346cbc9c293b1784baea2a1691ea`  
		Last Modified: Wed, 09 Apr 2025 02:19:25 GMT  
		Size: 5.1 MB (5069645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc68812dd830769ef3f1b51d3f9dc0417bc4c5cd0702e491d4d82b88a237e3bc`  
		Last Modified: Wed, 09 Apr 2025 02:19:25 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dbb8e31a3add6ad032d5ff4782c30d6b4b0d3e11e8b96e2ec7f88e6a6dbd231a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (176969876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a9e62870e3445681167713c3713f7790da8afa6391ff13fd58f26d48fff7e8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468d4121b83272eb440de71d531e8e18529eeb8b0e17efbde785ed87b3576297`  
		Last Modified: Wed, 09 Apr 2025 17:50:30 GMT  
		Size: 89.1 MB (89092779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597fdac2f0202fa7fe62270df2de6c03823d82718804d39b93a94accf0de22ac`  
		Last Modified: Wed, 09 Apr 2025 17:54:07 GMT  
		Size: 59.1 MB (59126558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b7a28108ef93e8202f6b64c561dd25718a2e2739e353cb7bd83f89987119b1`  
		Last Modified: Wed, 09 Apr 2025 17:54:05 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bae51d5e1d3b317eec5641dd09ab584ff05e5db697c80cdfa6e1d7a1459111`  
		Last Modified: Wed, 09 Apr 2025 17:54:05 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9ec49179997911c18b2047e4d6f002ffb03d1954179a2bb15133b7f498188cea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5091363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:217fcdab2123def9dabff01445e15ce94aa5ab8e9568ad6ab47d7cbb75996a79`

```dockerfile
```

-	Layers:
	-	`sha256:a3d846a77dd4120bf1f1d964ebdbb07427930235675e92ec245390681892692d`  
		Last Modified: Wed, 09 Apr 2025 17:54:05 GMT  
		Size: 5.1 MB (5075374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12a59c95b8f2df0a7f34c558e88e800669ae53a0f25c9f421ac70292e1a348bd`  
		Last Modified: Wed, 09 Apr 2025 17:54:05 GMT  
		Size: 16.0 KB (15989 bytes)  
		MIME: application/vnd.in-toto+json
