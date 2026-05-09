## `clojure:temurin-26-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:f899889a803d46ee6aef3c497b07e0be20bdce0d27ec1f4be362d4d6e0ccfc0e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2c09101f2c90ca2f60009eb044b7a9d66d1eee5de9ffc77223df02742a11e2e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.9 MB (183900982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce7165819d3844335d7d7b3a1bf3edf36e63f9f11c9f5567c5a7cfd49f1b039`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:20:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:20:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:20:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:20:38 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:20:38 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:20:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:20:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:20:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:20:50 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:20:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:77e30ef52aeb52d8466baf0f50b54ed2fc0b421f44c49e5bf93682b27110f4d3`  
		Last Modified: Fri, 08 May 2026 18:22:59 GMT  
		Size: 30.3 MB (30257958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb5f8c26c50be51544b0c360e97e359c12a76505e1620cf1095dacb93bbf1d2`  
		Last Modified: Fri, 08 May 2026 20:21:10 GMT  
		Size: 94.5 MB (94455681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d682fef4e39a2a77da906b77aea664082761dd4536f28331e3fe17a8b7d76a28`  
		Last Modified: Fri, 08 May 2026 20:21:09 GMT  
		Size: 59.2 MB (59186303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769b2e26d3becb45acefff376d8b2feea6a6267a822130c01de0b7fc7c283176`  
		Last Modified: Fri, 08 May 2026 20:21:06 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6049eec1487490bda3b277ef83eb0f3a57441cbad7bd3216fb102a1c1659187`  
		Last Modified: Fri, 08 May 2026 20:21:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f4c069f83498e35b27b44221264216b73b7422a6d739755a34417c42c86becba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5301386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40cac2f1a1e2663252d2b16a98a78d4b1a9d3a743fcddfb190e4ea67fa7ca757`

```dockerfile
```

-	Layers:
	-	`sha256:f37338e6b75172ebab2636dfd55474ae13f78702c46d0a1ab9929325ae7caf16`  
		Last Modified: Fri, 08 May 2026 20:21:07 GMT  
		Size: 5.3 MB (5285557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ab67e0ce3f0e2e792ca2017675948430f9d6c646b82eb4d33975ba8fef5dc6e`  
		Last Modified: Fri, 08 May 2026 20:21:06 GMT  
		Size: 15.8 KB (15829 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:acb75ee7b2f4db8ddd3c670e78d4fa17d458b5c67110c9f5f456bf4680587558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181469972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae36e249367261ebf30b13c9d938b04d18440e113f92e0c41abb774576a19cd0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:25:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:25:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:25:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:25:10 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:25:10 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:25:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:25:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:25:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:25:24 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:25:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ab0f13d792ff9100407906fb422a0b62a8b437abde4c245e03f0366814be9aae`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 28.7 MB (28742591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b261516367299a67e228c57e4e95e380e4630a31b90ad797127d875b167557`  
		Last Modified: Fri, 08 May 2026 20:25:48 GMT  
		Size: 93.4 MB (93395168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b20ffc23ab630d2b8783377a075b39c87a3c24bd9390497359efc2fd8b05bbd`  
		Last Modified: Fri, 08 May 2026 20:25:47 GMT  
		Size: 59.3 MB (59331173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff0d4f094b85a77981a978ac1c542e0912090b6846bf73a2a4dbd7154973baf`  
		Last Modified: Fri, 08 May 2026 20:25:44 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c58c755ae069d1db3f45bb410317d392ea27f28fb1c9f7f7ff5388fe085e08b`  
		Last Modified: Fri, 08 May 2026 20:25:44 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:51c0a0bd299669e2eff7fa1d3c6f841fe71a6c7e58fedf9591420726978d2e40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5307232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dda03f710e45dc8ca8dea1abbfd44c8291a2a28b1ba96c7355f632c867796ce0`

```dockerfile
```

-	Layers:
	-	`sha256:d79a3d0ef31c801b3b8fac5e4b061c30b841df68404cd2c634781b3ee12151d6`  
		Last Modified: Fri, 08 May 2026 20:25:45 GMT  
		Size: 5.3 MB (5291286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81c89266ed3fd43e9643e838265e1f1708493e7a24b09ed27ac738f18cfdd96c`  
		Last Modified: Fri, 08 May 2026 20:25:44 GMT  
		Size: 15.9 KB (15946 bytes)  
		MIME: application/vnd.in-toto+json
