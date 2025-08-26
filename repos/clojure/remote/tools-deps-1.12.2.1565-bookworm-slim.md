## `clojure:tools-deps-1.12.2.1565-bookworm-slim`

```console
$ docker pull clojure@sha256:a4f93ac0c6278ceb8048dfc700aca27eac863a05e6eadbde4d6c232a642dc460
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.2.1565-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:efc8b485c51857acf9c5a02daf795e15753abe245ee340b2e04b81c42ea0da23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255712310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b36736d3fb57412fae377620f1f58045964bc5348778b255b27012a7886034f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0976a2b85d9680202b5efd21763d991db4f57a6a31baa3d2dea1f16bc33017`  
		Last Modified: Tue, 26 Aug 2025 19:12:35 GMT  
		Size: 157.8 MB (157804752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30aaf088ddf17d6501eec0ad4769c9676fe7e446d751a51e7fbc52809530b02`  
		Last Modified: Tue, 26 Aug 2025 19:12:34 GMT  
		Size: 69.7 MB (69676259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f719ecddafc2592f96b5dc33b1cf07a6838b62e451039f039d30b43df371cb20`  
		Last Modified: Tue, 26 Aug 2025 19:12:27 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281534d0f7a2e520bf96e10e77bbd34e11e770ec1fc13fc27917dbb7f21c3053`  
		Last Modified: Tue, 26 Aug 2025 19:12:27 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.2.1565-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e5d9b91d153c68014c0c1b90c52284ea07d12cc3aed06979587ea76a01908013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5131646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441c3057d0a9d35eafe59cf47a1074c1d1484ce89c7d19a6d7b64bb8ae2aa18a`

```dockerfile
```

-	Layers:
	-	`sha256:26b5e5bc27e0b8b33b47306d1626a2ec499c8accdd1adf5e41e43b1dd6407ceb`  
		Last Modified: Tue, 26 Aug 2025 18:39:53 GMT  
		Size: 5.1 MB (5115071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:496bcdc67a197a6c2f5d4a41bb9b0c90464cf5fc8a9932f2539cec9449cab14d`  
		Last Modified: Tue, 26 Aug 2025 18:39:54 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.2.1565-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b1ddff4da9f14136b35e43f633f4ce67c0cfd1cf7738bec21a0e6c5fa737131b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 MB (253713757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54b3dd1001816565ce3b1bd8359e765dbf2c868dc6a367920985ca2ac64d1dae`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7991a92c7ee87da171852566b076064998d9091210c9e1f68f8874a4a0f1ef`  
		Last Modified: Mon, 18 Aug 2025 20:51:19 GMT  
		Size: 156.1 MB (156081253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c4c2836ef9b52981af34c11d65eccc77018a2c40dad9c8bc696ee34faf28da`  
		Last Modified: Tue, 26 Aug 2025 17:48:34 GMT  
		Size: 69.5 MB (69549460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf06219a6f05ae84a8a8a7f7840eeed8cceb5ada0bc6e16dd01ad1016d386aa`  
		Last Modified: Tue, 26 Aug 2025 17:48:28 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1509569a08fd6fa13b26d5bb128d1de6ea7a482ed7b966773136816cd2b1ee1d`  
		Last Modified: Tue, 26 Aug 2025 17:48:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.2.1565-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:541430df0486c295ce1e8e8a2f135a067095af52f0235e7707a7b1cb5478a244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2c6b277f3f98866e145f82a268e1e7682c793964114c055766b23deddd6872`

```dockerfile
```

-	Layers:
	-	`sha256:74307c93ed0102f47d33dfcc74bfd1adc55499acb3001de23fd041f3e6017662`  
		Last Modified: Tue, 26 Aug 2025 18:40:01 GMT  
		Size: 5.1 MB (5120856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:410ee0024ab2796f34b3b38687b5a7ce55e6374fa17d061273d6f71e1e873f2f`  
		Last Modified: Tue, 26 Aug 2025 18:40:02 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
