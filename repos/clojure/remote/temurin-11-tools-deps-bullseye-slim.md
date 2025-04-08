## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:157bf3172bee8b2711d144639e2b51c37e5f23f24ae09174317cbb2f76827853
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:15de8d3c425756121c59c90f1c249960a8d46e31b529ebaa452ad49a849a120b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.8 MB (234849910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a9afcaf2f39006aab064183d5d75cb9f7a17583a0c9bb29dd36ee3bc1166d6`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3f6ce8b073e7eef71039f57ae204d4e8c775628be068575fb8d98c6f685bc4`  
		Last Modified: Tue, 08 Apr 2025 01:35:50 GMT  
		Size: 145.6 MB (145598939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9acada818cc701bf9217724c77512e3728c93247b655ce98f6a58985587857`  
		Last Modified: Tue, 08 Apr 2025 01:35:49 GMT  
		Size: 59.0 MB (58992907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709725af712c6d312a9fd4c543a4919e0e3669a787ea927176595604359d965d`  
		Last Modified: Tue, 08 Apr 2025 01:35:48 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:73df2e3561fa3f97409ccda2a3321846113ce8b55bdef58ef900f5b2f4dbbc6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5153464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33871ab3fce16e2e861e3cde32adfadfc0f00cdc51b09e68288e2f8226dcde2e`

```dockerfile
```

-	Layers:
	-	`sha256:ad0b079b8120d1454c3cd15571557d5e80e95143e136efa7f812b6b0fda6019e`  
		Last Modified: Tue, 08 Apr 2025 01:35:48 GMT  
		Size: 5.1 MB (5139154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcb8a7e6cb9c4472f7952e073450d7dea0f384c6a58ff22ea46c1178570fee82`  
		Last Modified: Tue, 08 Apr 2025 01:35:48 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8ff196859ba4194562b4aebb5562f34cc20912791088a6b13b3dfdcbfd991eb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230262898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b683da63dafc995e7e1dc8015c4fc6aaf321759f94bc550c3cc6bca1e8bbdb00`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf8ee5f30067fbb13dc02b5c95f0d82b9ae43d756a8328e00639676b8265d57`  
		Last Modified: Tue, 08 Apr 2025 06:33:49 GMT  
		Size: 142.4 MB (142385396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1145fe300994298c0b049a81dbb042957133a4da7a9d46fbe1af77a58ea10ea`  
		Last Modified: Tue, 08 Apr 2025 11:24:45 GMT  
		Size: 59.1 MB (59127359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd3b0d97926f48800192ec36d1a72e9313ba5807494bcc605fb6d89e8b6bb52`  
		Last Modified: Tue, 08 Apr 2025 11:24:43 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c4433410b6d87fe391f08bd492b0b2b349d52ca423b07dec34513488041d54b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5159930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f4041777c03f697c6e390965e740e8f89d329cc4cc0003502a355ae3231f13`

```dockerfile
```

-	Layers:
	-	`sha256:572d8ed9d7239f40a64666a2a0dfff84e2bb6479f7c576ae67be1b545aabb332`  
		Last Modified: Tue, 08 Apr 2025 11:24:44 GMT  
		Size: 5.1 MB (5145504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0a22742121f90de8da96abdf9c1420df3597ece6c09c6eabe32132b3e7ee669`  
		Last Modified: Tue, 08 Apr 2025 11:24:43 GMT  
		Size: 14.4 KB (14426 bytes)  
		MIME: application/vnd.in-toto+json
