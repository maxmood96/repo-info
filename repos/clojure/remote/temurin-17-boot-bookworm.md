## `clojure:temurin-17-boot-bookworm`

```console
$ docker pull clojure@sha256:ddca9429f8031c3aa93ecdbd36cdef3ddef72b6625ee9e264d0c1d5668e2e7d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:936489524c270fc4bd3da24b32777dda4407cef79599e139c6af82e7bc8bc019
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.8 MB (258801578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c28e3e563bba89811425cb4e99eb9deb160d607deacf9f658abb72e1452c29b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:34 GMT
ADD file:ca6d1f0f80dd6c91b8ba1d1adf77d7af6d0e5f2f493a2858e384c11874314395 in / 
# Wed, 10 Apr 2024 01:50:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:16:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 06:28:24 GMT
COPY dir:88c5118aff6896f6ed535dcde576d68ef88ded459cca013e0f9beb3e430ebb52 in /opt/java/openjdk 
# Wed, 10 Apr 2024 06:28:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:28:25 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 10 Apr 2024 06:28:25 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 10 Apr 2024 06:28:25 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 06:28:31 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 10 Apr 2024 06:28:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 10 Apr 2024 06:28:32 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 10 Apr 2024 06:28:49 GMT
RUN boot
# Wed, 10 Apr 2024 06:28:49 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 10 Apr 2024 06:28:49 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 10 Apr 2024 06:28:49 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:609c73876867487da051ad470002217da69bb052e2538710ade0730d893ff51f`  
		Last Modified: Wed, 10 Apr 2024 01:55:11 GMT  
		Size: 49.6 MB (49560360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b999bb736fb5383b280a1b864a56049c77d7594a2a6e4588d3878a085cd0164`  
		Last Modified: Wed, 10 Apr 2024 06:45:39 GMT  
		Size: 144.9 MB (144893128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846964a642b7e8a673711d2896ec752c3a0bcefa824a4c4d793c2241ec1a14e5`  
		Last Modified: Wed, 10 Apr 2024 06:45:29 GMT  
		Size: 5.5 MB (5527363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a6908d7515606db7987f2c66b20758be972da49e72d63357629ac6776dd7e7`  
		Last Modified: Wed, 10 Apr 2024 06:45:31 GMT  
		Size: 58.8 MB (58820328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3728f93cd576dbd67cc40d1948e635adbaf1af3a4e6bbc3ffc58ee6670f627`  
		Last Modified: Wed, 10 Apr 2024 06:45:28 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0d85e6ed00d8337c0e68f8ebc7b9b544660f4287535591d8391657fa68c3ae81
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.5 MB (257487556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50468be07a0067a4b38bfb970483ec6d4e671d2ca4f42335ee8f1cc5ac193f69`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:12 GMT
ADD file:d795219dc83a41b5bb4106e62eebd31ceef0aae1b81541156eae5fe98e89337c in / 
# Wed, 10 Apr 2024 00:40:13 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:37:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 04:48:10 GMT
COPY dir:a5d0039514ccd79689a0ea6094d70ca92113e8cbcc38d473b7c0fcc04a1f496a in /opt/java/openjdk 
# Wed, 10 Apr 2024 04:48:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 04:48:14 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 10 Apr 2024 04:48:14 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 10 Apr 2024 04:48:14 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 04:48:19 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 10 Apr 2024 04:48:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 10 Apr 2024 04:48:20 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 10 Apr 2024 04:48:37 GMT
RUN boot
# Wed, 10 Apr 2024 04:48:37 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 10 Apr 2024 04:48:37 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 10 Apr 2024 04:48:37 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1e92f3a395ff98a929e797a3c392bb6d0f05531068d34b81d3cd41ed6ce82ca4`  
		Last Modified: Wed, 10 Apr 2024 00:43:42 GMT  
		Size: 49.6 MB (49596265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9944fa1d82dffccbdecd6f3662116d2cade312ebe17866b01cd24bf860a8bcc`  
		Last Modified: Wed, 10 Apr 2024 05:04:25 GMT  
		Size: 143.7 MB (143720939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bb223a24324a000d626427b070d27a3fd9e3d9db7a59c00ff75fa8c30a4bde`  
		Last Modified: Wed, 10 Apr 2024 05:04:16 GMT  
		Size: 5.3 MB (5349417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a6c26d6a97949e65e7d304956ce6c0512be7b3f9159f1f8fbe6cb39919aa6b`  
		Last Modified: Wed, 10 Apr 2024 05:04:19 GMT  
		Size: 58.8 MB (58820536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9e5c54695ca89fe8e4418545a5266d439bfcaed76549aff33847d82198106a7`  
		Last Modified: Wed, 10 Apr 2024 05:04:15 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
