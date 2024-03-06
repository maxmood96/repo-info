## `clojure:temurin-11-boot-2.8.3-bookworm`

```console
$ docker pull clojure@sha256:0f30159584ad23397c42ae7dde938914610f9f6b3e194ef5e9d69f165900a621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:0ccb22ef9e7573db80ec6cadf0e0197c4d39bc24d168734916809b7bd375d513
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259171482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5398e63b936004159a3dfd4b2482988c6c5b82cccd43136955e9cbcc57669a2`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:46:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 14:01:26 GMT
COPY dir:9807503b62b5ec57f5790350ba2323b4402a31264d57970336b28a606d7a3a68 in /opt/java/openjdk 
# Wed, 06 Mar 2024 14:01:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 14:01:27 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 06 Mar 2024 14:01:27 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 06 Mar 2024 14:01:27 GMT
WORKDIR /tmp
# Wed, 06 Mar 2024 14:01:36 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 06 Mar 2024 14:01:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 06 Mar 2024 14:01:36 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 06 Mar 2024 14:01:55 GMT
RUN boot
# Wed, 06 Mar 2024 14:01:56 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fef8f12b6baebdea896c533d306f9a4400d48aa6fc581898133c81fd740eeae`  
		Last Modified: Wed, 06 Mar 2024 14:22:50 GMT  
		Size: 145.3 MB (145271180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf9dbbb49cfe2b36cbe83f660daee0a03eae0bbb151d4d26ad0e256476f882d`  
		Last Modified: Wed, 06 Mar 2024 14:22:40 GMT  
		Size: 5.5 MB (5527126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bfbb4122cb49b1acffb3e89b2d41598d938e90bb50139a73fca2e811c57fe9d`  
		Last Modified: Wed, 06 Mar 2024 14:22:42 GMT  
		Size: 58.8 MB (58820571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:65939180069337241f129def219fc81a9b309912232dcf8d18b3293f0137a50f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255769455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4424e5f7f57ac9cd644c22b567afc933a03ce531171b790dd8195f0c8ff897c4`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:10 GMT
ADD file:73b36e8089732e9bb253d9a9db76cc1cf5c430bd49647849b77924cd5fdaf8ae in / 
# Tue, 13 Feb 2024 00:41:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:53:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 13:15:40 GMT
COPY dir:774c748cac67d918432726696917d770e1c557a90a62f56899a68f5b5861f304 in /opt/java/openjdk 
# Wed, 06 Mar 2024 13:15:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 13:15:44 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 06 Mar 2024 13:15:44 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 06 Mar 2024 13:15:44 GMT
WORKDIR /tmp
# Wed, 06 Mar 2024 13:15:51 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 06 Mar 2024 13:15:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 06 Mar 2024 13:15:51 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 06 Mar 2024 13:16:08 GMT
RUN boot
# Wed, 06 Mar 2024 13:16:09 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:c2964e85ea54bbef26d274e85fa0a3fde68f074e0774d0729e6ebe341e24eee1`  
		Last Modified: Tue, 13 Feb 2024 00:44:29 GMT  
		Size: 49.6 MB (49590965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b86d284bc578f785e758077d880420331cfdd72f8658c791ddced4e9345fc5`  
		Last Modified: Wed, 06 Mar 2024 13:33:36 GMT  
		Size: 142.0 MB (142008471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57546bc42819c70bdd1f5d1b08a3df16b399000edbb92d4bb58dbbe2cba7e1f7`  
		Last Modified: Wed, 06 Mar 2024 13:33:27 GMT  
		Size: 5.3 MB (5349520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c51e63e71405a9b51152fd9eea238ee752e1e8973ee76ab43fd98d59c1fb93`  
		Last Modified: Wed, 06 Mar 2024 13:33:29 GMT  
		Size: 58.8 MB (58820499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
