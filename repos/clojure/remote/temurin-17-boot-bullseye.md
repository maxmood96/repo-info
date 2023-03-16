## `clojure:temurin-17-boot-bullseye`

```console
$ docker pull clojure@sha256:1781c17f7585ac3ebee50364dbee205ad89984edda8ece205688a8ce3712cc6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:dca45bdaa5d14cb1fa6af654b9de83b61188d1e6454dba5910f1f0b27589660d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.7 MB (308666697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc8751376fa572182a582b7e9a4dcc6c67fc4b072702dde246790750905f750`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:45 GMT
ADD file:513c5d5e501279c21a05c1d8b66e5f0b02ee4b27f0b928706d92fd9ce11c1be6 in / 
# Wed, 01 Mar 2023 04:09:46 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:40:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 07:38:54 GMT
COPY dir:d90c8d6564183f8aad11f93ecfb2f7e0eeff18588ff2b62d7ca3d8d30672bc2c in /opt/java/openjdk 
# Thu, 16 Mar 2023 07:38:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 07:38:56 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 16 Mar 2023 07:38:56 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 16 Mar 2023 07:38:56 GMT
WORKDIR /tmp
# Thu, 16 Mar 2023 07:39:02 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 16 Mar 2023 07:39:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Mar 2023 07:39:02 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 16 Mar 2023 07:39:20 GMT
RUN boot
# Thu, 16 Mar 2023 07:39:20 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 16 Mar 2023 07:39:20 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Mar 2023 07:39:21 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:32fb02163b6bb519a30f909008e852354dae10bdfd6b34190dbdfe8f15403ea0`  
		Last Modified: Wed, 01 Mar 2023 04:13:58 GMT  
		Size: 55.0 MB (55045922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4e3bab9252a7f70c657716341799e1034f414d34d365bd602305efb3217645`  
		Last Modified: Thu, 16 Mar 2023 07:53:35 GMT  
		Size: 192.4 MB (192438202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a4588fc95264284cd4f1b36924b977b2414bc92d4790a7c6d2b1d7f5c1708e`  
		Last Modified: Thu, 16 Mar 2023 07:53:21 GMT  
		Size: 2.4 MB (2361747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0811500dde08886cb1364c51db6c23aa41802a3ff73671307696134aed77c53c`  
		Last Modified: Thu, 16 Mar 2023 07:53:25 GMT  
		Size: 58.8 MB (58820426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779dfc06edff0eac4225a68c47e6b3b54ab30354af54c4e3a389d4adb913dc68`  
		Last Modified: Thu, 16 Mar 2023 07:53:21 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:20d171fa49e98b87e7786226e53e2540d22b56c060bb0943017c55476807502b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.1 MB (306135525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48c97c705ce90cbaf1f222a82231b93b55def62a35e4fd69d5bbcd13df6da26`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:30 GMT
ADD file:a6a1df499d0d5b07fb366d776a11c42ddee6261e2425a921041b38e868192770 in / 
# Wed, 01 Mar 2023 02:20:30 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:01:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 04:54:02 GMT
COPY dir:44544f5117ae50af040f98b1979efcc18f4c9f0c7257bfc4a37b80697337361a in /opt/java/openjdk 
# Thu, 16 Mar 2023 04:54:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 04:54:06 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 16 Mar 2023 04:54:06 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 16 Mar 2023 04:54:06 GMT
WORKDIR /tmp
# Thu, 16 Mar 2023 04:54:11 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 16 Mar 2023 04:54:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Mar 2023 04:54:11 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 16 Mar 2023 04:54:28 GMT
RUN boot
# Thu, 16 Mar 2023 04:54:28 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 16 Mar 2023 04:54:28 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Mar 2023 04:54:28 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0f5fe16b1836feccd4765ac5685fc7a7b9c73445cac94fc595d2ffbc3cb59a7a`  
		Last Modified: Wed, 01 Mar 2023 02:23:53 GMT  
		Size: 53.7 MB (53703215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e865ee4af90df7b29aa63a7c22bf36683c14364d7edeb49331fd07b992650cd4`  
		Last Modified: Thu, 16 Mar 2023 05:07:49 GMT  
		Size: 191.3 MB (191260402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be37f4d1fd54d5b328639d509b4a3453a6f2fc3c5fb8df6565ce7bbb790a0b53`  
		Last Modified: Thu, 16 Mar 2023 05:07:38 GMT  
		Size: 2.4 MB (2351026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e24176359526947352e7756b60827ffbca1e637a4f158eda8246682ce477d6`  
		Last Modified: Thu, 16 Mar 2023 05:07:40 GMT  
		Size: 58.8 MB (58820480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9392dc3285c0da3ba7905319dfebe448d83ea524e4da967ae5d9ff2d415687`  
		Last Modified: Thu, 16 Mar 2023 05:07:37 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
