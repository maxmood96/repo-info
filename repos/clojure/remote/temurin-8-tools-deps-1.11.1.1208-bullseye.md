## `clojure:temurin-8-tools-deps-1.11.1.1208-bullseye`

```console
$ docker pull clojure@sha256:f170a2fb2e68566743a1dfa82935c5d4169cc83a0bb01993b4960530ef891b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-tools-deps-1.11.1.1208-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:1bfe02f81615e17450160fed527df73a0d4912fb24446778bc2313ef826e6a69
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181529180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbf4e8467356f7f86771dbff655eca852ecfbccf71d51e8a843f2aec2778c74c`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:26 GMT
ADD file:cc6a56676703ec7ab5db8f2f7bc18a3169c0816d38703845b6b77ae5342ab41c in / 
# Sat, 04 Feb 2023 06:51:27 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 14:05:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 04 Feb 2023 14:05:28 GMT
COPY dir:bbb84183d7ea38d81d8401f01e29d08935ee4c8bf6f90c6527579a1554c3bde1 in /opt/java/openjdk 
# Sat, 04 Feb 2023 14:05:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 14:07:35 GMT
ENV CLOJURE_VERSION=1.11.1.1208
# Sat, 04 Feb 2023 14:07:35 GMT
WORKDIR /tmp
# Sat, 04 Feb 2023 14:07:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4a3b1200c4d633202648dc3db6ed0a1311e75cc4baeee8fce32208c1eaa07537 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Sat, 04 Feb 2023 14:07:54 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 04 Feb 2023 14:07:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:699c8a97647f5789e5850bcf1a3d5afe9730edb654e1ae0714d5bd198a67a3ed`  
		Last Modified: Sat, 04 Feb 2023 06:55:53 GMT  
		Size: 55.0 MB (55025312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed6af97ccf16f95286359a7baad8fc2394e5c5fdeb6b0e3d4faa3a9509aa270`  
		Last Modified: Sat, 04 Feb 2023 14:20:01 GMT  
		Size: 54.6 MB (54635589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15cc928561afd9e2c8cd882fe75e3dfce2188f801e770a7ae388e0bfbfc06413`  
		Last Modified: Sat, 04 Feb 2023 14:20:58 GMT  
		Size: 71.9 MB (71867661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:489340816763d5fe929db0faaeacfc20e624fe95a9c4df6987be258a3ae50a43`  
		Last Modified: Sat, 04 Feb 2023 14:20:50 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-tools-deps-1.11.1.1208-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4c2b02e5bc6528a1378e49fc288111d7c71e1ec5f3e812f8e38738a54f7e22d5
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.4 MB (179395091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f86377d2e7631f8ac6c2faa610ffaf4123ba6a4be705c50d7aa384f4023da5e1`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:26 GMT
ADD file:c5a7c65d67685092faa3456c1a772550aa6d06ac07e1f98a95d39c31e304dbf8 in / 
# Sat, 04 Feb 2023 06:17:27 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 17:02:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 04 Feb 2023 17:02:16 GMT
COPY dir:b6d7e5613532d986930216de9e0fece0632e82564ce7a6a98baf63b4115f840d in /opt/java/openjdk 
# Sat, 04 Feb 2023 17:02:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 04 Feb 2023 17:04:29 GMT
ENV CLOJURE_VERSION=1.11.1.1208
# Sat, 04 Feb 2023 17:04:29 GMT
WORKDIR /tmp
# Sat, 04 Feb 2023 17:04:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4a3b1200c4d633202648dc3db6ed0a1311e75cc4baeee8fce32208c1eaa07537 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Sat, 04 Feb 2023 17:04:46 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 04 Feb 2023 17:04:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fac7262b6510529638951e16807cf1758f42c892ed924e334c27bb8bbcf7d7c2`  
		Last Modified: Sat, 04 Feb 2023 06:21:01 GMT  
		Size: 53.7 MB (53681927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1981d852fd5152d416c9ad7e8c497a15ca9447400a625831b166262fdf77c59d`  
		Last Modified: Sat, 04 Feb 2023 17:15:16 GMT  
		Size: 53.7 MB (53727941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e80c2b265bdd26fd9ec7024e7cc86211efa606924213ac3bdff4561c5f868768`  
		Last Modified: Sat, 04 Feb 2023 17:16:08 GMT  
		Size: 72.0 MB (71984606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef945830266433c44c688de96b1558060dc7632f59e5d5fd36144fd5152abc7b`  
		Last Modified: Sat, 04 Feb 2023 17:16:02 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
