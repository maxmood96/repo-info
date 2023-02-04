## `clojure:temurin-19-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:bd397b4c554dea1fbc5667fd6fd0d1c079fd723403d27907c2aa958887005fbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-19-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:b7a309529ea476e1593417e2f23cb8b6cb48ef2dd3d9db29cf0237a3998b2fb5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.3 MB (317319798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b76ab1323185ef470510e2eb001c4cc766c9f59ded3ca10b60c8c1f59c6a1f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

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
# Sat, 04 Feb 2023 14:14:33 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 04 Feb 2023 14:14:33 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 04 Feb 2023 14:14:33 GMT
WORKDIR /tmp
# Sat, 04 Feb 2023 14:14:39 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 04 Feb 2023 14:14:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 04 Feb 2023 14:14:39 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 04 Feb 2023 14:14:57 GMT
RUN boot
# Sat, 04 Feb 2023 14:14:57 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Sat, 04 Feb 2023 14:14:57 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 04 Feb 2023 14:14:57 GMT
CMD ["repl"]
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
	-	`sha256:e24a7d5cf316c719fe7bcac266330b15c61c451053868b0daa38ebc563844bf7`  
		Last Modified: Sat, 04 Feb 2023 14:25:26 GMT  
		Size: 2.4 MB (2360735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89de8ea8b1f84b2e8331504be43272bf28a706eb9891f58f760ef4b9ab64b224`  
		Last Modified: Sat, 04 Feb 2023 14:25:29 GMT  
		Size: 58.8 MB (58820404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b6d420dc3d84abb6e99c000edcf89a75f0baaaa35436996d401321a3a1ee16`  
		Last Modified: Sat, 04 Feb 2023 14:25:25 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-19-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e5c173a7fb1043309b6bf228139af5a5cb1ae0f1e77e78e5e8d50f63d6a64c60
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.7 MB (314708403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d839ed0c44abafccda871858bada9cd64daf39d226aaa389acd3e25f7f86ee0d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

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
# Sat, 04 Feb 2023 17:10:26 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 04 Feb 2023 17:10:26 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 04 Feb 2023 17:10:26 GMT
WORKDIR /tmp
# Sat, 04 Feb 2023 17:10:31 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 04 Feb 2023 17:10:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 04 Feb 2023 17:10:31 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 04 Feb 2023 17:10:47 GMT
RUN boot
# Sat, 04 Feb 2023 17:10:47 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Sat, 04 Feb 2023 17:10:47 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 04 Feb 2023 17:10:47 GMT
CMD ["repl"]
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
	-	`sha256:247599b1658a096c5eaa3665403efe378e7b42d6f2233798eed32826c89f06b9`  
		Last Modified: Sat, 04 Feb 2023 17:19:57 GMT  
		Size: 2.4 MB (2350653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636cf8e3d589a19625f2ad720be426efcf43cdbb93e4749bed61416d44cf802f`  
		Last Modified: Sat, 04 Feb 2023 17:19:59 GMT  
		Size: 58.8 MB (58820224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20151ccf5d48848e705c94086c5f749835bbbaeaf031f557e059611d5cbf7445`  
		Last Modified: Sat, 04 Feb 2023 17:19:56 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
