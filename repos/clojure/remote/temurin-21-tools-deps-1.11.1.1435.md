## `clojure:temurin-21-tools-deps-1.11.1.1435`

```console
$ docker pull clojure@sha256:b92880cda4e4a1e9e401ea55d6f12050a249d233203d09286f08f4a6880603b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-21-tools-deps-1.11.1.1435` - linux; amd64

```console
$ docker pull clojure@sha256:1ace8864768eeb20f473ba5c43423ef597794c8425b9562ad6fde01cd061961f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.6 MB (289628256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bce80e04efca734ff5fa27b7987205760c543c14189f7ffe0719b1e862b8d0f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:46:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 01:46:03 GMT
COPY dir:64a8841762a9afbd2fb8b4cf497b2dee87765737d44ff0387ce1cfc51371c9a2 in /opt/java/openjdk 
# Tue, 13 Feb 2024 01:46:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 02:05:35 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Tue, 13 Feb 2024 02:05:35 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 02:05:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 13 Feb 2024 02:05:54 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 13 Feb 2024 02:05:54 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 13 Feb 2024 02:05:54 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Feb 2024 02:05:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac03a7f283e20bd199f104c518db551847a814260afb78158754b57f9b907209`  
		Last Modified: Tue, 13 Feb 2024 02:09:07 GMT  
		Size: 159.6 MB (159582957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655a47ac8214cb30fe2befa676447660d35f1830683d86f5707980e06d28a73c`  
		Last Modified: Tue, 13 Feb 2024 02:21:45 GMT  
		Size: 80.5 MB (80491678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbbd70b8416996ec2379e3caacfee7e9a53de74201c38536f5e87495990b0181`  
		Last Modified: Tue, 13 Feb 2024 02:21:36 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f57538cac49a800c6ee699ba96e5ea2e0761a80d41060d79b0a468261ad04c`  
		Last Modified: Tue, 13 Feb 2024 02:21:36 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-21-tools-deps-1.11.1.1435` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5677b75b7f50c8a0991d65240e341ca11c70980696238c6e5e498d8fc25f9721
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.6 MB (287632759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8fc9d1499125bb3599da2a7e250551506117b9c686ff708f0bd212b65425c97`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:10 GMT
ADD file:73b36e8089732e9bb253d9a9db76cc1cf5c430bd49647849b77924cd5fdaf8ae in / 
# Tue, 13 Feb 2024 00:41:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:53:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 01:53:50 GMT
COPY dir:ab40534e435f9942975c0e8b5454d6b7a8d69c445f8e0758c1bd9c500e157fca in /opt/java/openjdk 
# Tue, 13 Feb 2024 01:53:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 02:10:32 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Tue, 13 Feb 2024 02:10:32 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 02:10:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 13 Feb 2024 02:10:49 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 13 Feb 2024 02:10:49 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 13 Feb 2024 02:10:49 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Feb 2024 02:10:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c2964e85ea54bbef26d274e85fa0a3fde68f074e0774d0729e6ebe341e24eee1`  
		Last Modified: Tue, 13 Feb 2024 00:44:29 GMT  
		Size: 49.6 MB (49590965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c549056bdb74e56fca77811dd657befb8252b41fdbe4d900869dcf87f967d62d`  
		Last Modified: Tue, 13 Feb 2024 02:13:34 GMT  
		Size: 157.8 MB (157784612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e8e2d5c2c71f671f8d77fe4d1a6edd2f3583f8de1973dccfb2ebbb45b6fd5b`  
		Last Modified: Tue, 13 Feb 2024 02:25:36 GMT  
		Size: 80.3 MB (80256169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6179a2eee27462e4e048d16c33b90784f0055e16d75fe02bdc092ef45cfa7cbf`  
		Last Modified: Tue, 13 Feb 2024 02:25:27 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb04e4555322bb489b072d53ce24a74de8962e343a5d038a9561e6502499072`  
		Last Modified: Tue, 13 Feb 2024 02:25:27 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
