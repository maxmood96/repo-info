## `clojure:tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:9dc739ac68a91d15fa3f39ba205bb8997501bf38bf60f6ca767756076f570ee6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ae355fbd4f6fdd70bc8dd9c6baa28ed324b3d76af0fbbc932808bd4317691258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.7 MB (181652347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be1905eafd672ea1092941af6513e599eb85e119a4373aa6c9f6389705dfa88`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 17 Feb 2026 21:45:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:45:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:45:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:45:56 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:45:56 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:46:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:46:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:46:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:46:09 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:46:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77437f05fcd5e08c58d99e1215b19a627c3f59f929740a78b912fee96bfd70b2`  
		Last Modified: Tue, 17 Feb 2026 21:46:31 GMT  
		Size: 92.3 MB (92256289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73bc161045c1423b65a8e7277514bd075a58a2d5604a243000b4874227ceb3b2`  
		Last Modified: Tue, 17 Feb 2026 21:46:30 GMT  
		Size: 59.1 MB (59136731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1580d215465930bbff97b6ab5d81e314137627b825d4dc6e49aa62466406cf9c`  
		Last Modified: Tue, 17 Feb 2026 21:46:28 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c459fe52ebabbc93558a32b015ee78683c03c45386766e311572b4495a77f085`  
		Last Modified: Tue, 17 Feb 2026 21:46:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c402bbd038995a21cfcef56b0cc389ff93902e8a137c6311293aed8bf4b5b015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5294738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2f14ace402134082b8eaca5c5f5cc3c9d2e3fe181455243393c4e9f469905f`

```dockerfile
```

-	Layers:
	-	`sha256:17c094afb41ca95c6071c3d8c1987fe0b612f5793b75ae9c5ae36a098d462f3c`  
		Last Modified: Tue, 17 Feb 2026 21:46:28 GMT  
		Size: 5.3 MB (5278214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bec15a0ebbd6732f7d717ef2f92830cf12dccc14808504b28eb93d8601b33b2f`  
		Last Modified: Tue, 17 Feb 2026 21:46:28 GMT  
		Size: 16.5 KB (16524 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:19761fe37522f273c2419b3cd5df988afbfe517eb9678c2e700c6fcf2379d798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179321769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f74f159f56fc2aa30bcd76ef9a3187df05f91f389b1a94227a5858e8c0619371`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 17 Feb 2026 21:46:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:46:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:46:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:46:05 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:46:05 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:46:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:46:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:46:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:46:19 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:46:19 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0bab5b9a037a7924cbfa7e0cedabf52dc41fc1e49df102241165282dd277e254`  
		Last Modified: Tue, 03 Feb 2026 01:14:08 GMT  
		Size: 28.7 MB (28744439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80424176c68013d3ceb2a7049cbe042719a882198832ddc42ad82131d032c602`  
		Last Modified: Tue, 17 Feb 2026 21:46:40 GMT  
		Size: 91.3 MB (91288273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0dba3126a4760b36269a459ba223313728d0fccba119838c95ec583b8da484`  
		Last Modified: Tue, 17 Feb 2026 21:46:40 GMT  
		Size: 59.3 MB (59288013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3110812ee5729518ad0133feea36306df1215b4261dad27f32cbb0a76202fd26`  
		Last Modified: Tue, 17 Feb 2026 21:46:37 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c88426165470627807beffac244002ac1ee48d47dcee37af2ae9d0b8a7fd56f`  
		Last Modified: Tue, 17 Feb 2026 21:46:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d25335c83df087d77075b596b61c7d54c8f525a1572942aa65e1d866a5c31f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5300634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f295f81f8405ff0534cc09786aa955fa8c61a5654b0252010de8e8b93d16427`

```dockerfile
```

-	Layers:
	-	`sha256:24d06d3a8b2ba6aed3a9a3c1232acc91aee7d9486664e363c3e509f9ab14ebf4`  
		Last Modified: Tue, 17 Feb 2026 21:46:37 GMT  
		Size: 5.3 MB (5283967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56e324ab1618c6f62d7234ad67d9224ace57c1e660811991371f5b96697c9cd3`  
		Last Modified: Tue, 17 Feb 2026 21:46:37 GMT  
		Size: 16.7 KB (16667 bytes)  
		MIME: application/vnd.in-toto+json
