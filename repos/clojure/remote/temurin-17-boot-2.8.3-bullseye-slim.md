## `clojure:temurin-17-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:1f1fdb21aabb0ea599cd0cda0824cd8ce7516183b739d2a0570b26f0f8925218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:64ebecd14ac371922dda8f4a99560edaa113d16a4e9e5871292f0c528fa1a25d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.7 MB (283747974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62bc6215ee5b586c427fa71a179b14808697a18873a2ec5c3d3dac05f73ee36e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Mar 2023 07:47:19 GMT
COPY dir:5cf52f938fe415b0022fbccb8cf978562c503c0b8313cc9dedf46c1c4edb35cf in /opt/java/openjdk 
# Wed, 01 Mar 2023 07:47:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 07:47:21 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Mar 2023 07:47:21 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Mar 2023 07:47:21 GMT
WORKDIR /tmp
# Wed, 01 Mar 2023 07:47:27 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Mar 2023 07:47:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Mar 2023 07:47:27 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Mar 2023 07:47:45 GMT
RUN boot
# Wed, 01 Mar 2023 07:47:45 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 01 Mar 2023 07:47:45 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 01 Mar 2023 07:47:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f039bcab9992b3a477fd101e656d4f5ad27c8c30323fd021475c390e3d41213e`  
		Last Modified: Wed, 01 Mar 2023 07:58:57 GMT  
		Size: 192.4 MB (192438214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe877147dcd0058221e9f9751e57f1000d59c5364fea20770cb875ddeeb51dd6`  
		Last Modified: Wed, 01 Mar 2023 07:58:44 GMT  
		Size: 1.1 MB (1077394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67ccd605e1b5258d903976165ca126a2a51a18b359dadbc9a5d7ccbf12022e3`  
		Last Modified: Wed, 01 Mar 2023 07:58:47 GMT  
		Size: 58.8 MB (58820566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4c205b9dddbb34ea41f762bcd9f13da12f24b26e12651ab02e29383b323f8c`  
		Last Modified: Wed, 01 Mar 2023 07:58:43 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8f9b03acdaf4a303b8e69a27d14a6cee7164f48e45c1ba5fd3a40a0a0c7d8c73
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.2 MB (281208889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547de7ad3548dce6431668f547d78690266c2c4b4658254610cb4c397f153feb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Mar 2023 03:07:09 GMT
COPY dir:a1bd99c3d82513db94430c73467e1e5c69ea4624d0489571d594afe503e15dc5 in /opt/java/openjdk 
# Wed, 01 Mar 2023 03:07:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 03:07:13 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Mar 2023 03:07:13 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Mar 2023 03:07:14 GMT
WORKDIR /tmp
# Wed, 01 Mar 2023 03:07:18 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Mar 2023 03:07:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Mar 2023 03:07:18 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Mar 2023 03:07:36 GMT
RUN boot
# Wed, 01 Mar 2023 03:07:36 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 01 Mar 2023 03:07:36 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 01 Mar 2023 03:07:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fea299b8494f8b0756cbfb644eec65ca18c102ef09fafc09ea59e9d201162b5`  
		Last Modified: Wed, 01 Mar 2023 03:17:40 GMT  
		Size: 191.3 MB (191260427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f02eda8a922dd7120c09b57f9c839d9bca5c9ba62784009164ddae4e02e22d7`  
		Last Modified: Wed, 01 Mar 2023 03:17:28 GMT  
		Size: 1.1 MB (1064589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48a42c2ee0d57f2d4b6cb4d63afa8abd094e3e6d466d36c655bcdf077ed77de3`  
		Last Modified: Wed, 01 Mar 2023 03:17:30 GMT  
		Size: 58.8 MB (58820661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4daadb5ee5298ac620c66d9ed8a6be116a8cf3ee371c410de0eae9f4e3ba8f`  
		Last Modified: Wed, 01 Mar 2023 03:17:28 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
