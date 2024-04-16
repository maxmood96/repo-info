## `clojure:temurin-17-tools-deps-1.11.1.1435-bookworm-slim`

```console
$ docker pull clojure@sha256:8dc2c512868cabe4166d7a04daf2af4a1ebe902ff9f3c3a93cef3da10f477d99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.1.1435-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:865c2b90730ea92c2f452a47fd7b4742b977d9054aa9f17566dc2bd181ac1188
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243086818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f1f3d678c769df0e4bec2f67976f0625cdfc9bdf1817b4889af804948f0a21`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:17:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 06:28:57 GMT
COPY dir:88c5118aff6896f6ed535dcde576d68ef88ded459cca013e0f9beb3e430ebb52 in /opt/java/openjdk 
# Wed, 10 Apr 2024 06:28:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:32:53 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 10 Apr 2024 06:32:53 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 20:29:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -sLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 10 Apr 2024 20:29:51 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 10 Apr 2024 20:29:51 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 10 Apr 2024 20:29:51 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 10 Apr 2024 20:29:51 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9330ece2b18c5aab4f640b1856df6879bdb1041bb0b0f67a4d3195236bed4e0`  
		Last Modified: Wed, 10 Apr 2024 06:45:59 GMT  
		Size: 144.9 MB (144893073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cfe17d8e105149b2ebf41ac85329010ba0ae9b01886a2a75e50897937e3664`  
		Last Modified: Wed, 10 Apr 2024 20:46:25 GMT  
		Size: 69.1 MB (69061370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24ee33f564b7ee2c0a260d4be67dfaedefa19bc788ae6be3f66e9193f61b4ed`  
		Last Modified: Wed, 10 Apr 2024 20:46:17 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ea921327d2eb9a19f6cf984888af06c209c5ddb03e2c69736e5b5766d49e56`  
		Last Modified: Wed, 10 Apr 2024 20:46:18 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-1.11.1.1435-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dbe758ef21446c275d708125e9bda5ed73093b5f6ec97070d4a03ae855c831a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241701447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c89e8a6612ae0e0197065461b79e07975c0ae1922b7681c03d36ebda67d18ea`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:23 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Wed, 10 Apr 2024 00:40:23 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:38:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Apr 2024 06:40:26 GMT
COPY dir:00f694ce512d2e49bdb0844fa7f6d54a4b39a35418d1c6b32b574b5d44cfc1da in /opt/java/openjdk 
# Tue, 16 Apr 2024 06:40:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 06:45:11 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Tue, 16 Apr 2024 06:45:11 GMT
WORKDIR /tmp
# Tue, 16 Apr 2024 06:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -sLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 16 Apr 2024 06:45:27 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 16 Apr 2024 06:45:27 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 16 Apr 2024 06:45:27 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Apr 2024 06:45:27 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1524327b5ca19acc0cd54b203239bb4f537664cf1202cda7b226bcd7d428c4e2`  
		Last Modified: Tue, 16 Apr 2024 06:56:52 GMT  
		Size: 143.7 MB (143720949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd7876d9555c0fb52889dd1fec0d623bc377d65f0cc85c795636e5908a2d15c`  
		Last Modified: Tue, 16 Apr 2024 06:59:26 GMT  
		Size: 68.8 MB (68817325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c616b73d2e9b14e11ba08290752bc28f6f9ecb3a54b3c90cd297ab894e2b4365`  
		Last Modified: Tue, 16 Apr 2024 06:59:19 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69c71f5eb7e0a2ee11742e471511e6d829e7f8c5cef37be10c5f2234009b73a`  
		Last Modified: Tue, 16 Apr 2024 06:59:19 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
