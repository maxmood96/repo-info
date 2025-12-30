## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:b72674b77b42722df6079b3093a8c4f5bcd97fb202a278241b571caefc85f0e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:cd1b3b0770d60812ed3cab9e2048393f41a80482e7641421d9a35afd888a9baa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.4 MB (234375739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f79b93714cf06367851b66ba5304fc6db607141c3aa65d42aa978aaba058f73`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Thu, 11 Dec 2025 22:32:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:32:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:32:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:32:26 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:32:26 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:32:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:32:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:32:39 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a88499d92e58a9f7d74dc939bd949d9c2d87abbbaaec03b5f87553e69d901a53`  
		Last Modified: Mon, 08 Dec 2025 22:17:50 GMT  
		Size: 30.3 MB (30258465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf7b307e07565c880943eda34e196721088715f39136f294e491f136c031625`  
		Last Modified: Fri, 12 Dec 2025 01:36:34 GMT  
		Size: 145.0 MB (144966652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78b4dd4299b3cb796389dc98e97b3d6ec0dd3cc69ee317b8248f4db33b487fc`  
		Last Modified: Thu, 11 Dec 2025 22:33:13 GMT  
		Size: 59.1 MB (59149976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a34881eb73eab9a8a4a3e2d096f743a7443d222b583f1b40e09497b2e9d030`  
		Last Modified: Thu, 11 Dec 2025 22:33:05 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7639c13e2c4df8e65b99340fa638147e0a99aac131f3c27b92656837c720bbff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5342475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b43e520876284457b453bd102e3f09d1a9731d3bd5a0cdfba0b25470612106d6`

```dockerfile
```

-	Layers:
	-	`sha256:f3fde5a7ee6287a015214f1df41e388891886ad072d511b6fc01b9bcd5a95409`  
		Last Modified: Fri, 12 Dec 2025 01:35:27 GMT  
		Size: 5.3 MB (5328208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b3a9d85d82eef1c9d38fd1102375f69e1b3dff25863859bcdc4b3a75219b73b`  
		Last Modified: Fri, 12 Dec 2025 01:35:28 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0b87c19560f5a006cc9efa3b31aec862da26483b9cf7975a03feaec5c106ab8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229765061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed53a6c3d9d56b07441920adfb53074d14d514742ba1bc245da0226e508191e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 00:57:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:57:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:57:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:57:36 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 00:57:36 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:57:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 00:57:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 00:57:50 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2b952d66bc8c719b5ca92eacb4307075591731bdc405a12ebd6fa840a24375b7`  
		Last Modified: Mon, 29 Dec 2025 22:27:18 GMT  
		Size: 28.7 MB (28748462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48872ca889428be28cf6f01c19cb518488e3b3a4de2f7a06d648f26f3a18bef0`  
		Last Modified: Tue, 30 Dec 2025 00:58:29 GMT  
		Size: 141.7 MB (141731575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b51c9970dda15f9cc8627185a5b341a40fbbd2cc05b6602fb90d6bb37ded2b`  
		Last Modified: Tue, 30 Dec 2025 00:58:23 GMT  
		Size: 59.3 MB (59284378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7234776d46d91125959e78e01af318d8a4344cb7ce8e9cad5bd083568e938a02`  
		Last Modified: Tue, 30 Dec 2025 00:58:17 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a671b726d9218f61d10e48da856ef7a5acfa5630add964a4f8c4ec7d1f812446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5348943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1816adc8f0a5ce765ac8ba31893b69c0f4e0ddfe03e76503dfd8ec652b239d`

```dockerfile
```

-	Layers:
	-	`sha256:6c685ed4ebe2cba2aa0df2eb23f7f665ee754f929a20ecfc350aec90625d2fcb`  
		Last Modified: Tue, 30 Dec 2025 01:35:28 GMT  
		Size: 5.3 MB (5334558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:474a2ad98653b3ca429a559417cb1aabf301cbccd4d49ac801fd88ab5886d254`  
		Last Modified: Tue, 30 Dec 2025 01:35:29 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json
