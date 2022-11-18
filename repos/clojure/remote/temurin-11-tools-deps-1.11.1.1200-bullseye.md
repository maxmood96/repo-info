## `clojure:temurin-11-tools-deps-1.11.1.1200-bullseye`

```console
$ docker pull clojure@sha256:82d26afe070fb2da60883fa41294942b7f27df832061cd266e1a57b039e4baf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-1.11.1.1200-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:dc365f15225fa3e43c24b91c4ec882a216bef61145bcb92f2db495834767088c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.8 MB (300806217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d886d4c283a0458f6b58c44c5632c471957c90cac6d85f0182b08c170ed70c0`
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
# Fri, 18 Nov 2022 22:23:47 GMT
ENV CLOJURE_VERSION=1.11.1.1200
# Fri, 18 Nov 2022 22:23:47 GMT
WORKDIR /tmp
# Fri, 18 Nov 2022 22:24:03 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "694381cb78d44f143bdcc38657507f012ebac4009bc57cec67abef1675447878 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 18 Nov 2022 22:24:04 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 18 Nov 2022 22:24:04 GMT
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
	-	`sha256:bb3055b9fcbd743a6a29983010a9588bff73e5ae28ac1daf41036665fe446431`  
		Last Modified: Fri, 18 Nov 2022 22:33:57 GMT  
		Size: 47.3 MB (47311169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95f3cec865f1d21c5e69faa71a24befa1c3b73c983b1f0a654c8a008c6cbc04`  
		Last Modified: Fri, 18 Nov 2022 22:33:52 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-1.11.1.1200-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:589fa41991447df519d49ba4098e875dddb39d3aaf1b6ec4c5815c2897d2f69b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.2 MB (296206157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b1b0995ed94099a2528c8809450fa5b1b9f4a9917e8e8593dccbb6a2b7291f9`
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
# Fri, 18 Nov 2022 22:43:06 GMT
ENV CLOJURE_VERSION=1.11.1.1200
# Fri, 18 Nov 2022 22:43:06 GMT
WORKDIR /tmp
# Fri, 18 Nov 2022 22:43:18 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "694381cb78d44f143bdcc38657507f012ebac4009bc57cec67abef1675447878 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 18 Nov 2022 22:43:19 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 18 Nov 2022 22:43:19 GMT
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
	-	`sha256:6274df5e695945cd5089800dc21990a89891727666748f311235d9bbccef13c6`  
		Last Modified: Fri, 18 Nov 2022 22:50:57 GMT  
		Size: 47.3 MB (47304513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d572f42d9eb77f6752ca922154d8461ff89ca740c132437e28b3e612c0deee90`  
		Last Modified: Fri, 18 Nov 2022 22:50:52 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
