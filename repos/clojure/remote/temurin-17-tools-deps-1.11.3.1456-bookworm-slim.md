## `clojure:temurin-17-tools-deps-1.11.3.1456-bookworm-slim`

```console
$ docker pull clojure@sha256:195ba015315dbb015ba985a5f16f094d4d1f3884f3ca486b8d53f2b64837eeb0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.11.3.1456-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:786b9ddcb0a42e9349cb79e338693920e844f48428c079c637df2d3e6ce9807e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243115176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19cd3ae1bcd85a6aece8b6458a39fc933c93800895ed42e1e0e11a6c26587de5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c27c506ae9a92327a0e91feb06bdbf6ca47bf557a5163145f38a18de3c89aed`  
		Last Modified: Wed, 05 Jun 2024 06:10:24 GMT  
		Size: 145.1 MB (145095123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5933d949c8c76661296c769f95e0e7ca840be06f46e5836eef103d036c8c8a6`  
		Last Modified: Wed, 05 Jun 2024 06:10:23 GMT  
		Size: 68.9 MB (68868597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d4c957b7c81ff71f11bb7a2262570ccea04926d94967b41ce82c6faa40918f`  
		Last Modified: Wed, 05 Jun 2024 06:10:22 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f82c78e0c91236dd3e9576ae6f1f7fa8306071da7e537dd202759be6772bf1f`  
		Last Modified: Wed, 05 Jun 2024 06:10:22 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.11.3.1456-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ac9b6fbf2b90f5bee9cdd5848f336c6e644b38584afe7ab82ef17d64000571d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4720400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def88153592a42a4a288bdc17e7b37ff41d2dc7357f70c9b847724b5c115e890`

```dockerfile
```

-	Layers:
	-	`sha256:b4d6ca06769d341957ede537b773b82c9e45cdafb5aa3646aa89afb3fffbbe31`  
		Last Modified: Wed, 05 Jun 2024 06:10:22 GMT  
		Size: 4.7 MB (4704938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffbc6a005c36e91e4ace0ba6166ce12857d648f2d9cfaf36be0bf97dfbb4e632`  
		Last Modified: Wed, 05 Jun 2024 06:10:22 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.11.3.1456-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:579c501f2308815c6bb253d326e22571c554424e9e530b29dd6d43ed97edbcb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241694374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b1850a97a4e93c62d5d76ef9c6de818afafbd21b632a3a243f0749732e753c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22608349e93829bba81d2d208b5bb14cbc7cb9450f4d75e80ac257e503978d5`  
		Last Modified: Thu, 13 Jun 2024 11:36:10 GMT  
		Size: 143.9 MB (143892766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbd9b37888c8808647b02d46fa609aa6e90204490f99c48b3fa1397754bc207`  
		Last Modified: Thu, 13 Jun 2024 11:39:30 GMT  
		Size: 68.6 MB (68620895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95033a0ee28816eceb2eea35b89be11505b0eef35f924f05f9cc3087753ac991`  
		Last Modified: Thu, 13 Jun 2024 11:39:28 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d723d18fcda060a87617371d4c00756a8f5e4d7f66156b9edaf5afcda9eafaaf`  
		Last Modified: Thu, 13 Jun 2024 11:39:28 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.11.3.1456-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:61a9d77000c99c110f6019040169e3284a88e28457be806be005a8e3560bdd2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4727376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07c1ce7eb3d68240f822c315bbd72756dfb23fbe7488e00acc12dee7dad2ae6`

```dockerfile
```

-	Layers:
	-	`sha256:628c8adacffb3f4826bb5416ed54b328e2533e6cc94303a75c4403739b28511b`  
		Last Modified: Thu, 13 Jun 2024 11:39:29 GMT  
		Size: 4.7 MB (4711323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:849a35f6ee6602e4ab8a5838196ae3bf29bd725ab8150bc2cd5def4170fceb5b`  
		Last Modified: Thu, 13 Jun 2024 11:39:28 GMT  
		Size: 16.1 KB (16053 bytes)  
		MIME: application/vnd.in-toto+json
