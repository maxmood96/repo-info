## `clojure:temurin-21-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:2ace7de45edbe95e2536d2cca603dd2c0892ee267c8dcd0af83c76da3cbd99bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0bddf3e58e8cac7c48c5a3e7e2113fdc43a129f45499e95bfec1da5f9c7d12a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244525948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15bdb64afdb20079df4afae79526f9ca4589f456ef92b74af683981ae0f01b85`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Thu, 04 Jun 2026 17:46:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:46:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:46:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:46:46 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:46:46 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:47:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:47:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:47:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:47:00 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:47:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8419f4a27c97b0c111ab0dc77e0159bd3abfadcb948d4a49cf6dd6670703b84e`  
		Last Modified: Tue, 19 May 2026 22:36:35 GMT  
		Size: 30.3 MB (30257598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270cda023211248fd129f41ae115b5eedd5f5f208f4da019e0b9aca2925668ed`  
		Last Modified: Thu, 04 Jun 2026 17:47:24 GMT  
		Size: 158.2 MB (158166904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730a5bc26cf9a7a989fc123a667c39dffd5b266d5a9ecdf1e294c8a5458bcc44`  
		Last Modified: Thu, 04 Jun 2026 17:47:21 GMT  
		Size: 56.1 MB (56100399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a235c3e86c4c91acfbe2b02280bd6ade43cc0fd90a88ff31a3ae5bd5a33c37b1`  
		Last Modified: Thu, 04 Jun 2026 17:47:19 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c41cdc7131de19dff53694a60b1685579b3059c9b042ea27634a7ac248f058b`  
		Last Modified: Thu, 04 Jun 2026 17:47:19 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b49d7412427f2e1ad5273fab223c077b8f104ca41c1324a615651e02a3328890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5335687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba184fa62f073618cde3a7d52955492bcd16791fbd73f0315c601344f36be65`

```dockerfile
```

-	Layers:
	-	`sha256:accb3d5c74cdbd2007fb18d9a37b7f0e7b990771b7448b6700acf44b0161ce51`  
		Last Modified: Thu, 04 Jun 2026 17:47:19 GMT  
		Size: 5.3 MB (5319697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d7dbf1bbf31ce23de8ebc6acb1f24ec5dbc085eebe22542071bd30c178f8299`  
		Last Modified: Thu, 04 Jun 2026 17:47:18 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a519c7e79d10a8d3c576125b67f8555b1c76c8d483f1b05125be4db4a0caa996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.5 MB (241473790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d1b5fa5d26dd42523cd967656d5725996adfeb111cfac3606060c4d05391feb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Thu, 04 Jun 2026 17:46:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:46:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:46:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:46:33 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:46:33 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:46:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:46:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:46:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:46:46 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:46:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2b99ba6638377be8e7e1e9a328ebb001513ab9f700c8168d404eed03437c7ce5`  
		Last Modified: Tue, 19 May 2026 22:36:47 GMT  
		Size: 28.7 MB (28742972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22122758a5112415adbf1b41ec50572980981fb51cb7f689340d059c7a8bc164`  
		Last Modified: Thu, 04 Jun 2026 17:47:09 GMT  
		Size: 156.5 MB (156461285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea3f40d12b773d210a651a782a3fe3b54530d39ebc5b297619952843a386f75`  
		Last Modified: Thu, 04 Jun 2026 17:47:07 GMT  
		Size: 56.3 MB (56268486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3978b88341cc58eb82c871f34138f49f25363a7b715be46ca93dc7797b5ba178`  
		Last Modified: Thu, 04 Jun 2026 17:47:03 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99457f46bb054bd3ca05e60a91492dce5e27113b8d72d74d21c93ef540cc6a56`  
		Last Modified: Thu, 04 Jun 2026 17:47:03 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c36b7d206b8aaeaf6e307228cd12e8ec3d08278014af6d77765039d4c52fcbcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5341536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92b2c7e1712f1a1e808c5ebfe3ef22d28f8e014cf7db1275d0e769350bdb4ac2`

```dockerfile
```

-	Layers:
	-	`sha256:74ef1fe05fae8f0421d7278139224aefa4274f9d5872244532e793530546b1dc`  
		Last Modified: Thu, 04 Jun 2026 17:47:05 GMT  
		Size: 5.3 MB (5325429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cff381c231c37bd870b60c979add94d58e9510cc1e8c54a2a238f2d5a8d2aa2f`  
		Last Modified: Thu, 04 Jun 2026 17:47:04 GMT  
		Size: 16.1 KB (16107 bytes)  
		MIME: application/vnd.in-toto+json
