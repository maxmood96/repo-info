## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:f2c16789e1a37c22ab028908f2a6ad20c3a9b6e98d035baf825f4e9e8bb9173b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e1eef148ed43211b376a55d004a451050125facb0e97d72cd8b58712099841e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243458187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79eebb8cb14230c3455de4aa367fb6398f7dec06324ae037956bceef45e8a4ad`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:47:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 14:02:05 GMT
COPY dir:9807503b62b5ec57f5790350ba2323b4402a31264d57970336b28a606d7a3a68 in /opt/java/openjdk 
# Wed, 06 Mar 2024 14:02:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 14:07:49 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 06 Mar 2024 14:07:49 GMT
WORKDIR /tmp
# Wed, 06 Mar 2024 14:08:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 06 Mar 2024 14:08:09 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 06 Mar 2024 14:08:09 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d001d8a2900abfa74e3eea1ab01d3a896c3ba25736082483c2e900b34e2ad16`  
		Last Modified: Wed, 06 Mar 2024 14:23:15 GMT  
		Size: 145.3 MB (145271156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5baac5152967a2ce44e1d4928953940dda17a07ab92a2e5312e22ddb639d9591`  
		Last Modified: Wed, 06 Mar 2024 14:26:19 GMT  
		Size: 69.1 MB (69062321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a354780b8499e7048191260f60a5b2f46654a10d55990303dc79452e45d8c73e`  
		Last Modified: Wed, 06 Mar 2024 14:26:10 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b263a2a0e394137670646f6663893801757fd8364dcea5e09abb640d1dc43d45
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.0 MB (239982476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf1c06e076304d0720e0ca99e8147e011aa29a9e476260220abd83fa03e02e20`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:55:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 13:16:12 GMT
COPY dir:774c748cac67d918432726696917d770e1c557a90a62f56899a68f5b5861f304 in /opt/java/openjdk 
# Wed, 06 Mar 2024 13:16:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 13:21:10 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 06 Mar 2024 13:21:11 GMT
WORKDIR /tmp
# Wed, 06 Mar 2024 13:21:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 06 Mar 2024 13:21:27 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 06 Mar 2024 13:21:27 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb60af30bdfa4757501b10b3144c73b97f2ae7d85ebcf327f64d9b6e809c371`  
		Last Modified: Wed, 06 Mar 2024 13:33:53 GMT  
		Size: 142.0 MB (142008469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ae895fd4bcc5086762535e6bb8569bd880b55f16c2414cea2f98e21608d396`  
		Last Modified: Wed, 06 Mar 2024 13:36:30 GMT  
		Size: 68.8 MB (68817026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54967ac1fb5e4e87cc51b3e9c598517fd645fc4579fe9370d871ae46619bb7d2`  
		Last Modified: Wed, 06 Mar 2024 13:36:24 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
