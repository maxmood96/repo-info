## `clojure:temurin-11-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:3acb2d9818344f93379c27a53532b9cc95758e5cbfd0114283d3da22de0cc6c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:18c36b6c79993bc0af257a4311f233d85caaf33eda664990421933d8e4ebf9c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236147426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:832a9eed0ceb8417ef792c4f2bedf3abd60a7c43b26a54beccd44d50f95b20f0`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:02:38 GMT
COPY dir:72d046f3e284b8eca8066a837ab8a68f91b4cf5355de7f6803a8ee9b7ce3d682 in /opt/java/openjdk 
# Wed, 16 Aug 2023 18:05:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 18:05:05 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 16 Aug 2023 18:05:05 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 16 Aug 2023 18:05:05 GMT
WORKDIR /tmp
# Wed, 16 Aug 2023 18:05:11 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 16 Aug 2023 18:05:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 16 Aug 2023 18:05:11 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 16 Aug 2023 18:05:31 GMT
RUN boot
# Wed, 16 Aug 2023 18:05:31 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209f416efba54d09e37495a54336ac55d40fc467f753f97e78f060748b4513e5`  
		Last Modified: Wed, 16 Aug 2023 17:06:20 GMT  
		Size: 144.8 MB (144831672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d22c399f44847c6dfe3a825ca2d24fd7b7a00909391b6ca7dcd19085208a24`  
		Last Modified: Wed, 16 Aug 2023 18:15:39 GMT  
		Size: 1.1 MB (1077554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16ebc2065e4ccee2320a9c6d4c788d02ff2461724694d661d91283a4280b2bb`  
		Last Modified: Wed, 16 Aug 2023 18:15:43 GMT  
		Size: 58.8 MB (58820522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0e5b9740376e179ff4dfce30978a053fc786aaea52937252a47cf6adb8139d87
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231513361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ebdbcb54fd9e1bb1947edac961320a586716b9a13bedc2bad928fe7a1c69890`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:22:18 GMT
COPY dir:6acc55ac013a722a8db4af8f0ce8de9270cd9aeb372e6c734b449d15adcc5218 in /opt/java/openjdk 
# Wed, 16 Aug 2023 17:22:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 17:22:21 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 16 Aug 2023 17:22:21 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 16 Aug 2023 17:22:21 GMT
WORKDIR /tmp
# Wed, 16 Aug 2023 17:22:26 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 16 Aug 2023 17:22:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 16 Aug 2023 17:22:26 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 16 Aug 2023 17:22:44 GMT
RUN boot
# Wed, 16 Aug 2023 17:22:45 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1e09cb30a1ef0915a1ffb7a7e09dbfbbd6ca50b0de70ef22c1ecb37d83b229`  
		Last Modified: Wed, 16 Aug 2023 17:31:53 GMT  
		Size: 141.6 MB (141565229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4090bdd24a4cef221a5363e3a65c032a4581830eaf62aa499e1dce08a59176c7`  
		Last Modified: Wed, 16 Aug 2023 17:31:43 GMT  
		Size: 1.1 MB (1064823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7225500deeb83354f8de149044e8025798f38a361418677acab6a21f4bc87d08`  
		Last Modified: Wed, 16 Aug 2023 17:31:48 GMT  
		Size: 58.8 MB (58820493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
