## `clojure:temurin-24-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:8155a95f16a3fa7f2c4e24d3a4eeed4e2f4a76761d13f252a8aaae6fe9b7d613
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9faf9b07579fa65be225263c5b1ae57ebcbc124f89f562f1b83783cd8c8bc247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.4 MB (179383320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88112441cb2f8fea4892d0f3c059f584d042553b9dacd5055564a9deb513e8af`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3e41ca17193bcd7630e4dd210602930b1f94464bdd59680bbf6654206f7707b8`  
		Last Modified: Tue, 12 Aug 2025 20:44:40 GMT  
		Size: 30.3 MB (30256118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d22a7bfee203ce2dc886b6addac184161a053c956642f2b8efe28a208a8345`  
		Last Modified: Tue, 02 Sep 2025 01:31:24 GMT  
		Size: 90.0 MB (89975181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95826f5bcef9316fec6d3911584c0626f427663717aa135396e1184c36facf23`  
		Last Modified: Tue, 02 Sep 2025 01:57:09 GMT  
		Size: 59.2 MB (59150980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f407f34d503ce97b63197db4f93a0f8d9200296d95d7cbd3d72f71be86dafdb2`  
		Last Modified: Tue, 02 Sep 2025 01:01:09 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed16cd233e5f74cdd10b66a037deeea326c7016d8ec2b4f3216bd6e4ee9edc2`  
		Last Modified: Tue, 02 Sep 2025 01:01:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:300c0c9198272c4717823eee389dcb07921c279cd8eea05bd18f1446a1fa87f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5274586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f59f5b11b9173f78b6b60cb2c199cd974e33bdff8f3972aafdc0ef8661e95d`

```dockerfile
```

-	Layers:
	-	`sha256:1a0ebe26977de37fb1dda5730eefb5325ea89e5ecb26b33e10ac62bcf9bc82c8`  
		Last Modified: Tue, 02 Sep 2025 03:43:17 GMT  
		Size: 5.3 MB (5258715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c4fb4f7e799b70adc60812dd09c32fa3e8c85777f20668748c831798d972131`  
		Last Modified: Tue, 02 Sep 2025 03:43:18 GMT  
		Size: 15.9 KB (15871 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:35cbc2a5f3089e6f1a2a0243ed00dbc10cb5698fbd4ab14f7d66c2351cf68202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.1 MB (177126787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f01446a69ab3042266a45a60444c28827ed8b1fe96e53dfcb682560dc13e1c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b99ef417bc3eb3946e7b3162f6c19dbca1039f3b4124deb116c3a0ab763e65ad`  
		Last Modified: Tue, 12 Aug 2025 22:33:30 GMT  
		Size: 28.8 MB (28750491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba3d12b45d8e4d10ca991b219a355a4f41aa2138be3962b8523e2c567bbad12`  
		Last Modified: Mon, 18 Aug 2025 17:22:57 GMT  
		Size: 89.1 MB (89092530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ce8291cb6da479ecf2794d0edac57bb44e1bba4183d73735cf0efdb865748b`  
		Last Modified: Tue, 26 Aug 2025 17:56:31 GMT  
		Size: 59.3 MB (59282722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c220821bb44b632af169e4c410d2b9b5c54af258ba94af362958dffe319d1e31`  
		Last Modified: Tue, 26 Aug 2025 17:56:26 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82de7962cc0362c08d3e3829fcad71743f2137bb6c7c372984bc8362e866ece5`  
		Last Modified: Tue, 26 Aug 2025 17:56:26 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8eaf7e4ada130195cf3604c08869fcd449e4369138f1f3b3bae7ec1dee4c8298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5280434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8533512cc2fabe427a7e83ca251d6848163e27f4dd42478871705f18331eceb5`

```dockerfile
```

-	Layers:
	-	`sha256:65c7e220f86e35e82fa3e668f9ff0fb823cbb8efc703519f11ba679fd47aa0c6`  
		Last Modified: Tue, 26 Aug 2025 18:42:39 GMT  
		Size: 5.3 MB (5264444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce1e1432ffb916bab81b897fa1c48eccf951ffa0a80877abc4a0576488d3c010`  
		Last Modified: Tue, 26 Aug 2025 18:42:39 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json
