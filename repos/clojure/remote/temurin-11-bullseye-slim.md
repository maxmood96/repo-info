## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:dd9596926e9b8deff6d360b9c095c798dec2fbba2d5798a1c5c0c0f96426f111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e6917fdd780025d0254e948a9b20dbfd7f3bc7c5a6da7d65294f7d50c27ff36b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.3 MB (291349331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd8c24cd066f05ba78a5416af2ad5f8037d618462547815380b7c94e2b2bcaea`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Nov 2022 00:29:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Sat, 05 Nov 2022 01:12:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 01:17:02 GMT
ENV CLOJURE_VERSION=1.11.1.1189
# Sat, 05 Nov 2022 01:17:02 GMT
WORKDIR /tmp
# Sat, 05 Nov 2022 01:17:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "1afd91b165776615eca84cce2271e5fe5d5818c55dee0f082b1304bb1464b3e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Sat, 05 Nov 2022 01:17:19 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 05 Nov 2022 01:17:19 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eeac167d177f8e3f122f752a133299e5053ba524e678b50f631ee9e5c6e940`  
		Last Modified: Sat, 05 Nov 2022 00:31:16 GMT  
		Size: 198.5 MB (198455845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f80adccc38ba1104daa0927ca61af4939452782d00656628482b7a0d3a514b`  
		Last Modified: Sat, 05 Nov 2022 01:28:36 GMT  
		Size: 61.5 MB (61472828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e737dac9bede65594b1fff631143e9c112beb9feb5066492b8cacaab22b092`  
		Last Modified: Sat, 05 Nov 2022 01:28:29 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:82b33a0b76c6ac6e95b2894bfab5ef18929ef26424f5e178bb41be563cf20ad4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.9 MB (286858775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3faadb76d17414e0d01eeb1121a199d226b16611eb967a566109efd661bcf77e`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 04 Nov 2022 23:12:49 GMT
COPY dir:5aa0292cc524fb250468b6c5a859d971d75bcb0dd4bed7cfb9f10423858de6d6 in /opt/java/openjdk 
# Fri, 04 Nov 2022 23:12:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Nov 2022 23:15:48 GMT
ENV CLOJURE_VERSION=1.11.1.1189
# Fri, 04 Nov 2022 23:15:48 GMT
WORKDIR /tmp
# Fri, 04 Nov 2022 23:16:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "1afd91b165776615eca84cce2271e5fe5d5818c55dee0f082b1304bb1464b3e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 04 Nov 2022 23:16:02 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 04 Nov 2022 23:16:02 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb106e6b88c840d8bc916d39cbd7e76282f34fad97623abb4a385dbc33404ce`  
		Last Modified: Fri, 04 Nov 2022 23:23:35 GMT  
		Size: 195.2 MB (195201089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0719b30aea1c156c35c7030bd75d2e6e8b68d1d27e476849eb9eee9fc076e08a`  
		Last Modified: Fri, 04 Nov 2022 23:25:27 GMT  
		Size: 61.6 MB (61593159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae350f29046b30fbce9684c79723ba071aafe4e8b0266b22400fc1644e407f9`  
		Last Modified: Fri, 04 Nov 2022 23:25:21 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
