## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:5ed098a0cb5dfb6a771704b61acc4a13c549e272d35358db0cb587e8ee7731cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:a31f67dc23410cd63277ee291b3e21cb1d05f92a8684c48a99f088fbabebe60c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.8 MB (300796090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a1b4e9417e7af717f1aabbab7b8483ad1fc6dcebdd6a031460731940ea0277`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:43 GMT
ADD file:abc6873c98339a3c496cb75ec2528e65ebe1f20d2cea777033f86dcd55d73da5 in / 
# Tue, 15 Nov 2022 04:04:43 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 17:50:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 17:54:03 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Tue, 15 Nov 2022 17:54:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 17:56:14 GMT
ENV CLOJURE_VERSION=1.11.1.1189
# Tue, 15 Nov 2022 17:56:14 GMT
WORKDIR /tmp
# Tue, 15 Nov 2022 17:56:31 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "1afd91b165776615eca84cce2271e5fe5d5818c55dee0f082b1304bb1464b3e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 15 Nov 2022 17:56:31 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 15 Nov 2022 17:56:31 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a8ca11554fce00d9177da2d76307bdc06df7faeb84529755c648ac4886192ed1`  
		Last Modified: Tue, 15 Nov 2022 04:08:24 GMT  
		Size: 55.0 MB (55038615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b1d80bdfeef6cb6cdf5a91dce43100373840e0ed893c308f6732d8bf622362`  
		Last Modified: Tue, 15 Nov 2022 18:08:18 GMT  
		Size: 198.5 MB (198455814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8668f649deadb2e68a94b8c4024cc4359fa3dac8468a30714db3045fb57c4f8`  
		Last Modified: Tue, 15 Nov 2022 18:09:25 GMT  
		Size: 47.3 MB (47301046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c118806796f8758e09c9438548effb617fb49adc35ceba8fe9df38bc404e46a5`  
		Last Modified: Tue, 15 Nov 2022 18:09:19 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7c06c4b3554723708771135172c100a83916592dfa2f9f7325575ad86c068da5
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.2 MB (296196005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cafe948210c2b1da909d0de747020a6c33cb1e267986fd462f96c2327941e820`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:12 GMT
ADD file:1f3a7177f64e1adda3e7a541c93dd4322c6ecb4f00f7b015665df2c0c08b59a5 in / 
# Tue, 15 Nov 2022 01:41:12 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 05:48:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 05:51:26 GMT
COPY dir:5aa0292cc524fb250468b6c5a859d971d75bcb0dd4bed7cfb9f10423858de6d6 in /opt/java/openjdk 
# Tue, 15 Nov 2022 05:51:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 05:53:21 GMT
ENV CLOJURE_VERSION=1.11.1.1189
# Tue, 15 Nov 2022 05:53:21 GMT
WORKDIR /tmp
# Tue, 15 Nov 2022 05:53:33 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "1afd91b165776615eca84cce2271e5fe5d5818c55dee0f082b1304bb1464b3e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 15 Nov 2022 05:53:33 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 15 Nov 2022 05:53:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:077c13527d405646e2f6bb426e04716ae4f8dd2fdd8966dcb0194564a2b57896`  
		Last Modified: Tue, 15 Nov 2022 01:44:12 GMT  
		Size: 53.7 MB (53699862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6410c82310e7ed376d2f9bdb09d5bba8c5586def41b40a45fc26ed1c405a8a0`  
		Last Modified: Tue, 15 Nov 2022 06:03:10 GMT  
		Size: 195.2 MB (195201165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c3e431c84f580ce12397f85014d104fa250de304ff12298dd2353520bc3c89`  
		Last Modified: Tue, 15 Nov 2022 06:04:07 GMT  
		Size: 47.3 MB (47294361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83582cabd4830383387b2d94f9a24ece00c88dd52d3ff45719c5752f2abd6df3`  
		Last Modified: Tue, 15 Nov 2022 06:04:02 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
