## `clojure:temurin-8-boot-bullseye`

```console
$ docker pull clojure@sha256:6daaa56dcf61ffa0f1939f970563320d67cf20a5edb783efe0c2b835f0da32d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:664f4da1b33d2a39873668d7665c496523cc33ee1e1b1d8d97160aa4c10a699b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.8 MB (219752139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20dc41b8d2b05a02a24aa4ed89aa5580a692d60081bbc15da742ec039b5b11ad`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:43 GMT
ADD file:abc6873c98339a3c496cb75ec2528e65ebe1f20d2cea777033f86dcd55d73da5 in / 
# Tue, 15 Nov 2022 04:04:43 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 17:50:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 17:50:31 GMT
COPY dir:53540f2d79f4eef9b2bf8c4b39ecdbbd82fb14bfcf951e14853afffd2efa2ecb in /opt/java/openjdk 
# Tue, 15 Nov 2022 17:50:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 17:50:33 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 15 Nov 2022 17:50:33 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 15 Nov 2022 17:50:33 GMT
WORKDIR /tmp
# Tue, 15 Nov 2022 17:50:40 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 15 Nov 2022 17:50:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 15 Nov 2022 17:50:40 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 15 Nov 2022 17:51:06 GMT
RUN boot
# Tue, 15 Nov 2022 17:51:06 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:a8ca11554fce00d9177da2d76307bdc06df7faeb84529755c648ac4886192ed1`  
		Last Modified: Tue, 15 Nov 2022 04:08:24 GMT  
		Size: 55.0 MB (55038615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc3c1232a71c325547fbbeb2b9de7293ab2fac0425f4b1e29f33f7ba72c3686`  
		Last Modified: Tue, 15 Nov 2022 18:06:30 GMT  
		Size: 103.5 MB (103530622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344df9d1f16e360b730a29b01ba5f404fd25f5899e52090f2d848494ac9e62e0`  
		Last Modified: Tue, 15 Nov 2022 18:06:21 GMT  
		Size: 2.4 MB (2362098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac0c9fa884dff120ed823aa34ee3bca8c3479cf7dcad4c2be37a8a0ac854407`  
		Last Modified: Tue, 15 Nov 2022 18:06:24 GMT  
		Size: 58.8 MB (58820804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cc9041c109a644fa5e440a7e62c993bceb9aa5475d70891e3f2163fe69f224a2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 MB (217499966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ee0b82bac020a407dc776becbc62d07d2dc54c7ca4765f4522d37ac60dc9b8`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:12 GMT
ADD file:1f3a7177f64e1adda3e7a541c93dd4322c6ecb4f00f7b015665df2c0c08b59a5 in / 
# Tue, 15 Nov 2022 01:41:12 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 05:48:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 05:48:27 GMT
COPY dir:8a3fd802e7e57a45d80b19a89e91b421563b952585d39995819354f278317671 in /opt/java/openjdk 
# Tue, 15 Nov 2022 05:48:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 05:48:30 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 15 Nov 2022 05:48:30 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 15 Nov 2022 05:48:30 GMT
WORKDIR /tmp
# Tue, 15 Nov 2022 05:48:35 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 15 Nov 2022 05:48:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 15 Nov 2022 05:48:35 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 15 Nov 2022 05:49:16 GMT
RUN boot
# Tue, 15 Nov 2022 05:49:16 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:077c13527d405646e2f6bb426e04716ae4f8dd2fdd8966dcb0194564a2b57896`  
		Last Modified: Tue, 15 Nov 2022 01:44:12 GMT  
		Size: 53.7 MB (53699862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046fabb8a21ba00eac3c1d47151d833a4f75a4a53165082db8407708793358bf`  
		Last Modified: Tue, 15 Nov 2022 06:01:34 GMT  
		Size: 102.6 MB (102626606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d0b51bafe27d21744296eef25f4c6184aa3339f54ee01843ee4003e8490adb`  
		Last Modified: Tue, 15 Nov 2022 06:01:27 GMT  
		Size: 2.4 MB (2352260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdacf89c997b10916f66c7ad65997b7ce4dfdb028742e61044ba69603ad7e87`  
		Last Modified: Tue, 15 Nov 2022 06:01:30 GMT  
		Size: 58.8 MB (58821238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
