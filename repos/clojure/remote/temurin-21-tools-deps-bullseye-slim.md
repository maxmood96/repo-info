## `clojure:temurin-21-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:4f4dbe89d84203ff9b62d6b4fadeb7aaadbfca3dc015678307205b7e260dea52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:955776a6296ab93bbb19ab590a4a52c3fda685cdbdcf109c17fec65369a5896e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246885788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faac1d2ed2978962624328c382720d535d13189f10687ecd5b11548d03c345d7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e982ca09eef8b3f27f6333071135d9d3f3979b940e371327568b5100f4325e0`  
		Last Modified: Wed, 23 Apr 2025 17:16:45 GMT  
		Size: 157.6 MB (157634511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e5a329b90438e21769458fd2f96b402e31ceaff47a501137b5543e5e4eb0e3`  
		Last Modified: Wed, 23 Apr 2025 17:16:43 GMT  
		Size: 59.0 MB (58992812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aced7f2573e9c5e95d844065733a8528ccdc6d16b6d01a6fd8e49fa9f16030`  
		Last Modified: Wed, 23 Apr 2025 17:16:41 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5b96e690ef13a68a07da5417c521190a11345ab11ca7713d5ef8bcbf123ed7`  
		Last Modified: Wed, 23 Apr 2025 17:16:41 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2b61586af6856d128973c8c7b6d6d567c0e2a48c6ba7b881154ed4c06eace45b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7d682cb341e55c3391a7eb347f5482e252e9a79fefb82660c650b66ebbcc13`

```dockerfile
```

-	Layers:
	-	`sha256:de9404f78fd36e911b64fd82132338464762f57ae0a4a41abf99e58edd21d7d6`  
		Last Modified: Wed, 23 Apr 2025 17:16:42 GMT  
		Size: 5.1 MB (5122811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2362c33f9e31fe39a3bc5e5eab90be244bd55697a00b740c0c3da536cb92550b`  
		Last Modified: Wed, 23 Apr 2025 17:16:41 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:15d2c194b75aea3f21dcc50563031a4c276aa1e343ac336d53c277eff1ea114f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243806652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df83d879a1ac0b09505011ffdbb828a570824f4ca4d1d61c7941f6e42384cb8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6ea0ce4481c6c59b9cdc12bd913c4b5bafca5da592cdedda4048ea90395fca`  
		Last Modified: Wed, 23 Apr 2025 18:09:18 GMT  
		Size: 155.9 MB (155928792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb6181e21004275c098d7ee7b36609911106b4eea148eb3dbf3b85d1a80d9ab`  
		Last Modified: Wed, 23 Apr 2025 20:00:39 GMT  
		Size: 59.1 MB (59127314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7290008066b80f0e9e3d3f707f7f9dd1f89b7ce850391453ff6c1a74f0e9bdc9`  
		Last Modified: Wed, 23 Apr 2025 20:00:37 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef59f216b41ee2e80b7708038c65f6c5d549e27a283e27e8be6e58d973ba50a`  
		Last Modified: Wed, 23 Apr 2025 20:00:37 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5fc716697a0807e68b6debed4fb80ce6671925930906664dbee7a30c653573f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5145284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5124ec248fc408c975b4f71e238a92d8588e9d1919f11906221ac9169d09c6`

```dockerfile
```

-	Layers:
	-	`sha256:0162214ca18eb0b02ba22c00d4491cc56fc90b6523a5fa6759af492d86d84aec`  
		Last Modified: Wed, 23 Apr 2025 20:00:37 GMT  
		Size: 5.1 MB (5128567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6fcd9001b0ceeb97d4b23c704a600bb4c055d17cf9dea693816410e12e39983`  
		Last Modified: Wed, 23 Apr 2025 20:00:37 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
