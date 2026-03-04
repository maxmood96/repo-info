## `clojure:temurin-8-bullseye-slim`

```console
$ docker pull clojure@sha256:79d0eb566642bd97f9c242a17adaa4d2ec10d4f7bb73dfed67c856864d1262e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:db223fe81ad593f6c3ea3bf5b7c8231aa12a4280a3dae03432c6992c61c6055d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144612408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd9549e4e05e3a41795bf0ce9098e33596b0950bc2eb8246294893b2bc52fda7`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Wed, 04 Mar 2026 17:48:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:48:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:48:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:48:54 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:48:54 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:49:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:49:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:49:08 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:34f0642d22440b5813561cd4375937013bfb556bec8ff3b0e208699b786282a7`  
		Last Modified: Tue, 24 Feb 2026 18:43:06 GMT  
		Size: 30.3 MB (30258379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a2029a0aa632aab8eb51aab50408ede9fb5bfd9e63283d5857ac878e8c7918`  
		Last Modified: Wed, 04 Mar 2026 17:49:25 GMT  
		Size: 55.2 MB (55170059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428c84ed15463ecdc430ed8bbefb1e0dc025daee1f710184eae939f1efe1f1fa`  
		Last Modified: Wed, 04 Mar 2026 17:49:26 GMT  
		Size: 59.2 MB (59183324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3bbeed703beebafbb461c16d7825d694c72da2dc5b126ed3b8b7272eee604be`  
		Last Modified: Wed, 04 Mar 2026 17:49:22 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7f90a0670f8a28158a1df875b7d7c03970139dbbd70b284934289cf6016a2ffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5456912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:409fb58a28e79a24675960321c707598ab0443eb6f588d20a1a4f9369c5f917b`

```dockerfile
```

-	Layers:
	-	`sha256:0618c1cb7571a45b1ff8d06ed3f25b5df4b08ad78fd6f68bfe411fbe74a52ac3`  
		Last Modified: Wed, 04 Mar 2026 17:49:24 GMT  
		Size: 5.4 MB (5442664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c786c07dac49f9563a4753c289a0fddcfcbe42460574e96956a9c9dc8b9f270`  
		Last Modified: Wed, 04 Mar 2026 17:49:24 GMT  
		Size: 14.2 KB (14248 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f840b45bd53aae891899c848442ac823f55378e4e54e77c245754376d9bce73d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142319958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6effbeab026fbbdf214d8707dfc60d39ed64d2bcd663a650690f89bdebb4109`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Wed, 04 Mar 2026 17:48:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:48:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:48:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:48:17 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:48:17 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:48:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:48:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:48:31 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:018c0693c4a2532e5636d6115333db6d882da8f33f1f40cb3e88dbe62da21aac`  
		Last Modified: Tue, 24 Feb 2026 18:42:36 GMT  
		Size: 28.7 MB (28744470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f7c639ff2dd9d7394471d49c167964e28dfee8c523368012f195fb1bbc5ebc`  
		Last Modified: Wed, 04 Mar 2026 17:48:48 GMT  
		Size: 54.3 MB (54251612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11d29c12c1d173f82f8a195293bc19cfc7979f07aa71688d07e0ddecb092b24`  
		Last Modified: Wed, 04 Mar 2026 17:48:48 GMT  
		Size: 59.3 MB (59323231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88b5f9ee6f13a144f3652eca66dd99ec3cde6d36edb8606640239cb528cd363`  
		Last Modified: Wed, 04 Mar 2026 17:48:45 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:12a7c1c816cc7c06e94f52b0ff2e5781bd192a6c42bf05d261ef43faf97fd77b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5463460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4e12e789daaefe893cdfa9b0284618f02ce14fa148b85491e8c8a38cd40561c`

```dockerfile
```

-	Layers:
	-	`sha256:ef4add7c138d3dde265748fcea91a280063942d431eb9741935baa9db9f26c14`  
		Last Modified: Wed, 04 Mar 2026 17:48:45 GMT  
		Size: 5.4 MB (5449096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efe250544016add0fc73bc4d4eeed48233a5236604e911e2eef53b5525e306b2`  
		Last Modified: Wed, 04 Mar 2026 17:48:45 GMT  
		Size: 14.4 KB (14364 bytes)  
		MIME: application/vnd.in-toto+json
