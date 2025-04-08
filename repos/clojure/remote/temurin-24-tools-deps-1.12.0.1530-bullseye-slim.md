## `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye-slim`

```console
$ docker pull clojure@sha256:0ed39622769ead80bbcb8bd9428dcfdb4102cecd90f7ee83ce001f72cbedb9d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c3dece1d213e327e44890cffde7e5a9bac0cb391dba6793aff537a8a2e7ce6f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.2 MB (179200288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c07941276eb6a7ae03aa1598e824044c88abe0e17c56b310e1a43e8c780cf61`
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
	-	`sha256:63eb247c3c702339b2f368f5def817eeb52fe9335b5c7178fe1b0b9379133c83`  
		Last Modified: Tue, 08 Apr 2025 01:37:56 GMT  
		Size: 89.9 MB (89949037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d71fb680be5bdfcd4ee649b0ded7f42ff262a69ce61cd1a75bb653e659c0e8`  
		Last Modified: Tue, 08 Apr 2025 01:37:55 GMT  
		Size: 59.0 MB (58992794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94f59c553835889c1bd039630a67dece6f0ecb407ca61f1c36489f63cc141da`  
		Last Modified: Tue, 08 Apr 2025 01:37:54 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30c051faa60d3cbc5b502a6b78f0232e8726a57001b616a46b17ccc54bfb6e2`  
		Last Modified: Tue, 08 Apr 2025 01:37:54 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e8f17f60e3c8d6860e061b6b4e702279ef653f7941ee4f97cca2cce7b39197fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5085517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e423dc346d1ded5ca9cc0264e5b32314d75c5909143083d735913a328369c6d`

```dockerfile
```

-	Layers:
	-	`sha256:0f51788af19ad145a74cb1640b5477d306aeaf08f500bcd56fba3c33c6aed642`  
		Last Modified: Tue, 08 Apr 2025 01:37:55 GMT  
		Size: 5.1 MB (5069645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3551adbc0876299599dfbedc1e0e99a4530b2a4097f8e65911b4a68c4e32966e`  
		Last Modified: Tue, 08 Apr 2025 01:37:54 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8a253490db89347cb1798f925ef4e4c116234fb8b4139e6314568655ef81b6b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (176970753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45e6bf8b2065963111fab85e49e989aa38dbea07fb67373a4c520c48dd7c31b8`
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
	-	`sha256:0ce53162f17d7825ca3d155dc21d219a55e5efbe94eefc1dc69ca305f80be34d`  
		Last Modified: Tue, 08 Apr 2025 11:39:37 GMT  
		Size: 89.1 MB (89092707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f210791e3c5489851d9370619629e980b002d87a3cce239b92b27ee8344bbb`  
		Last Modified: Tue, 08 Apr 2025 11:42:16 GMT  
		Size: 59.1 MB (59127509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3ce4b6f3c7524f92f70bfdda87aae2606567a2f9a9fba1da70f1346cac3902`  
		Last Modified: Tue, 08 Apr 2025 11:42:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67b4de9fdbae200bce46e27e060fd219900f8006b8f7e18f25b42d1b5efc89e`  
		Last Modified: Tue, 08 Apr 2025 11:42:14 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:411ea5396d7da819ec02d01dbe35c26b6670e0ef0337215bbf18fad29ee3e81f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5091364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834e2a5a07be3dbdf2d499fbb0c5d0c4b30a64b88183f0288c2d8bb4ff052f5e`

```dockerfile
```

-	Layers:
	-	`sha256:eec074421fbd4c727f0b147ddb1bd319cb3770b393bf4feb008dc098ed795648`  
		Last Modified: Tue, 08 Apr 2025 11:42:15 GMT  
		Size: 5.1 MB (5075374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:325ffd92d8b5092c22adcbf488e4095b45522af73000c446ae41f25e77d5d2aa`  
		Last Modified: Tue, 08 Apr 2025 11:42:14 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json
