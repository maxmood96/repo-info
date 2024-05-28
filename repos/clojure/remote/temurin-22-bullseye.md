## `clojure:temurin-22-bullseye`

```console
$ docker pull clojure@sha256:b13bb5d01dca77af8d91a9a3a5ce37fe00a31c4aeacc423ce814b5f9f8c54a03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-22-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:78c88a662a646812c3c269ceb91de2705c824b7aa9951e75985ecaf263b16c70
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280837512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0402a628734c53ee5f36e9002db9fcc4339cf1f870690fd315e459dee21ad29`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:28:14 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 14 May 2024 01:28:14 GMT
CMD ["bash"]
# Tue, 28 May 2024 21:21:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 21:43:28 GMT
COPY dir:26aa9b736de249ab67b8c50e579c4c188c999c32408e8bbdcde37c30c2d0e7d3 in /opt/java/openjdk 
# Tue, 28 May 2024 21:43:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 21:45:47 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 21:45:47 GMT
WORKDIR /tmp
# Tue, 28 May 2024 21:46:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 28 May 2024 21:46:05 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 28 May 2024 21:46:06 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 28 May 2024 21:46:06 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 21:46:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1fa83d9d3382df6799451227760bdef26d7b3aaee09c0490746ddab4a52130a`  
		Last Modified: Tue, 28 May 2024 22:05:28 GMT  
		Size: 156.7 MB (156714931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27273d5391eff37725510b6092f321ed51d9686584e7a797975073499e1b7f9b`  
		Last Modified: Tue, 28 May 2024 22:07:10 GMT  
		Size: 69.0 MB (69022166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc666a95794cef42b708e7ad8c6c74399cda3df9954df7f62a25467a9512c1a`  
		Last Modified: Tue, 28 May 2024 22:07:02 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f05738359a63024edffeb591304249874bced58d9844682ba6f65a0b8cafd3f`  
		Last Modified: Tue, 28 May 2024 22:07:01 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-22-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:886846af12730b8d203d6e263ca83c1d353339e0ff7b06d97a79ed3aad9cd84b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.6 MB (277615470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f85ed8f3100f470885c612a5fc02cdf0c64385a8b35d803835ce2e8d316923`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:47 GMT
ADD file:43721c605da3f74f0c3f71384780fc0e57e2478b88197672caaf4baa3eddab23 in / 
# Tue, 14 May 2024 00:39:48 GMT
CMD ["bash"]
# Tue, 28 May 2024 19:44:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 20:02:43 GMT
COPY dir:8db4aa7d00469f3c784932412aa95caf68b05146a02559362a91df21ce463ad4 in /opt/java/openjdk 
# Tue, 28 May 2024 20:02:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 20:04:43 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 20:04:43 GMT
WORKDIR /tmp
# Tue, 28 May 2024 20:04:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 28 May 2024 20:04:58 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 28 May 2024 20:04:58 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 28 May 2024 20:04:58 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 20:04:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:078d9526cc72763b2db16388f6b511c18a73e3e7f9d229364b3b85a6b5277bc8`  
		Last Modified: Tue, 14 May 2024 00:43:13 GMT  
		Size: 53.7 MB (53738990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84a1f76b155da5c15c43207f175b35e0a21820d0d8c424cae5b958fe3956aa4`  
		Last Modified: Tue, 28 May 2024 20:22:14 GMT  
		Size: 154.7 MB (154737692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f00810a24c34d95dfa6239e4f7c936be5e017290105de10256119b5f556f93a5`  
		Last Modified: Tue, 28 May 2024 20:23:39 GMT  
		Size: 69.1 MB (69137770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591692a0ca8d8f98b41ff6f1a960fd481679018b016cd266b8927a49e1ef1a9a`  
		Last Modified: Tue, 28 May 2024 20:23:31 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77b9ebec0978a3b11daee34cddd60693e2647499b60c196699de3f2cce9b34e`  
		Last Modified: Tue, 28 May 2024 20:23:31 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
