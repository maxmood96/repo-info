## `clojure:temurin-17-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:9784e42b053d86af88b69a2d1ec3a6d3dab128f7993c38a3b0652a89927d75e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2df42ded5be2abfe34d548effcaa63603e1fdae8a234e1d033491b801ba0e8a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242317297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9ac90879e65b002f94e2527853067325c589e4a64eb9a55df36036f7b7ca54`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf03e0c3a6ea52e34458201dd1df27704b40eb46ad9cda6d082511cab298db7`  
		Last Modified: Tue, 25 Feb 2025 02:32:50 GMT  
		Size: 144.6 MB (144566549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb5a3b2112dbc54431f248175e553ad90397c078a5092c5b37887f0bcf47a3f`  
		Last Modified: Tue, 25 Feb 2025 02:32:49 GMT  
		Size: 69.5 MB (69530406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746e55a5ce7c9708040f2f58115927ce6fcb42cacd0aeb4dc7178b8c560a054d`  
		Last Modified: Tue, 25 Feb 2025 02:32:48 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8aced933c9daf6a4a5dfecf1878aed6d464b4a67c222d42d92aca85234a0ae3`  
		Last Modified: Tue, 25 Feb 2025 02:32:48 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:424c368e9718220bce3f5106979a96024a2858d953a624654674723691a19342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4928464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a12a3e91381aea86036d77d8209ca5a81d20cbb4d3be243efb0d000b6eb0e9`

```dockerfile
```

-	Layers:
	-	`sha256:75b98daa5a54ed26720778d3faed0ffc2a9a55a1c6f0075bbde4940311ff04d5`  
		Last Modified: Tue, 25 Feb 2025 02:32:48 GMT  
		Size: 4.9 MB (4912585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53f333401330b68bedaa3d2070bd294acb6f34f9833fd8a94d2b723aa931450a`  
		Last Modified: Tue, 25 Feb 2025 02:32:48 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:28e9d0d2c15024e7b49e99bf336979399c0a3030d052d25bbc2328e1e765bfa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240883446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f1d77ffeda06ff8521ef9c4e20e4510a5e4501e83fb7ae18247f1de8e34d5df`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5cb4ddbefdc1f0c1073972dc799e34b039fe82f27484acb4e57384df5a407d`  
		Last Modified: Tue, 25 Feb 2025 11:03:37 GMT  
		Size: 143.5 MB (143454729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8cf57bdf03b58b9a24ab35e9cc7eb52c90eb29f7953457b8cc0ad9dd5f5d75`  
		Last Modified: Tue, 25 Feb 2025 11:06:49 GMT  
		Size: 69.4 MB (69379253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057047550854d6a8ec75d07b83ccd36fd6f506890138bb48fb4de49b7ef73e1f`  
		Last Modified: Tue, 25 Feb 2025 11:06:46 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef7cabbbf7cbb476eef48cb30725cc6fd33ce89d87f0d9258eae7b968102720`  
		Last Modified: Tue, 25 Feb 2025 11:06:46 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e68f546284101e25f34275957c12185eb80533f52417a6deedb9a97e3458ef4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4934342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33cc23c02673c07f7c5c89a3c28d20695a7a74fa5284f127b994c9653ac21ac2`

```dockerfile
```

-	Layers:
	-	`sha256:d4826024febe4f5795c9914f35010d2d4a2267354a9f6da5490501240bcbeb3b`  
		Last Modified: Tue, 25 Feb 2025 11:06:47 GMT  
		Size: 4.9 MB (4918346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b859e73c811803bbbb3080cc02f8cb7dbae5c79ade6eeba0c6a17d008f9432c`  
		Last Modified: Tue, 25 Feb 2025 11:06:46 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
