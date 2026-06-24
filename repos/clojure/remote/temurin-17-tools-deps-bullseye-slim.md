## `clojure:temurin-17-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:239e9c213a01247dd0e36ae0ee8f2368b9b9c6e9d456950a8b74cca8e9654d7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:761cc0e407436d6b6c631d6487aa388b9ecdb31d27f5f55c6e2fdcb9bf77e6e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232266219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b03c2c56a66a8843aff555d222052c04d1a0e83ff4f5989a4f510e6830dfcf54`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:18:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:18:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:18:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:18:02 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:18:02 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:18:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:18:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:18:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:18:14 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:18:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0251c4232e4025b51352f0bb7119fd866d4a6a62861f09baea6fe5af4c6eee59`  
		Last Modified: Wed, 24 Jun 2026 00:28:14 GMT  
		Size: 30.3 MB (30259447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68893c4fea8ecf7be8ba86b19462db09c65fc194cadcbd05463cdf3da04fcb1e`  
		Last Modified: Wed, 24 Jun 2026 02:18:37 GMT  
		Size: 145.9 MB (145905427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f71d65de36725b9f541a7233ecf81a77c3fee7f736b084fe2be9b1796ded4e`  
		Last Modified: Wed, 24 Jun 2026 02:18:35 GMT  
		Size: 56.1 MB (56100304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a78069e26cedca2418033c9f85e16af93692470735bfe1071831646095a9b46`  
		Last Modified: Wed, 24 Jun 2026 02:18:32 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e70d117598f27e51b865bbbe89d99576236ffde6ce9a35b2ef14d2205b4ef5`  
		Last Modified: Wed, 24 Jun 2026 02:18:32 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:17dd9d8780d0ea34817ad8d6eeadbe7e047a0d3e9f61bbb3093df3628e41eb70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5333839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0605ff727522515285c365f55a9bded0794253c5cadb3980b50b337bf8b9433c`

```dockerfile
```

-	Layers:
	-	`sha256:5bfcca35264d7db41c27fce3ba6555033b5adbed4de7128abd4545a47e560f71`  
		Last Modified: Wed, 24 Jun 2026 02:18:32 GMT  
		Size: 5.3 MB (5317849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa51eaf947a276b66bb069212650a1e35469b40e0ed7f4e87ddb81fd2232d2bf`  
		Last Modified: Wed, 24 Jun 2026 02:18:32 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:97bc0ea0cb6481da69c33068b7b376727520f8a893b8acbe7fa348bd71a93344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.7 MB (229739990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24191403fddc5b34f4f62cdf5ee57ef045eb7cb39546769196112c729ca8a149`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:24:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:24:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:24:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:24:47 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:24:47 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:25:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:25:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:25:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:25:00 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:25:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:58009b48fe731a10341c4f5f98dfa280afd10fa34cc71961411d37e306120dd0`  
		Last Modified: Wed, 24 Jun 2026 00:27:56 GMT  
		Size: 28.7 MB (28746926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036aeadf354b4f3f838c1c1f47b43c9d198f7cb8f22187fd0d5497db453f4a30`  
		Last Modified: Wed, 24 Jun 2026 02:25:22 GMT  
		Size: 144.7 MB (144724312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd298031fd15dc126dbd17b97d64265ba43359a53c8b9d9b0ee56c8d46da843`  
		Last Modified: Wed, 24 Jun 2026 02:25:20 GMT  
		Size: 56.3 MB (56267711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3702d66d8f587be925131f74cc743f224c5606b8d4c7cb3d37932975f872ae9`  
		Last Modified: Wed, 24 Jun 2026 02:25:18 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e91a62f99918f78fda58b3d5459034987d5fbf2a33972fcd644c3dd8a4d5ff`  
		Last Modified: Wed, 24 Jun 2026 02:25:18 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b59d3f05dc9c3d1e35478af56dccdc27baafd25b8e9d46c5b2dd79f2a2977b21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5339689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000bea4ddac40225ff49bb896ed489e47fe9171c99ac7c424496f1f517e3a041`

```dockerfile
```

-	Layers:
	-	`sha256:2468ba59017d6a26ca8f58e049f46a3e9fa163bf685717d4a1299ffbd92274c5`  
		Last Modified: Wed, 24 Jun 2026 02:25:18 GMT  
		Size: 5.3 MB (5323581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0dac6e6cf9be38a82eb23b75f29fee743e39cefe93d3ff9025197cb9dff22ea`  
		Last Modified: Wed, 24 Jun 2026 02:25:18 GMT  
		Size: 16.1 KB (16108 bytes)  
		MIME: application/vnd.in-toto+json
