## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:9124d228fd6bffc8e7b2a2015ef2af6e930fe10369a1c2a3cd96ebdfd7751f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:65d984e50a17c7123f8220fe9b3eb7876eb19f02ae2cdbcf9acb968edd5105bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234941383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d3ad8c77d2973fc0ca6e621d39ea7d1cb4f7f8d1198b4ade8c53e9ab5cfc9b8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:12:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 Mar 2024 06:24:15 GMT
COPY dir:3be96ae7faea81e90455993c99b71c9b45986c7e71f70fc577ab97699c92b508 in /opt/java/openjdk 
# Tue, 12 Mar 2024 06:24:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 06:28:48 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Tue, 12 Mar 2024 06:28:48 GMT
WORKDIR /tmp
# Tue, 12 Mar 2024 06:29:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 12 Mar 2024 06:29:05 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 12 Mar 2024 06:29:05 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 12 Mar 2024 06:29:05 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 12 Mar 2024 06:29:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa99337ab9effaa7179d80eb78de5d10c8c8d850b1473f6d62d507d309df157`  
		Last Modified: Tue, 12 Mar 2024 06:41:30 GMT  
		Size: 144.9 MB (144893175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ecc4c8fff05f42eb79cde2db809cc014877b7c587c125bd2d053fb0c5b5457`  
		Last Modified: Tue, 12 Mar 2024 06:43:21 GMT  
		Size: 58.6 MB (58624706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d6707a43586c2118ec36b3dc7d078e32571291dca4c82ce2d75807f42518b8`  
		Last Modified: Tue, 12 Mar 2024 06:43:14 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3264857e37ddf5a06c2dec5230442fe502c82ec8087aedb4adcd26a8b475cbb3`  
		Last Modified: Tue, 12 Mar 2024 06:43:14 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3cd5dc9364e9dd77873ba1406ea8eae093aaee64c8bc1b94c06998f52cd23460
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232543850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf9eea35f57d63f8329033a8c9165dfec564b49f97e33bb22da97000bba9234`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:45:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 02:40:27 GMT
COPY dir:a5d0039514ccd79689a0ea6094d70ca92113e8cbcc38d473b7c0fcc04a1f496a in /opt/java/openjdk 
# Thu, 28 Mar 2024 02:40:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 02:44:34 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 28 Mar 2024 02:44:34 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 02:44:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 28 Mar 2024 02:44:49 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 28 Mar 2024 02:44:49 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 28 Mar 2024 02:44:49 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 28 Mar 2024 02:44:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:357c1070edd1560e2fca055cc1853bc6786248dbfbf2c71f7238747ddd407d1c`  
		Last Modified: Thu, 28 Mar 2024 02:54:36 GMT  
		Size: 143.7 MB (143720921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f05df7dfc4573947c962870d1042d76580b9cbc2adb8dd02b0f08020c076c6`  
		Last Modified: Thu, 28 Mar 2024 02:57:03 GMT  
		Size: 58.8 MB (58750795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd7e7d1f9b6dc0fab97d5331f027220c55ccb84d587b7f406f5dcffe151c567`  
		Last Modified: Thu, 28 Mar 2024 02:56:58 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90bcbe48d651522d8f5811d42744d093d38db9bf2a6a5e3f75b03f8ecdf64a8a`  
		Last Modified: Thu, 28 Mar 2024 02:56:58 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
