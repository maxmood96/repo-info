## `clojure:temurin-25-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:2f775c3ed8d7ba2e4d13d2d9abd77ba5c920923dffe642a9a49f20ad976b85ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ad493972f7c60f91d67248324e824d4941cdee2ef6e4d491cac193eb4a859f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178933523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad9e2f3bff316213c9b5654aae8f52109131d0c9d1bc9e657196a5c86b9815d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Thu, 04 Jun 2026 17:47:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:47:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:47:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:47:23 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:47:23 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:47:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:47:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:47:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:47:35 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:47:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8419f4a27c97b0c111ab0dc77e0159bd3abfadcb948d4a49cf6dd6670703b84e`  
		Last Modified: Tue, 19 May 2026 22:36:35 GMT  
		Size: 30.3 MB (30257598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348d0ef944c64a2f080b25bf635db26b7fa54855f7beed816e91919754e5eada`  
		Last Modified: Thu, 04 Jun 2026 17:47:56 GMT  
		Size: 92.6 MB (92574586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36009b8a1a3f8466c0afda0963159fe0f0ba56d878ec029e24f37af0c4a83a78`  
		Last Modified: Thu, 04 Jun 2026 17:47:55 GMT  
		Size: 56.1 MB (56100296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303976516e76b0ef8b90167c4dc58c36e267e8c1ccf1a4f21763e38ecefa92e3`  
		Last Modified: Thu, 04 Jun 2026 17:47:52 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b8ef22bd4c7244200a6b9fa979470a671b34971ec7f1171528e01913ecd6e9`  
		Last Modified: Thu, 04 Jun 2026 17:47:52 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d9fe476dd566777c49e5d26b0db5fbd726cc93b3f416a2ca1ccfec9be4c73d20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5302614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4530cc769d47127684bffb30051e5f775ef387c8e841feb2b2709803b728423e`

```dockerfile
```

-	Layers:
	-	`sha256:628e32a9855749f19b128c82e4cee8c1954c6ec9e8a32d3e045db695dbf804e9`  
		Last Modified: Thu, 04 Jun 2026 17:47:52 GMT  
		Size: 5.3 MB (5285935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dc7f99b4ee08d6ca59908f0b65028157a357150b9228a0e344feab1b72de017`  
		Last Modified: Thu, 04 Jun 2026 17:47:51 GMT  
		Size: 16.7 KB (16679 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1704a5b5613bf7263c090a0a5ee0074231acbabe166510ecc7920fdb9da4f849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.6 MB (176553520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57117272c71a2dd2ede263c90d908c544596cd5cc78d9f880211a1f680210eff`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Thu, 04 Jun 2026 17:47:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:47:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:47:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:47:19 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:47:19 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:47:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:47:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:47:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:47:32 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:47:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2b99ba6638377be8e7e1e9a328ebb001513ab9f700c8168d404eed03437c7ce5`  
		Last Modified: Tue, 19 May 2026 22:36:47 GMT  
		Size: 28.7 MB (28742972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83d35abe240900415ba2acb89e995c89b1a4d8dbcbd54b31f1ea6cf6d0116a8`  
		Last Modified: Thu, 04 Jun 2026 17:47:53 GMT  
		Size: 91.5 MB (91542260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae59c27131c7a9b3cb2365be8a713c10ed36624e5ff176600aa54175e8f799e`  
		Last Modified: Thu, 04 Jun 2026 17:47:53 GMT  
		Size: 56.3 MB (56267247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ff52918f538c7dbfd6a486a123d3ea59f865e88316100509dfb100bc43c9e3`  
		Last Modified: Thu, 04 Jun 2026 17:47:50 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15dac6a344704f0af26cd6b515685943c090cff2872c952acd33346d15c0eb8e`  
		Last Modified: Thu, 04 Jun 2026 17:47:50 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:93886e899ebf2d6dc10efc947635289ac832403b2407a5998b2c2059ade4077e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5308509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cdeb925f6d68bff54f08d9588876eabc851bd97ac568f27b9f08085d172b60b`

```dockerfile
```

-	Layers:
	-	`sha256:3fa1255ff04f2816843d82c1c16dc92e7105df1d5d0749a42235046348515318`  
		Last Modified: Thu, 04 Jun 2026 17:47:50 GMT  
		Size: 5.3 MB (5291688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3f3e8e739631bafd5946a1754d7de007eae2cd351753dffbf70de95fbfbe91d`  
		Last Modified: Thu, 04 Jun 2026 17:47:50 GMT  
		Size: 16.8 KB (16821 bytes)  
		MIME: application/vnd.in-toto+json
