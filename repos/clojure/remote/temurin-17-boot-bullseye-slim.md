## `clojure:temurin-17-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:306693202351df6a9f1dca2ddf6e84bad56db592667a138e1ca66509a7feeb65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:79899fd28de78710e2bb10a43bb9dd9a1420d330dec606357c0421e85ccf85ef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.2 MB (236219336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5dc40cc998420bfaced9230db98734e0884a9f38712d13a27521fe36e1b7f6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Apr 2024 11:04:33 GMT
COPY dir:634e6dc1071a76d830a1c58e20efb6c42c0d02beb44d214374fc7817b69efa15 in /opt/java/openjdk 
# Tue, 16 Apr 2024 11:04:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 11:04:34 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 16 Apr 2024 11:04:34 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 16 Apr 2024 11:04:35 GMT
WORKDIR /tmp
# Tue, 16 Apr 2024 11:04:40 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 16 Apr 2024 11:04:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Apr 2024 11:04:40 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 16 Apr 2024 11:04:58 GMT
RUN boot
# Tue, 16 Apr 2024 11:04:58 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 16 Apr 2024 11:04:58 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Apr 2024 11:04:58 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:004fb25e77fd8165a70ae4b224760af36beadedcfcac6da9b3bc5ae18dff8ab1`  
		Last Modified: Tue, 16 Apr 2024 11:22:55 GMT  
		Size: 144.9 MB (144893102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53573ba07f5b853cc0e039efde5f988ed96de38b3b4d5a2024198726ecfcac9`  
		Last Modified: Tue, 16 Apr 2024 11:22:43 GMT  
		Size: 1.1 MB (1077715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:927d5f7b85047d4a53fcfb5b4ce321e860cc32bc859e75205f3ec8d4311a1a75`  
		Last Modified: Tue, 16 Apr 2024 11:22:47 GMT  
		Size: 58.8 MB (58820380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7719421dd17a4eee91e6d810a14bfa28fc7cc62ea3e165ac7743aaafacbba25`  
		Last Modified: Tue, 16 Apr 2024 11:22:43 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cb7ff36a59039c83933133efac6f6521c1ffd7ce679d171cb5dea9a62b2af3a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233682959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8a7f93057e7c63bf1f517e57b2ebe6a5dd6b701e3aedb1f058ed265e440803`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:39:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Apr 2024 06:41:34 GMT
COPY dir:00f694ce512d2e49bdb0844fa7f6d54a4b39a35418d1c6b32b574b5d44cfc1da in /opt/java/openjdk 
# Tue, 16 Apr 2024 06:41:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 06:41:37 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 16 Apr 2024 06:41:37 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 16 Apr 2024 06:41:37 GMT
WORKDIR /tmp
# Tue, 16 Apr 2024 06:41:42 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 16 Apr 2024 06:41:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Apr 2024 06:41:42 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 16 Apr 2024 06:41:59 GMT
RUN boot
# Tue, 16 Apr 2024 06:41:59 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 16 Apr 2024 06:41:59 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Apr 2024 06:41:59 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbeb97876b5dac3782043f1df2ea53c545e7b19ee4061e684a03256552ae431`  
		Last Modified: Tue, 16 Apr 2024 06:57:27 GMT  
		Size: 143.7 MB (143720862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a09f661cae0d0e8b553180dafec1f1a9db3045c756e36ec0053aa0e70c01e4`  
		Last Modified: Tue, 16 Apr 2024 06:57:18 GMT  
		Size: 1.1 MB (1064970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78be5403640314994441a10747a7583443c5d7d729e6e928698bb9276427b48d`  
		Last Modified: Tue, 16 Apr 2024 06:57:21 GMT  
		Size: 58.8 MB (58820422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5364450733274f573bb252973bd8f0345f920e2a711df142eabfa9c8fd8a133`  
		Last Modified: Tue, 16 Apr 2024 06:57:18 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
