## `clojure:temurin-19-tools-deps-1.11.1.1208-bullseye`

```console
$ docker pull clojure@sha256:66637915633dcdf19f692f05c5ebee98c65988d9236f132cb93368b69457f35e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-19-tools-deps-1.11.1.1208-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:7c7698a9f47081f0fd49ec808491756c796a9a6867b10c6d5f14c95065af78fa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.0 MB (328006780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47916fdd60eaceea01bf09cfd02921d4713b5b38d1430e2a1b6d58129acdd7c0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:26 GMT
ADD file:cc6a56676703ec7ab5db8f2f7bc18a3169c0816d38703845b6b77ae5342ab41c in / 
# Sat, 04 Feb 2023 06:51:27 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 14:05:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 04 Feb 2023 14:14:31 GMT
COPY dir:94cb5af8175285c10c94286222d8a35302f3f8c290e00011a75c67156659d6ab in /opt/java/openjdk 
# Sat, 04 Feb 2023 14:14:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 14:16:35 GMT
ENV CLOJURE_VERSION=1.11.1.1208
# Sat, 04 Feb 2023 14:16:35 GMT
WORKDIR /tmp
# Sat, 04 Feb 2023 14:16:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4a3b1200c4d633202648dc3db6ed0a1311e75cc4baeee8fce32208c1eaa07537 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Sat, 04 Feb 2023 14:16:54 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 04 Feb 2023 14:16:54 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Sat, 04 Feb 2023 14:16:54 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 04 Feb 2023 14:16:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:699c8a97647f5789e5850bcf1a3d5afe9730edb654e1ae0714d5bd198a67a3ed`  
		Last Modified: Sat, 04 Feb 2023 06:55:53 GMT  
		Size: 55.0 MB (55025312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:315f8da6444a266b14b964d30d4c839b42701def1a15f9b4ccf306ed2efcc5a3`  
		Last Modified: Sat, 04 Feb 2023 14:25:40 GMT  
		Size: 201.1 MB (201112948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cffc865c1ae3abee53d35d94d85e838cd32e7323c569ff204c78fe004e5eeb19`  
		Last Modified: Sat, 04 Feb 2023 14:26:48 GMT  
		Size: 71.9 MB (71867503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae5e36ce4e70d1f47c156250e3026ee237064f6338574d4af58ab07d584da73`  
		Last Modified: Sat, 04 Feb 2023 14:26:40 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0056f34cd2744059e3282a26cae9ec355ac275635b6243bf1673a7fb172b4c91`  
		Last Modified: Sat, 04 Feb 2023 14:26:40 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-19-tools-deps-1.11.1.1208-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:27befa13cdf1e342b03c209fec70988f4f7bfe9bd5a75cc26b53194bba9d6d07
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325523149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9471ad7ae1f1f9637460a9614491121f36b66abdf8a10d46898d6d8362c89676`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:26 GMT
ADD file:c5a7c65d67685092faa3456c1a772550aa6d06ac07e1f98a95d39c31e304dbf8 in / 
# Sat, 04 Feb 2023 06:17:27 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 17:02:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 04 Feb 2023 17:10:21 GMT
COPY dir:9a6a873ca11063f6f04e7f088397a1fce771e2b1aa8590b72eb07158cfac883f in /opt/java/openjdk 
# Sat, 04 Feb 2023 17:10:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 17:12:13 GMT
ENV CLOJURE_VERSION=1.11.1.1208
# Sat, 04 Feb 2023 17:12:14 GMT
WORKDIR /tmp
# Sat, 04 Feb 2023 17:12:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4a3b1200c4d633202648dc3db6ed0a1311e75cc4baeee8fce32208c1eaa07537 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Sat, 04 Feb 2023 17:12:28 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 04 Feb 2023 17:12:28 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Sat, 04 Feb 2023 17:12:28 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 04 Feb 2023 17:12:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fac7262b6510529638951e16807cf1758f42c892ed924e334c27bb8bbcf7d7c2`  
		Last Modified: Sat, 04 Feb 2023 06:21:01 GMT  
		Size: 53.7 MB (53681927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34aff5f492c4d4ea83d318ec6f9272a812b54796a8a0a69b9d9270336f3202b`  
		Last Modified: Sat, 04 Feb 2023 17:20:09 GMT  
		Size: 199.9 MB (199855199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06f6382cac0d38dad6ec3eeb02001cf7dcf1d695503a1505a98d03e754d0e539`  
		Last Modified: Sat, 04 Feb 2023 17:21:10 GMT  
		Size: 72.0 MB (71985009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c02164fde340138fb34f3eb791c21d92f2e8f299dfddeed7ec8585cbff921a`  
		Last Modified: Sat, 04 Feb 2023 17:21:03 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da1435fcf198e97c80ba7287563e408a594043a13ff89f265a581b034f6eb83`  
		Last Modified: Sat, 04 Feb 2023 17:21:03 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
