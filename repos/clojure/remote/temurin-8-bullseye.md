## `clojure:temurin-8-bullseye`

```console
$ docker pull clojure@sha256:2a4be3171f7a843219430332ab10794efac830b78e04c82be5f32b01721e4d0b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e83f621dbec18fdc07919ff059f6c7389f8383fff8fec504e84120f1ee79680c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.0 MB (178043834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597f69df794f4d603ba90db9b6018a0ecfd0db1a7cc99a511453c9a317314d13`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:035115815e46101f9c9956e02e706f2f3ec8748e2b415f0d232b51eb76a6a779`  
		Last Modified: Mon, 08 Sep 2025 21:12:56 GMT  
		Size: 53.8 MB (53755396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c9624669f7aa5bee8dedaa10346f464a0e29df49f955e6ba47c900935af2e7`  
		Last Modified: Mon, 08 Sep 2025 21:41:58 GMT  
		Size: 54.7 MB (54731308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d8aeff026e516698c10e59361c264131b3a5534afe9f7afb80d91935c1965e`  
		Last Modified: Mon, 08 Sep 2025 21:41:58 GMT  
		Size: 69.6 MB (69556486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8770a51b093b9500023064085e84858dea5d0e6b7dbb1aa0ecbd9ee3cda5e0f8`  
		Last Modified: Mon, 08 Sep 2025 22:59:58 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:74d089ba563deaf2672257ed881d68b247d2077b91d2dc329e97b4203ca7bf65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7531514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:202b75b8ee86525dd8128394c5c48fc8675a845ea9441d4f2e0dac8184ff91a7`

```dockerfile
```

-	Layers:
	-	`sha256:48104e421502ff24f626c253bdabdfd4e48845cf7ee4418eaacc42753edd450e`  
		Last Modified: Tue, 09 Sep 2025 00:45:44 GMT  
		Size: 7.5 MB (7517277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfa58c6a3606780718b969483333af40578652f484bcf1e721ab713ff76b8d1f`  
		Last Modified: Tue, 09 Sep 2025 00:45:46 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:be0a2c9db7d66a179eeef6cb7f35775fe9d34bb281025cf457af471662171d65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.8 MB (175768644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ab03ebddedabe4b5bc5ac27c214e8a2a442a8d688d8d51a5d844d2b7c7f4b6`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:7b68ea47bc3cd8615e51fdbe0976cb4999ba56ce8764e755543a4521d69a32f6`  
		Last Modified: Tue, 12 Aug 2025 22:08:57 GMT  
		Size: 52.2 MB (52248409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2989b905258edd2f0f329af9cd9a2939ead2ac1d72fc9ea5d2106f5e2ecb42e`  
		Last Modified: Tue, 02 Sep 2025 07:35:06 GMT  
		Size: 53.8 MB (53835656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22182ebdb579846aa28169a704446339aeb6339f14a2af0798bdcc42d541483f`  
		Last Modified: Tue, 02 Sep 2025 07:41:04 GMT  
		Size: 69.7 MB (69683934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2673a86a8f12de1073b98f5a11b903abac3fe78eb552afec9877bbe4430425c6`  
		Last Modified: Tue, 02 Sep 2025 07:40:50 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2efea8f33b648c4be61e3110873d27f471214622fbe1bf3821d0820eb844cd3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7537429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e25957ffa1168d20d3de59b885431a8c406821daa5ad3ead195346fd793611b8`

```dockerfile
```

-	Layers:
	-	`sha256:e0a47da361577e622ed1cf1f0d7274a9f0e2dbc922324ccb88e7fb44a5df18b5`  
		Last Modified: Tue, 02 Sep 2025 09:44:26 GMT  
		Size: 7.5 MB (7523074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3d1dc2cca8c015f05fb782db9d33f35d189ad8bf28366f6bbdd7a9f5df07cd2`  
		Last Modified: Tue, 02 Sep 2025 09:44:27 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json
