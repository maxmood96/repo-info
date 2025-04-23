## `clojure:temurin-24-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:f1a4f05ef4bb2a12547c02e05c881a102f869b4c3ed00978c48919736a861abc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f47e6a4c9d4b8251e23b7fa862ab73a3a21f3e34f451c1edef900ee6e78e82a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.2 MB (179203433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c9e781c9e9ac1dae4833f2825e8f9ed5b1fa1f8a647dd05cde346e055a6d42`
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
	-	`sha256:dee42e78fd78442427d7b1fd5874548153b4147c3bb4c0620b7fffe6d9992563`  
		Last Modified: Wed, 23 Apr 2025 17:16:40 GMT  
		Size: 90.0 MB (89951972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bea45f85d4624f1f3b9c3d55c130313718ee55ce2504406b1b5611c87165481`  
		Last Modified: Wed, 23 Apr 2025 17:16:40 GMT  
		Size: 59.0 MB (58992998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c7f96cf7a88c1d64186418d6fdf46d57207b47bb683c7a5160eb0d9431aba6`  
		Last Modified: Wed, 23 Apr 2025 17:16:39 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38490e4e176f32735fa4b4b88c03eaba3164af2caa5fa7a7aa10e2cd92648c4a`  
		Last Modified: Wed, 23 Apr 2025 17:16:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3b487b88b1f283d6f0834802471f4acbb068cc6827fdb715f56061d9d4c273bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5085531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc5597d1cc87421c29108c447ded4721f421cd9464628e166d984b898ce8ba3`

```dockerfile
```

-	Layers:
	-	`sha256:9f754d22279b99c99395ba2ebbbd63886c2ecd95c9672b3596b679b7771ab7ac`  
		Last Modified: Wed, 23 Apr 2025 17:16:39 GMT  
		Size: 5.1 MB (5069659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90c095871a4d95c5266b44aefcb8c5bc4daeb307220ff7f2deeacb08d798384f`  
		Last Modified: Wed, 23 Apr 2025 17:16:39 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bullseye-slim` - linux; arm64 variant v8

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

### `clojure:temurin-24-tools-deps-bullseye-slim` - unknown; unknown

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
