## `clojure:temurin-11-trixie-slim`

```console
$ docker pull clojure@sha256:f1baa56d40fa0d182cbb03ea060a3b01bff7b1507119abaa5acec9c72c774843
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-11-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1285f82397342eb5b4057751789c0d10c56562e8835f679c4478ba558e8147ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.6 MB (247601095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91d83decc3d03eddb8fd1d89c7cfec8b0d4b9ed968cade9058c0897c3a979408`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 17:49:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:49:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:49:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:49:39 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:49:39 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:49:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:49:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:49:57 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848795d850c8f084e4e7720beb6214578e9a048093aff7b4e3343cbab6c5139e`  
		Last Modified: Wed, 04 Mar 2026 17:50:21 GMT  
		Size: 145.8 MB (145806749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf300d29b985c9ed9c26bfcb262e38b63eec12bf75abeaa2eb1daf9c5a8d335`  
		Last Modified: Wed, 04 Mar 2026 17:50:19 GMT  
		Size: 72.0 MB (72015068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4ba6cedd7a7ce291b5c24c480bf58e2fa8cf7be56324cee52b3356d46ced24`  
		Last Modified: Wed, 04 Mar 2026 17:50:14 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:519e0422e7e3a2f05977f52d4b81ea246b6360baf57ec9383ebd18664a974a2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5293446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f527a3ff082342764647febe83f1c86d7f9c49a8007b577cc37b0d06fc6795`

```dockerfile
```

-	Layers:
	-	`sha256:46d0b8af6da4f980046ced4ffe62e3715de66ca5dd2925fb4b467e7c1308ed62`  
		Last Modified: Wed, 04 Mar 2026 17:50:14 GMT  
		Size: 5.3 MB (5279205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d1dd8af5379ce644714150e24dbd7a4c6d671be23ced05e2a6a71d3c0504265`  
		Last Modified: Wed, 04 Mar 2026 17:50:14 GMT  
		Size: 14.2 KB (14241 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1cece545371257e7c249fc90b967fdb411168f704ea83d9a0fe15ec22bbcc790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244473461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7873a35d58b954b0829c273b605277b41edec4ca21162cd83a4cdcf6c408291`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 17:49:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:49:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:49:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:49:29 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:49:29 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:49:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:49:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:49:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75873750afb381eeea87786eb93676f693bae323818b058401e7834cadb32e78`  
		Last Modified: Wed, 04 Mar 2026 17:50:10 GMT  
		Size: 142.5 MB (142501433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75bd32cdd5425d86409aa204a7bda9e2eabbddd3f62173111b58595701f226a`  
		Last Modified: Wed, 04 Mar 2026 17:50:09 GMT  
		Size: 71.8 MB (71831286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492eb6dc976c558a91358cd49e69f70a4bbcc7935325187028aa5a75b0838a19`  
		Last Modified: Wed, 04 Mar 2026 17:50:06 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:45a3e102c90b10a2ea3ab0b0cc9eefad68673f7aba21a946b11cac4dafba0c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5299953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a6cc1d012c1f20ae25e720350068cd304cd7679cfb2c2382bab79d4a19b1b8`

```dockerfile
```

-	Layers:
	-	`sha256:6edf98c262c377c62d69e344944dac836138d5e7f5fd71d16ba0a98f2308fb10`  
		Last Modified: Wed, 04 Mar 2026 17:50:06 GMT  
		Size: 5.3 MB (5285592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6c8d90c86bd1d6098803b6451483b1fcb03dc71a866b6013e6d43a7c1ede501`  
		Last Modified: Wed, 04 Mar 2026 17:50:06 GMT  
		Size: 14.4 KB (14361 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:f81414c049fe0d5f7ff56059591f463a84376b59706fd295f64bb7fffea18ffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.0 MB (244026303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f1d69a0f06e56ff71e33f2643e6c22ecad161d51853e73785889bb318ef525f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 17:55:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:55:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:55:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:55:20 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:55:20 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:56:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:56:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:56:17 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a48df0a1a5f52547a7518f52873d8ef8fb8e585eb341c3fd741361b7020d6b`  
		Last Modified: Wed, 04 Mar 2026 17:57:02 GMT  
		Size: 133.0 MB (132997810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fabf17d5d49facfa1f89b9d96f70244960dc1049f9b9093027f70c3635c72b5`  
		Last Modified: Wed, 04 Mar 2026 17:57:00 GMT  
		Size: 77.4 MB (77427632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959683af44ffb56764a2e72e7e9c5bdf3a1328757a5a1cc6e8544613b54a8065`  
		Last Modified: Wed, 04 Mar 2026 17:56:57 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:68f755906dc2621df5d08c0ec969df1f751e28ca3b3477c8bfb167c9730f6dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d77645704ac9e36a8db6165478fcbc56c0dac0c25b7af0eeb632687ff3310a`

```dockerfile
```

-	Layers:
	-	`sha256:b709417414066e853cb44c088b003edd4e3eae230d8c47d9f5530c8d361e69a9`  
		Last Modified: Wed, 04 Mar 2026 17:56:57 GMT  
		Size: 5.3 MB (5282961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e892836e7ffea1fdaf1653ce7b3c271b1c98dc1cce1a9ca48ccbd1a8321d2323`  
		Last Modified: Wed, 04 Mar 2026 17:56:57 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:9c6100fc8043b675c29155d6ab1bb526fa3eada5e744140ec71f54b91360e37f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.4 MB (229384534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:937d46371c43db762ec28390318a17b54e3cf6e289396eede702277b65ca4d11`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 17:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:48:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:48:05 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:48:05 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:48:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:48:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:48:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced6ebfafb4648effdf9c50b1f2ce7a16be2d246533a6ba5c77a07ae2e7abe8d`  
		Last Modified: Wed, 04 Mar 2026 17:48:49 GMT  
		Size: 126.6 MB (126562023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fc30d1936bca7fcd262be9b98750549ecc6f0da6c4bfbed9ee563e5d1f097f`  
		Last Modified: Wed, 04 Mar 2026 17:48:48 GMT  
		Size: 73.0 MB (72983688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553ebdd07583d625b2e72de89a8506b782d2d9252bef5f6cc460ac13b07dc771`  
		Last Modified: Wed, 04 Mar 2026 17:48:46 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:72ada2917c223c55f5bab0bcc84fbaf2727af0c30d1f72eeb2f956354c4cc274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e6c75b7ae95cc702ae76abc8e01426a0b01c1c369bdf5adbb3dcec97c913035`

```dockerfile
```

-	Layers:
	-	`sha256:f3539865086ee8292b3e4fdbdf718847a967fab799c498bfa86f5d1b2f250236`  
		Last Modified: Wed, 04 Mar 2026 17:48:47 GMT  
		Size: 5.3 MB (5275133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:234e4b769570046ce43536eed48e31df1c47ce4479f0a32198a6303e9dbdaefe`  
		Last Modified: Wed, 04 Mar 2026 17:48:46 GMT  
		Size: 14.2 KB (14243 bytes)  
		MIME: application/vnd.in-toto+json
