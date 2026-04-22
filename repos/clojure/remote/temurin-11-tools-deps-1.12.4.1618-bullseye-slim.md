## `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye-slim`

```console
$ docker pull clojure@sha256:1f0ea21ba51485e6f5c6f5c7dd94368d4cf4bf4cc4db1932e7bf1f794ce28eed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1b641d497a3722b4f44382a29bb8f1f18e4a29eab53d4bc34da9d6d7be2426ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.3 MB (235251362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ac803f5d47794f323c103e693dce762b6f7c3a016b4ee5155231f17078e026`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:43:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 01:43:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 01:43:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:43:35 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:17:33 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:17:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:17:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:17:47 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7263c37a27b96bd5e0c0de77a44122fc986156c49e3c82b0ba12448611753e10`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 30.3 MB (30257934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1971bdb31dd9b92c393f93fb19674ff9b70f7485b4a5f00a63d85950637fe069`  
		Last Modified: Wed, 22 Apr 2026 01:44:29 GMT  
		Size: 145.8 MB (145806794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134d6963cd0b7cb1773bbf09b6636824150d386323232a8d91b1d7b24ef65062`  
		Last Modified: Wed, 22 Apr 2026 02:18:03 GMT  
		Size: 59.2 MB (59185989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4453f0d7442332874b62dbb305384dc306f77069dfa4eb858a99328cd33bdce1`  
		Last Modified: Wed, 22 Apr 2026 02:18:01 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f94941775deb2cb2cde1e862f9172afd2728308049db8b324ee2a638ef1309f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5353660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91628aa58370eb7d4b82430296c36ef3185884f74ce0896f830e6d4ebc64c7ce`

```dockerfile
```

-	Layers:
	-	`sha256:94da31b4e97cf9fbe79492b3a495c99f738ea35963b9725a3cd99c93dd2e3ce4`  
		Last Modified: Wed, 22 Apr 2026 02:18:02 GMT  
		Size: 5.3 MB (5340194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37f7da8105cfc8e5c429aeb835a6c48ea3d9260f789631098ac82376db047a32`  
		Last Modified: Wed, 22 Apr 2026 02:18:01 GMT  
		Size: 13.5 KB (13466 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:74fa2dde40a20a721f82b6a7642d3eeb80f564cb0b3af8ef0cfa07f4f43c7a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230575021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c59eb7c9288a7f901a1c60d9afd24b2e8bb6f30b557e34a84578172ed9154b3a`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:20:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:20:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:20:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:20:53 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:20:53 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:21:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:21:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:21:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ab304f220d8a8ccbd47569f385750aa3f87cafd221f915b82f8e566f1abe130b`  
		Last Modified: Wed, 22 Apr 2026 00:16:28 GMT  
		Size: 28.7 MB (28742512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26600aee22ead7827362fa31dfb6cfdc0a04d61583156e0182e6fde7635faceb`  
		Last Modified: Wed, 22 Apr 2026 02:21:29 GMT  
		Size: 142.5 MB (142500863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64e69e6509cf681989e9a843e1544ece5d465c6a7c65d3607ec011298c61cc7`  
		Last Modified: Wed, 22 Apr 2026 02:21:27 GMT  
		Size: 59.3 MB (59331002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7583b334aee3958b87fe8e99c289af2034200e561db81b88f0320c93ecb41af9`  
		Last Modified: Wed, 22 Apr 2026 02:21:25 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1274fd693a8aa2b585f8dbc63c741a2dd3dc14097f5bf8e76eb044da17034563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5360928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa0b2e6c8c41850196140fa392dddc8fe250a12c3f2f751cf8462daf84543b1`

```dockerfile
```

-	Layers:
	-	`sha256:badd8a9cb8f9d72ef853f3e5bd5749e8c035e79e8033dd27e4b6b750268f16c2`  
		Last Modified: Wed, 22 Apr 2026 02:21:25 GMT  
		Size: 5.3 MB (5346544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ad7cf56ff790e147a67d88a3ee5427656e12086bab0c395aaf1300cfe483211`  
		Last Modified: Wed, 22 Apr 2026 02:21:24 GMT  
		Size: 14.4 KB (14384 bytes)  
		MIME: application/vnd.in-toto+json
