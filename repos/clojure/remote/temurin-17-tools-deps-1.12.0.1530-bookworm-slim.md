## `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm-slim`

```console
$ docker pull clojure@sha256:907658c3d9feae625d8255de1595a18a08b7479e66ce9ff1ffead1bb3ea9c93c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3636f9eb735f17cb178fdf68dfb9ff9a68e3f78b77dcf47080b638dcb95aa05c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.7 MB (244693124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b9a5fc6f63250f407e4ed4742b867fd1ff76d5d97e52b14df2cd11024e6d884`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:449a7edde3ba5def4eafb2b5cc6c504888b67a07a4ac78fe543654e99d9e9ad2`  
		Last Modified: Wed, 23 Apr 2025 17:15:58 GMT  
		Size: 144.6 MB (144635038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7561f6185d49a21bdc643ce0f78874875f81e04eb3836d912b57867f4a8ddee2`  
		Last Modified: Wed, 23 Apr 2025 17:15:57 GMT  
		Size: 71.8 MB (71829781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a9ad4b654d866d11060693fa95756ccfd9491d763e5351698939665f8eaba5`  
		Last Modified: Wed, 23 Apr 2025 17:15:56 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c607219778696bd96d3524e3a734a3c150845e0b5fa035a73571f511ced840`  
		Last Modified: Wed, 23 Apr 2025 17:15:56 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4b4cc26e697d1cc3c90925c0c870df074667875d1f98db4e74ba261d2a4d4bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4929844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a93c0a27382dbe121ad0af5b654aa69ee18476db8da16d9d0f96ba6f1884845`

```dockerfile
```

-	Layers:
	-	`sha256:677ae7562feb230bc19519218b4c93f39b65cec6aaac81008a7de6786162925c`  
		Last Modified: Wed, 23 Apr 2025 17:15:56 GMT  
		Size: 4.9 MB (4913965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0cc43c5c7bff6d931f0810c329a292a80f1549f4c13f0e994c5d57b3b39947e`  
		Last Modified: Wed, 23 Apr 2025 17:15:56 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:823111b421f9994a0056775413665a6956939625678f9ed6d1440c86b287e66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243229090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e31d3c949b2d11ec80cd9c251df2c99b58aba8b56706abeb77639b98348922d9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2fd54931494fa678d9e6c5de86eeb0e31884f8c1ac2e2974581bfb59351acd`  
		Last Modified: Wed, 23 Apr 2025 19:46:14 GMT  
		Size: 143.5 MB (143512631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23636eb4664371a518eafd7e21ab671a51e3f53054fe6cf57acdf061c403884`  
		Last Modified: Wed, 23 Apr 2025 19:50:50 GMT  
		Size: 71.6 MB (71649093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a214a1aa50c4279857e92bea3b87ab67cb3e7b3f0b6950cdaab3005485676ac`  
		Last Modified: Wed, 23 Apr 2025 19:50:48 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ff04436d2a245f06ec370f9b9da985a33792a1bf0765a5352ba5b8f0462200`  
		Last Modified: Wed, 23 Apr 2025 19:50:48 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4ce85315360be529581d18496b9428e04932bec3a59d14af9cff00d6372b967e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4935723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0ea3c37e9c08310b255d3ef0baa73c8fec205e224f150b4fb14fe7721587d12`

```dockerfile
```

-	Layers:
	-	`sha256:5fd4226389113cbfd684f330dd635af70df290ca8c320f9bdc4c6c9652057371`  
		Last Modified: Wed, 23 Apr 2025 19:50:48 GMT  
		Size: 4.9 MB (4919726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0636d7860183d45f030cf5b99212f1e80e835fb6a96da87a875d32be92fb0f4`  
		Last Modified: Wed, 23 Apr 2025 19:50:47 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
