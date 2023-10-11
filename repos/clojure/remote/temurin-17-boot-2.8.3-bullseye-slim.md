## `clojure:temurin-17-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:e36e6a110530aeaf1b764fe8f18952c3d524d75fd7878fa4c7c6499cb0d92356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:51843c8e9e9fb1ce3aadab28ba1b35fb3af4583fe48b91e3ce647fc889924265
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236094065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a08c49d2fc491dedb627fdfcfff5913366df3139f4912338462ca2af8f9f78a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Oct 2023 18:57:49 GMT
COPY dir:762e280751e9eaacf2bfae42d6a8cb2a49846426bd7c5675b21a4c0c8ae8fb71 in /opt/java/openjdk 
# Wed, 11 Oct 2023 18:57:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 18:57:51 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 11 Oct 2023 18:57:51 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 11 Oct 2023 18:57:51 GMT
WORKDIR /tmp
# Wed, 11 Oct 2023 18:57:56 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 11 Oct 2023 18:57:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 11 Oct 2023 18:57:56 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 11 Oct 2023 18:58:14 GMT
RUN boot
# Wed, 11 Oct 2023 18:58:14 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 11 Oct 2023 18:58:14 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 11 Oct 2023 18:58:14 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c78747fe143b7fa5e45754d0d844a02627e9122cc66bfd025736a5061056de6`  
		Last Modified: Wed, 11 Oct 2023 19:07:35 GMT  
		Size: 144.8 MB (144775760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c926f6f1af046b37aa468da7d2fd6a970b3c9cce8927b668b4a8b5ffeba23e`  
		Last Modified: Wed, 11 Oct 2023 19:07:23 GMT  
		Size: 1.1 MB (1079451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0fed006f8b1bffdf5380b82d7ede0d067fcb184c77993ab0817fd2e95eafb0d`  
		Last Modified: Wed, 11 Oct 2023 19:07:27 GMT  
		Size: 58.8 MB (58820592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a01cc3ee4c40257b51ca75d0035e55773fffe34ec5400a291818b546fc7484`  
		Last Modified: Wed, 11 Oct 2023 19:07:22 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:17df10a2774645f10c44e85ade98034431410647f0edc81a8ad2ab031b07a543
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 MB (233495426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ec9cf0cb3284f3e9d2258408404b4afa36e2e2736fff55ca2e9ce9428c93699`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Oct 2023 18:51:20 GMT
COPY dir:9add47918f86acac35c907520d4811042633ac78a65fb2fbf0acc7586100f57a in /opt/java/openjdk 
# Wed, 11 Oct 2023 18:51:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 18:51:23 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 11 Oct 2023 18:51:23 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 11 Oct 2023 18:51:23 GMT
WORKDIR /tmp
# Wed, 11 Oct 2023 18:51:28 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 11 Oct 2023 18:51:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 11 Oct 2023 18:51:28 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 11 Oct 2023 18:51:46 GMT
RUN boot
# Wed, 11 Oct 2023 18:51:46 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 11 Oct 2023 18:51:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 11 Oct 2023 18:51:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60a5e42dbe89feb66757745c24f293a64023b9ecb8f3d2eabea16d8087f3809`  
		Last Modified: Wed, 11 Oct 2023 18:59:48 GMT  
		Size: 143.5 MB (143543479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f10d82f0061d2d534bf5b984089fbfdec69a19f7a9b2ea113fd8859a7690ff`  
		Last Modified: Wed, 11 Oct 2023 18:59:39 GMT  
		Size: 1.1 MB (1066859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:900595c1195c1945faf6b192838c00faeff09177d993a137f36fb10ab89cad6d`  
		Last Modified: Wed, 11 Oct 2023 18:59:42 GMT  
		Size: 58.8 MB (58820601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828647a864f23d9c0478ff3f2a2322e5a06352630b4f0de03c6104b436b51a41`  
		Last Modified: Wed, 11 Oct 2023 18:59:38 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
