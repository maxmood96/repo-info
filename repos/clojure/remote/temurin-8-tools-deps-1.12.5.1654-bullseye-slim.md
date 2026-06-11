## `clojure:temurin-8-tools-deps-1.12.5.1654-bullseye-slim`

```console
$ docker pull clojure@sha256:3f4b156c90c61a4402102a75e2f675f9370615483559d9f9ae7df721e2853e5e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.5.1654-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2ec54d7718be67f493b277c3254178c58df30e4b77ebd7ffa0332132774a8777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141559869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011fd0445bf0a6758e3c4b5e6229b1360f9be6ce346b4a11cc786d597880982d`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:15:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:15:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:15:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:15:40 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:15:40 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:16:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:16:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:16:37 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:55534d9909ecd18467599b415fa2553c3106849154ae8a361a75f1a24f2a4364`  
		Last Modified: Wed, 10 Jun 2026 23:40:12 GMT  
		Size: 30.3 MB (30260255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd1a4be12a3ed9435b7e5c3bb1bd0c2b5d6ef8e1ceeba1d0bc7fd81e051ec8d`  
		Last Modified: Thu, 11 Jun 2026 01:16:10 GMT  
		Size: 55.2 MB (55198723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9697fa08d66917a002bff6dd4dd4a3fa59ce2ac9448fcd066084f941c779d08`  
		Last Modified: Thu, 11 Jun 2026 01:16:51 GMT  
		Size: 56.1 MB (56100246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c1dbce16588bdd3de6004150d2acb9d537b5e4f5ff04295136be2ef04cb78c`  
		Last Modified: Thu, 11 Jun 2026 01:16:49 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.5.1654-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cfb71da515cfe6e3d50239c699fb889ddc13d4ab09fb107215ac85aacd15ce6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5451657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:373646dbf57eb5c98621771bfb94be2fcffffe61069b1b49336adf261b748a6e`

```dockerfile
```

-	Layers:
	-	`sha256:0edb57b029ee467aadeda76ffd5f1e01b221b0dee351a8570d9d8fd2749e3cfc`  
		Last Modified: Thu, 11 Jun 2026 01:16:50 GMT  
		Size: 5.4 MB (5438209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d10a560aa032cfa46d1184e6c029368ad9d494fdc5afd96d2c90f317344cbf3`  
		Last Modified: Thu, 11 Jun 2026 01:16:50 GMT  
		Size: 13.4 KB (13448 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.5.1654-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dd54ada53558de1db1f49555c3b352e7ee962c9858d1075b25ac2629fa3261d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.3 MB (139287252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d61c6f41c32aa76ff30e8e37950130cbae36867928b5df87c504de7bb251967`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:19:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:19:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:19:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:19:54 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:19:54 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:20:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:20:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:20:45 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ca483a18241c226a06a4a4afd22dc5496062254c671fa595136458fb8fcd0107`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 28.7 MB (28746154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdf5e245f425b3b061e73b36ea2abe8a56a3ecc6ce2d5695c6bf1928f092405`  
		Last Modified: Thu, 11 Jun 2026 01:20:24 GMT  
		Size: 54.3 MB (54272922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d93f9aa782b142a48493b9c3f650fecae45429e630f88e0efc2d412aacdcf65`  
		Last Modified: Thu, 11 Jun 2026 01:21:00 GMT  
		Size: 56.3 MB (56267531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c255e6ccc7f79c8ae14af9617c74a95056f7e7dbcb5915b7bd1dc590f650d6`  
		Last Modified: Thu, 11 Jun 2026 01:20:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.5.1654-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:586b2d34838e26b94df4c995da457b4de7087d6ec3982fc3252c3cff9b73e694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a007c14289b93372a1220153b7043501867b4354f1764f72c94b4c54d6fc167e`

```dockerfile
```

-	Layers:
	-	`sha256:97ba66998edb83d88d12ea8a85a7e4fbcb6f30f87af23ff24dbc7b2440cc6f07`  
		Last Modified: Thu, 11 Jun 2026 01:20:58 GMT  
		Size: 5.4 MB (5444641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0707e481f1b676e910af017d1cec84b699a4a47b71ce3cdd298856842b097267`  
		Last Modified: Thu, 11 Jun 2026 01:20:58 GMT  
		Size: 13.6 KB (13565 bytes)  
		MIME: application/vnd.in-toto+json
