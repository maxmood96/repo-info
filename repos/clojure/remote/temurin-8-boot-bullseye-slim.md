## `clojure:temurin-8-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:8d67cedb1666a4299a2c4463ebf6b40499b2c4fa8cb014722080c718d0e8d395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:edacef66eeb5df93501fe9d184a9f94194ea64837a829906865c0ae8ecd26a23
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.9 MB (145944822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d5e3b3959c14d762765a50759839c80f49ed605be6f1147a3c22a926c9d3ba`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:41:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Mar 2023 07:41:23 GMT
COPY dir:bbb84183d7ea38d81d8401f01e29d08935ee4c8bf6f90c6527579a1554c3bde1 in /opt/java/openjdk 
# Wed, 01 Mar 2023 07:41:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 07:41:23 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Mar 2023 07:41:23 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Mar 2023 07:41:24 GMT
WORKDIR /tmp
# Wed, 01 Mar 2023 07:41:29 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Mar 2023 07:41:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Mar 2023 07:41:29 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Mar 2023 07:41:47 GMT
RUN boot
# Wed, 01 Mar 2023 07:41:48 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210fb3e5d8b959c70a42ac05437d84dbd0b87ade6872fb868c2e70d60c561eb7`  
		Last Modified: Wed, 01 Mar 2023 07:55:19 GMT  
		Size: 54.6 MB (54635554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c0192019cb2f29f89d70524028039846179714e8f0f73436199433a7f0c91e`  
		Last Modified: Wed, 01 Mar 2023 07:55:12 GMT  
		Size: 1.1 MB (1077394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfaef22a939a8563967e41316f799540b7763d9ea643bb3f8107f164a4e60045`  
		Last Modified: Wed, 01 Mar 2023 07:55:15 GMT  
		Size: 58.8 MB (58820471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2dc8211e3d71eaf1e0faef70eb2c3da4e2480f2e3d54801964761e7c845ce760
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143675745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3499c3fbcde931e1ee8a0cf0387472e2f159e364c9521b1df4620a3df1219231`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:02:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Mar 2023 03:02:03 GMT
COPY dir:b6d7e5613532d986930216de9e0fece0632e82564ce7a6a98baf63b4115f840d in /opt/java/openjdk 
# Wed, 01 Mar 2023 03:02:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 03:02:05 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Mar 2023 03:02:05 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Mar 2023 03:02:05 GMT
WORKDIR /tmp
# Wed, 01 Mar 2023 03:02:10 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Mar 2023 03:02:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Mar 2023 03:02:10 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Mar 2023 03:02:27 GMT
RUN boot
# Wed, 01 Mar 2023 03:02:27 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ed8d1b5c6c501960add7e45237e7cb7c527399c9fe073375eb66890797d9b9`  
		Last Modified: Wed, 01 Mar 2023 03:14:20 GMT  
		Size: 53.7 MB (53727906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2b5192d322c72ac1942a42e12b349b6632720946eb54472879c5db6d7b7dec`  
		Last Modified: Wed, 01 Mar 2023 03:14:15 GMT  
		Size: 1.1 MB (1064601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce4553c2f0d322233ac3dcb0af1dcaf3dac59ee6f754696fa4ead955032cc36`  
		Last Modified: Wed, 01 Mar 2023 03:14:18 GMT  
		Size: 58.8 MB (58820424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
