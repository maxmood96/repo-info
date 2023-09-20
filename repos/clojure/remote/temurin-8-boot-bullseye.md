## `clojure:temurin-8-boot-bullseye`

```console
$ docker pull clojure@sha256:06a56d85d43b2afcfb6523daf161780350f493fd14b72a46ce4a25dfc0062483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:f91a7d9bdf20bf4f8e6f8fe12a290582943b522cf26e785330df25170d5f9c11
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.8 MB (219824375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a0ed2e724a2e191de9561bf773e26d650cf50fe1bbe4c6f432b27510df7414`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 20 Sep 2023 04:55:51 GMT
ADD file:85db4f4c5016f51f7112a5d09cb7d4620f565a1379ae4b8a03c5ffc23886a876 in / 
# Wed, 20 Sep 2023 04:55:51 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:21:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 Sep 2023 07:21:48 GMT
COPY dir:66cfc1773e07dead4d108eefca05e38bbe528aec6797deefc0559c5a4d41e721 in /opt/java/openjdk 
# Wed, 20 Sep 2023 07:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 07:21:49 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 20 Sep 2023 07:21:49 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 20 Sep 2023 07:21:49 GMT
WORKDIR /tmp
# Wed, 20 Sep 2023 07:21:55 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 20 Sep 2023 07:21:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 Sep 2023 07:21:56 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 20 Sep 2023 07:22:18 GMT
RUN boot
# Wed, 20 Sep 2023 07:22:18 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:ddf874abf16cc990e0fd75a154a34ca0a03ee310ad895a18fb62ae15bf4171fb`  
		Last Modified: Wed, 20 Sep 2023 05:00:41 GMT  
		Size: 55.1 MB (55056714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b0aa7fd12821e6e0bd8d864138e0a239c587d7c9e54b266a9620f577d42bf3`  
		Last Modified: Wed, 20 Sep 2023 07:33:50 GMT  
		Size: 103.6 MB (103585016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ad57434bf071b384a66fd1b6680430cfefd6ff8231e0d150f06d742c53b5ac`  
		Last Modified: Wed, 20 Sep 2023 07:33:41 GMT  
		Size: 2.4 MB (2362100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f04cea8bd7ff3c354f23e1c3bbe180c2f377166ea41ba660886b2fcc080e42`  
		Last Modified: Wed, 20 Sep 2023 07:33:45 GMT  
		Size: 58.8 MB (58820545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a11a05416d9ae35329db569c1082b93831a15962a1e1f0740305b1c4ff2ef7a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 MB (217567307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34b07d60f05a9d5deb38895320a8b3d2f83cc7c8622ef99e5f52e65fd344f4cf`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:45 GMT
ADD file:6bc001e951ef1280f566a92e65fcff57aefb8a280aa3510b7cd4b4e0a54c5cff in / 
# Thu, 07 Sep 2023 00:39:46 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 09:03:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 Sep 2023 09:03:53 GMT
COPY dir:b83f0a0f236c1f97de459c8ae266f437d3630abb3700f3b868301c8fe017c49a in /opt/java/openjdk 
# Thu, 07 Sep 2023 09:03:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 09:03:55 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 07 Sep 2023 09:03:55 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 07 Sep 2023 09:03:55 GMT
WORKDIR /tmp
# Thu, 07 Sep 2023 09:04:01 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 07 Sep 2023 09:04:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 07 Sep 2023 09:04:01 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 07 Sep 2023 09:04:25 GMT
RUN boot
# Thu, 07 Sep 2023 09:04:26 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:61c16b7975697b00760ff9536c09eed29b6a76923d4d98be38e9cdc749506417`  
		Last Modified: Thu, 07 Sep 2023 00:43:21 GMT  
		Size: 53.7 MB (53704716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6c9b10898343ff844fa6dfe6448ebad584c5b03b783f81be4ce715ad2b88b1b`  
		Last Modified: Thu, 07 Sep 2023 09:14:27 GMT  
		Size: 102.7 MB (102690511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dda039e2bb980fb309b859d6bd77e0ca131c6961eea402ca81384c316da3038`  
		Last Modified: Thu, 07 Sep 2023 09:14:20 GMT  
		Size: 2.4 MB (2351460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1001eb63f095a0e8b8610f55366ea75cb903596bc76962244fac68c74a6f0e6d`  
		Last Modified: Thu, 07 Sep 2023 09:14:23 GMT  
		Size: 58.8 MB (58820620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
