## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:7a312ac4244629f94e1f44c2b4383c3c37d9010be7c739deec65e26b50110fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:fdcd3db2e0d260ce3a97f57888b86fd9ce0553a1c0f5f1173e86b48b6c288d97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.3 MB (285341319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cae279394e0a326525cf858c3632c4d82264bcde3706ee3763eff767af025f8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 Mar 2023 09:01:07 GMT
COPY dir:186a37b080989e6e1268f71ac4b081d0a966a2c5c8b71fa2a808fe83b4537ae1 in /opt/java/openjdk 
# Thu, 02 Mar 2023 09:01:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Mar 2023 19:25:52 GMT
ENV CLOJURE_VERSION=1.11.1.1252
# Tue, 07 Mar 2023 19:25:52 GMT
WORKDIR /tmp
# Tue, 07 Mar 2023 19:26:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "11a5997124d7469578a78f145e68fad6eccd32bf7086979f6abbf19739c85930 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 07 Mar 2023 19:26:11 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 07 Mar 2023 19:26:11 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 07 Mar 2023 19:26:12 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Mar 2023 19:26:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93920d1539d63c977bce91553f85dcaf59acca3032ac3d7434770f05c8b85044`  
		Last Modified: Thu, 02 Mar 2023 09:16:09 GMT  
		Size: 192.4 MB (192438217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e046e43d02f5453735cc62c495677d0b2bfd69dc7a0453a096ac34da6a6caaa0`  
		Last Modified: Tue, 07 Mar 2023 19:36:25 GMT  
		Size: 61.5 MB (61490684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a837e60092ddc5f42f44cb2b9a41055d9e73c4cae334baab4906b26d5b90af4`  
		Last Modified: Tue, 07 Mar 2023 19:36:13 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a37d5f3b540e33c5faa25ffb1eb6c8331199797961a9baa90b3a02464eea26b`  
		Last Modified: Tue, 07 Mar 2023 19:36:13 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b99db88c443d1812558c272077214a40164bba38123445c220d356a0ebdec52b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282929447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44b3133cfaa6bef8553d23549bc66bd5416902fa97e1dc219e92fa23b9f3e69b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 04:54:34 GMT
COPY dir:44544f5117ae50af040f98b1979efcc18f4c9f0c7257bfc4a37b80697337361a in /opt/java/openjdk 
# Thu, 16 Mar 2023 04:54:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 04:57:17 GMT
ENV CLOJURE_VERSION=1.11.1.1252
# Thu, 16 Mar 2023 04:57:17 GMT
WORKDIR /tmp
# Thu, 16 Mar 2023 04:57:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "11a5997124d7469578a78f145e68fad6eccd32bf7086979f6abbf19739c85930 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 16 Mar 2023 04:57:30 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 16 Mar 2023 04:57:30 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 16 Mar 2023 04:57:30 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Mar 2023 04:57:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22fd3d2fa5647f50c6abfaf315449074732a3ae4821d578ce315c4827bc6417a`  
		Last Modified: Thu, 16 Mar 2023 05:08:08 GMT  
		Size: 191.3 MB (191260401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5879d371046e2f489623c4c83b148494f0e7459392125db4744ee00bde279a39`  
		Last Modified: Thu, 16 Mar 2023 05:10:16 GMT  
		Size: 61.6 MB (61605213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f725df624cac82e0f317527d92491a965728b2fa09b8e5940c2ce33136f23e17`  
		Last Modified: Thu, 16 Mar 2023 05:10:10 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a26f6ed108ae5086480024a674b982c70460271086561a5fef4f5ed9b9fa24b`  
		Last Modified: Thu, 16 Mar 2023 05:10:10 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
