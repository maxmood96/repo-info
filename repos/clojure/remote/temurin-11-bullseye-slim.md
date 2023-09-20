## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:394cb60951890194580c4ba29afe13c9e3e20bd5066500ecea64cb773c42099a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c738b9f2e8712ebe1dcb56f104c30ff0e45c2bdb0a2a06061fed3d031a8e6030
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.7 MB (237738689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee3c4e76bd1f87d8b2500c9360d30e450b2a9a61cf647ea977e7a11bb8b91c56`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:03 GMT
ADD file:7eb149bcaba1d7dcab06b3f9a0615ca459e9cb28459a0864f92b0037f270ba66 in / 
# Wed, 20 Sep 2023 04:56:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:22:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 Sep 2023 07:25:26 GMT
COPY dir:3e9b1d3d54369337872a2b8aa8c30068d69b28c2def3ec3bf07ba34bd69d48a0 in /opt/java/openjdk 
# Wed, 20 Sep 2023 07:25:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 07:27:18 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Wed, 20 Sep 2023 07:27:18 GMT
WORKDIR /tmp
# Wed, 20 Sep 2023 07:27:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 20 Sep 2023 07:27:35 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 20 Sep 2023 07:27:35 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7dbc1adf280e1aa588c033eaa746aa6db327ee16be705740f81741f5e6945c86`  
		Last Modified: Wed, 20 Sep 2023 05:01:05 GMT  
		Size: 31.4 MB (31417711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:386a93addc060819e53101917ea458e4b015b760aeb9ab2f21c38b4ff88c1e7d`  
		Last Modified: Wed, 20 Sep 2023 07:35:54 GMT  
		Size: 144.8 MB (144826040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b3fb04ecaf8609168b3ca6b63d4823f656169997afb9ee1d8a0208afa9f0a9`  
		Last Modified: Wed, 20 Sep 2023 07:36:52 GMT  
		Size: 61.5 MB (61494321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f78d1f1e4b0ba99eccb769da22e6706df12ff6305a1b3620a1d73e5a3cb842`  
		Last Modified: Wed, 20 Sep 2023 07:36:45 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ce093a36e34a3b103c9282d66ab79166bbad73e1109337c0a51757d56aa56e17
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233245257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09d017a1e4b8675e7b8635725fce6707bcdd84878ba3f504aa75e2419d8fbc7c`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:53 GMT
ADD file:abd1ad48ae3ebec7a6ecc8ce3016c25be2afcbaedfcb904bc89b1ce59400aef0 in / 
# Thu, 07 Sep 2023 00:39:54 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 06:46:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 Sep 2023 06:47:24 GMT
COPY dir:68819d2d348aedadecb99120d7ca4a63dcc1e3aa0bb526ecbd9925396c38234c in /opt/java/openjdk 
# Thu, 07 Sep 2023 09:07:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 09:08:50 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Thu, 07 Sep 2023 09:08:50 GMT
WORKDIR /tmp
# Thu, 07 Sep 2023 09:09:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 07 Sep 2023 09:09:05 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 07 Sep 2023 09:09:05 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f96ab15157043879c2ff23e0556e798eba6a6ff3d7fd5d1384de223bb9f66f1d`  
		Last Modified: Thu, 07 Sep 2023 00:43:41 GMT  
		Size: 30.1 MB (30062903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50b018ed6a392610f1ab69e85cc642842b49d22521199586d6067dfd326f17f2`  
		Last Modified: Thu, 07 Sep 2023 06:49:54 GMT  
		Size: 141.6 MB (141570382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0789fd3ef9d272213b805bb88fc4a0ce5f4c23d7d65a1425da62ed632313e56e`  
		Last Modified: Thu, 07 Sep 2023 09:17:10 GMT  
		Size: 61.6 MB (61611356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d62ff56dc108a15d24870f126cf264b02a4b9c8fa619731dc710ec789b9fae`  
		Last Modified: Thu, 07 Sep 2023 09:17:04 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
