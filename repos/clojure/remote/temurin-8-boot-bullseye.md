## `clojure:temurin-8-boot-bullseye`

```console
$ docker pull clojure@sha256:332806ad01bac1660836b07c6e87dd7d1c5f909ad9a35e11d7c93b3f964cd964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:fddb734f73a96d34b4ddb9f8904b793543c975fad0070572638bc3666eda3558
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219870045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2c1f2b1f2ae8334a068d91954c60b8b481f6a53f28c73e709ecce8e8be6617`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:59 GMT
ADD file:8efdcc3201e79c8a09fc9c1ade08492ea33f838047332a7c61988f6357339dee in / 
# Wed, 10 Apr 2024 01:50:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:18:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 06:18:02 GMT
COPY dir:7a6a87e7bb8d56b27d71b1f614847d2afb4282190a48214e2e48b164fbef7bc7 in /opt/java/openjdk 
# Wed, 10 Apr 2024 06:18:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:18:03 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 10 Apr 2024 06:18:03 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 10 Apr 2024 06:18:03 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 06:18:10 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 10 Apr 2024 06:18:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 10 Apr 2024 06:18:10 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 10 Apr 2024 06:18:30 GMT
RUN boot
# Wed, 10 Apr 2024 06:18:30 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:ac323bdaa10f869bd9e7adecd8f5326e44acc4c59168868108b1cdf3891089cc`  
		Last Modified: Wed, 10 Apr 2024 01:55:52 GMT  
		Size: 55.1 MB (55090264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559c58dda9fddadf47ec61579a42c98d54a9dbbe36bc23256a7472bdbc9d7d1a`  
		Last Modified: Wed, 10 Apr 2024 06:39:37 GMT  
		Size: 103.6 MB (103591916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba1ca3e7ae42dfefa1da9db9174077e43a62203146af5e7d320234a350784ff`  
		Last Modified: Wed, 10 Apr 2024 06:39:29 GMT  
		Size: 2.4 MB (2367286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:985568f6d3d181254aa023588318a4c1daed6131c6c4d3c10ff0d528d2e67367`  
		Last Modified: Wed, 10 Apr 2024 06:39:32 GMT  
		Size: 58.8 MB (58820579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:974cedff1cdea526a8062bf3193fa763d831784b64b17fa32e45561031636257
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 MB (217608572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da8afcc2d741766b0e783c3075e096a427aa4807aa4d7b00b2c4dce9b7ba8b4c`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:30 GMT
ADD file:6fedb173fe261ff0e13b004ca692b7edcc74dcc3c4384fee092b96ef9508992c in / 
# Wed, 10 Apr 2024 00:40:30 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:39:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 04:39:24 GMT
COPY dir:d67e1a8d4006c4d31bb089f955cdf6054ae46936c41fb4bbc9c830e6a49d11d6 in /opt/java/openjdk 
# Wed, 10 Apr 2024 04:39:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 04:39:27 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 10 Apr 2024 04:39:27 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 10 Apr 2024 04:39:27 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 04:39:32 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 10 Apr 2024 04:39:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 10 Apr 2024 04:39:32 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 10 Apr 2024 04:39:50 GMT
RUN boot
# Wed, 10 Apr 2024 04:39:51 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:197947a07d5f6c6ff020ca65dcea4e52671f85f67bee1b59af46cb0dc36580d9`  
		Last Modified: Wed, 10 Apr 2024 00:44:24 GMT  
		Size: 53.7 MB (53729176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4356e798bd14d733012e92b998ac0cebce255bbc6b9b566fbd468609bb72b42`  
		Last Modified: Wed, 10 Apr 2024 04:58:22 GMT  
		Size: 102.7 MB (102703041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea4acff61dc5e1e02f1b10ade5012515c76f7c7913f46b6dff282d8129909d7`  
		Last Modified: Wed, 10 Apr 2024 04:58:16 GMT  
		Size: 2.4 MB (2355774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd2c89a5046fb67e4938ee19b67d5a37ff31e54142b72996a99ed55ccbdb952`  
		Last Modified: Wed, 10 Apr 2024 04:58:18 GMT  
		Size: 58.8 MB (58820581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
