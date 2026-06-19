## `clojure:temurin-26-tools-deps-1.12.5.1654-bullseye-slim`

```console
$ docker pull clojure@sha256:dac0ac481112ab321cd0f61a8954649241ec25efac13183b4f1e1efeb0dce87b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-tools-deps-1.12.5.1654-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4abb11a144e050cecd6d6601c437b4e3b2be41d5488c785a58aa988c5dadc12b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180885868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06c85e226b552ffd96d292fe65f7593decff9c7c7032c4168a93b7bb44af11a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:21:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:21:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:21:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:21:54 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:21:54 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:22:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:22:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:22:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:22:07 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:22:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:55534d9909ecd18467599b415fa2553c3106849154ae8a361a75f1a24f2a4364`  
		Last Modified: Wed, 10 Jun 2026 23:40:12 GMT  
		Size: 30.3 MB (30260255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bdaf2a27cd127e5ec226532e9fc5591369d8d3f9fe39eec4c753f26455ca7be`  
		Last Modified: Fri, 19 Jun 2026 02:22:26 GMT  
		Size: 94.5 MB (94524351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6502c2d1c6913f5cd5aeba06765df0bf5749add6bdd041ddde1a2379209907cd`  
		Last Modified: Fri, 19 Jun 2026 02:22:25 GMT  
		Size: 56.1 MB (56100220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22cf4f492b13c85ae6f9e9d81a93f1e20064177344f9ff67555b57889b0a2e3`  
		Last Modified: Fri, 19 Jun 2026 02:22:23 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7718915a6211f061b4da3fcb84cbec19f9daccf0e0a8e18a256fbfa8103e4c2d`  
		Last Modified: Fri, 19 Jun 2026 02:22:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1654-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2159ac1ae6b02988ce57bd9f5647f1f7fe71d6d33b992435ff225d5e13c5acf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5300346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac570ace2c5c0d45dd49e7eb6f69180710321b1819773d484dd3a83a62916329`

```dockerfile
```

-	Layers:
	-	`sha256:5bdeddc6748e0f446782d165709dd1fac4cf067b05c46aca1c3bcec495041a9b`  
		Last Modified: Fri, 19 Jun 2026 02:22:23 GMT  
		Size: 5.3 MB (5284364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64e7dd60d121698fe3d95486d46cd08d6286a5d261bc79298aa645bf0e5c8d40`  
		Last Modified: Fri, 19 Jun 2026 02:22:23 GMT  
		Size: 16.0 KB (15982 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1654-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0af472c97350b5fb202e56fef25cd878003318b3a7667a1554dd4a5040a02089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178519236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3db24f7ec1d01b127e5d7378aa2425d0bf5abb33f613a38480b34dc11b363e1c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:22:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:22:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:22:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:22:17 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:22:17 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:22:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:22:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:22:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:22:30 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:22:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ca483a18241c226a06a4a4afd22dc5496062254c671fa595136458fb8fcd0107`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 28.7 MB (28746154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:285d7283252d58c3a50918d5ddfef125d5498d11f5d4ff6b037d8a3d3b8885f3`  
		Last Modified: Fri, 19 Jun 2026 02:22:52 GMT  
		Size: 93.5 MB (93504358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0197a538de23b33e0a862f7c8cc5b4a2638842ff0f0cabaa0ec0241d8c00f4e0`  
		Last Modified: Fri, 19 Jun 2026 02:22:51 GMT  
		Size: 56.3 MB (56267682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586fc6096f963276a0460ff2c7c1b1ab3b2822aba626b801942c0e3eff031021`  
		Last Modified: Fri, 19 Jun 2026 02:22:48 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8abf01e8a6933ce980d322ea25acbfcffea0745cb5254ab86c314247eaecca`  
		Last Modified: Fri, 19 Jun 2026 02:22:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1654-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:95deaf811398f3167b66889073c7223d44a9564d9d21e6adc540208f63c6fa14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5306194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d917f08da6e6af090ba3d17cdfb3af641ee22212cfdd2809001fd41e198f8555`

```dockerfile
```

-	Layers:
	-	`sha256:e3e459e0e26fbc120d621439fea498f1d66b0bec3f07fc3d22aab7bfc3cf28bc`  
		Last Modified: Fri, 19 Jun 2026 02:22:48 GMT  
		Size: 5.3 MB (5290093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:946bafc0dd06780d34cb9bc565c5a553501e0dba15e740adccdfc1d9bec3840d`  
		Last Modified: Fri, 19 Jun 2026 02:22:48 GMT  
		Size: 16.1 KB (16101 bytes)  
		MIME: application/vnd.in-toto+json
