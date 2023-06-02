## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:5d2c972adfbcf6e00e5f8badb8e0eeb6a001eeb1e55e5b3e1f3c6208c47bc2b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:dc62da6ada77797fa502666d03dcd9907845d3d4992ec8f431d0d836346e4763
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.4 MB (291448334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f83cf06a919e8411237cbe7ae9df08923fd530a1f69c320795d7c3512f77bb6`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:19:27 GMT
COPY dir:480a3269dc817a8cead3ef1e03a246c3e173090658469b19c2165cafbd3da5de in /opt/java/openjdk 
# Tue, 23 May 2023 08:07:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:09:26 GMT
ENV CLOJURE_VERSION=1.11.1.1323
# Tue, 23 May 2023 08:09:26 GMT
WORKDIR /tmp
# Tue, 23 May 2023 08:09:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "c4666f0e2c2397b91554befd71ff6149b2e89acbf90400e1dcf557526cfb593d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 23 May 2023 08:09:43 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 23 May 2023 08:09:43 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e80ece7b5d59b8f713850fc7b510f037c2d5884cbead449774454a259f42de`  
		Last Modified: Tue, 23 May 2023 04:21:29 GMT  
		Size: 198.5 MB (198549524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd368ed6ec757c267d12d395c5c20cf2b0e0754331d9cf4f5289c47bd14efc8`  
		Last Modified: Tue, 23 May 2023 08:18:02 GMT  
		Size: 61.5 MB (61494605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8726ace00639efdeb0c9bd32c97f6e0c86f4f38467947f570a3d46a89a2e5205`  
		Last Modified: Tue, 23 May 2023 08:17:55 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ac75f5bcc2ab46f786087b42ca1af72ae81523bd59a21e141d1a7fd4bf88fbc6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.0 MB (286986437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7538cebcea310eca40989752333c4235d7fc986d5f391d6d7eb8e49555781600`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:15:33 GMT
COPY dir:26a87923e6280eb6d7e3200000ba2b8bbfa8612b133801ac6abaec9535613186 in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:15:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:18:03 GMT
ENV CLOJURE_VERSION=1.11.1.1323
# Fri, 02 Jun 2023 01:18:03 GMT
WORKDIR /tmp
# Fri, 02 Jun 2023 01:18:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "c4666f0e2c2397b91554befd71ff6149b2e89acbf90400e1dcf557526cfb593d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 02 Jun 2023 01:18:18 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 02 Jun 2023 01:18:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ce6b04b349835fc6f3b283f12235744dbbbc7db7136934011776cdcb8de4d4`  
		Last Modified: Fri, 02 Jun 2023 01:24:58 GMT  
		Size: 195.3 MB (195324212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0334e0b37cda30404ea2a99742193bfbbee7bc9537cda87d6f3719f62eb9ed3`  
		Last Modified: Fri, 02 Jun 2023 01:26:17 GMT  
		Size: 61.6 MB (61608859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f904ceb13b36037f1a70afea3cae06e1fada7fcc217b6dffd651e408aada11e`  
		Last Modified: Fri, 02 Jun 2023 01:26:10 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
