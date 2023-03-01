## `clojure:temurin-19-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:d26d337b35946955c8906e059e58acac483d8af6c572389dc60be7044bd9d7e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-19-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c71f4dc3c0f42f446e0f1f98c1a80d77ac8a592a5a75af34afde536649a6a295
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.4 MB (292422639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50a798def4ba5de4c8a0062a8d01a81a0c4583ee00dd8d33040fd5c28d6f7f0f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Mar 2023 07:50:20 GMT
COPY dir:94cb5af8175285c10c94286222d8a35302f3f8c290e00011a75c67156659d6ab in /opt/java/openjdk 
# Wed, 01 Mar 2023 07:50:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 07:50:22 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Mar 2023 07:50:22 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Mar 2023 07:50:22 GMT
WORKDIR /tmp
# Wed, 01 Mar 2023 07:50:28 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Mar 2023 07:50:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Mar 2023 07:50:28 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Mar 2023 07:50:45 GMT
RUN boot
# Wed, 01 Mar 2023 07:50:45 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 01 Mar 2023 07:50:45 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 01 Mar 2023 07:50:45 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b3ccae27fe03c16494d3c8f769e2249b243d16240726cb9587a989c25ac8d0`  
		Last Modified: Wed, 01 Mar 2023 08:01:12 GMT  
		Size: 201.1 MB (201112994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa05e0f84760dab73538abb4a7a6f179ef6b0782895f88768d4d198e71d55ce0`  
		Last Modified: Wed, 01 Mar 2023 08:00:58 GMT  
		Size: 1.1 MB (1077385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f52a3350b54149c23953c0aef058f264f53f6d74b1c5be608041aaa0735715`  
		Last Modified: Wed, 01 Mar 2023 08:01:01 GMT  
		Size: 58.8 MB (58820457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d66a62abc3d469facdaa93bb7e6aa72062e03d49ab3cd5f0b3c33d82962a4c`  
		Last Modified: Wed, 01 Mar 2023 08:00:57 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-19-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f29d605f91295e9c727b90f0ccc1472f26a59c349bdacfca89c8339f4d77e1c2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 MB (289803473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d2c8067eb2c7fa9b74196ee2a016681052ded75d6d4934753d0b28e49e03f4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Mar 2023 03:09:45 GMT
COPY dir:9a6a873ca11063f6f04e7f088397a1fce771e2b1aa8590b72eb07158cfac883f in /opt/java/openjdk 
# Wed, 01 Mar 2023 03:09:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 03:09:49 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Mar 2023 03:09:49 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Mar 2023 03:09:49 GMT
WORKDIR /tmp
# Wed, 01 Mar 2023 03:09:54 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Mar 2023 03:09:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Mar 2023 03:09:54 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Mar 2023 03:10:10 GMT
RUN boot
# Wed, 01 Mar 2023 03:10:11 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 01 Mar 2023 03:10:11 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 01 Mar 2023 03:10:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee23dab4c9395b25d6fc9f10fb3db021a5fb12f2747057b25dfcd66add5df0fd`  
		Last Modified: Wed, 01 Mar 2023 03:19:32 GMT  
		Size: 199.9 MB (199855200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:240c0137fdc38d9314ba6eb91b44574ea66a1e62051a9987a1e92375b9c17087`  
		Last Modified: Wed, 01 Mar 2023 03:19:20 GMT  
		Size: 1.1 MB (1064586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:333431c7d4ac1a8d242676e73239ec35e620573bace9efd1c14419ce8a2a6212`  
		Last Modified: Wed, 01 Mar 2023 03:19:23 GMT  
		Size: 58.8 MB (58820472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686f5f0a50dc1315220e9ff587cf356799f20e1dd079c3978dcf02cd5e40e4d6`  
		Last Modified: Wed, 01 Mar 2023 03:19:19 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
