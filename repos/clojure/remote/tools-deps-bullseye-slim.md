## `clojure:tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:252897c4e647fc1a6b9b32d380371afd8e1cd04fd95ae5f62f8d72547b4f02d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:71bac450dafc8fab932e988b7ca1878322f0fb0f99d59de05aebb9442980da13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.0 MB (182024150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb5ec876931a0913300abfed9be1641b7792619194c995dd8e74bd4d962f8a70`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 15 May 2026 20:16:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:16:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:16:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:16:05 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:16:05 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:16:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:16:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:16:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:16:17 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:16:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:77e30ef52aeb52d8466baf0f50b54ed2fc0b421f44c49e5bf93682b27110f4d3`  
		Last Modified: Fri, 08 May 2026 18:22:59 GMT  
		Size: 30.3 MB (30257958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcf4fc49793fc77cfd7cc2ba4aea1a4c8d28483d701d14e37aa3afb7cd97eff`  
		Last Modified: Fri, 15 May 2026 20:16:38 GMT  
		Size: 92.6 MB (92574588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba74cbe10f73730c67624990eb041d44ddd306e2eab07bf5d5d7a546a594353a`  
		Last Modified: Fri, 15 May 2026 20:16:38 GMT  
		Size: 59.2 MB (59190558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a86263c0a2f9b82de9f323734386f74e6270828876d7c5484ca1e2969cf1a67`  
		Last Modified: Fri, 15 May 2026 20:16:35 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647df0eb94b48d054c4ec75eb9046b04f38054293dc99623aaf0eff7abee4ba6`  
		Last Modified: Fri, 15 May 2026 20:16:35 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:38ad33105b0e6b1b2b609c0837f0697acd16732723a9262844a5147b21cb15a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5305447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95676839a85db22dbd5253faf56714ff864f07539de9db63acb0f28ddcc7851a`

```dockerfile
```

-	Layers:
	-	`sha256:462542e92fe9ae413f79c4a96e7e838fe1bb35afd06f0252c50c167768408c14`  
		Last Modified: Fri, 15 May 2026 20:16:35 GMT  
		Size: 5.3 MB (5288768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25dfae19dd950bc925436d9b8596752705e157c081f41c016c3e93188325d17b`  
		Last Modified: Fri, 15 May 2026 20:16:35 GMT  
		Size: 16.7 KB (16679 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:48ad7a411680c8cf0112c3846ae9a4c16c946e22c409093875eee2e34a50f43d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179645868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc65af12c2aa42f979f852de92a1ce591817a29b78316c5e77529e6033aaf720`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 15 May 2026 20:16:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:16:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:16:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:16:09 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:16:09 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:16:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:16:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:16:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:16:22 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:16:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ab0f13d792ff9100407906fb422a0b62a8b437abde4c245e03f0366814be9aae`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 28.7 MB (28742591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d7bb6fd16dd3fee9b84d122f4547eaa57b1425b041faaebf1e6d801a4309b7`  
		Last Modified: Fri, 15 May 2026 20:16:44 GMT  
		Size: 91.5 MB (91542260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40512b02454dbc5ac46dbd15d2f00e4f9616ccd378a7bd785b7d77bad0a2d750`  
		Last Modified: Fri, 15 May 2026 20:16:42 GMT  
		Size: 59.4 MB (59359973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6436a6002c59a4984c18078381c7195e8aa807fec798e6100ff8c2a20c2afaf5`  
		Last Modified: Fri, 15 May 2026 20:16:39 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98c9350183293aea70f2193ce7a10648be4615063d51df68afbbda92aea3183`  
		Last Modified: Fri, 15 May 2026 20:16:39 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e55867e5e6cc12de31a5b338352bd51ac4858de618f91f336d3424df390f772c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5311342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc98a2926321509222dc37e7ca45d9494fca55f5ccbcfabf8514396a0be9e5b`

```dockerfile
```

-	Layers:
	-	`sha256:7a59f2e1a1f0c0940109264067f7f0c479f6b2b2f4cf84056a70ea2b71a0d3db`  
		Last Modified: Fri, 15 May 2026 20:16:39 GMT  
		Size: 5.3 MB (5294521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fde4624caed2e28ba7915783723f3fee67e67fdd59f1ea483c6805b9b799fc7a`  
		Last Modified: Fri, 15 May 2026 20:16:39 GMT  
		Size: 16.8 KB (16821 bytes)  
		MIME: application/vnd.in-toto+json
