## `clojure:temurin-8-boot-bookworm`

```console
$ docker pull clojure@sha256:25e415de763c83ef30006c064631f4f91fe1568dad9d7f54263f899c30a0e2f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:4072809103cc0e17b733a50eef8abd5fba19df67ddf5bc07f511009b5309f844
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 MB (217527097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2982666182d7c470f5ebc56c5854070815193daf26f53849c7a325f41521888`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:05 GMT
ADD file:6d9e71f0d3afb0b288cf2c06425795d528a142872692072ab1cd1ad275b67d1f in / 
# Wed, 31 Jan 2024 22:35:06 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:41:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 31 Jan 2024 23:42:17 GMT
COPY dir:7a6a87e7bb8d56b27d71b1f614847d2afb4282190a48214e2e48b164fbef7bc7 in /opt/java/openjdk 
# Wed, 31 Jan 2024 23:42:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:42:18 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 31 Jan 2024 23:42:18 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 31 Jan 2024 23:42:18 GMT
WORKDIR /tmp
# Wed, 31 Jan 2024 23:42:26 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 31 Jan 2024 23:42:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 31 Jan 2024 23:42:26 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 31 Jan 2024 23:43:12 GMT
RUN boot
# Wed, 31 Jan 2024 23:43:13 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:6a299ae9cfd996c1149a699d36cdaa76fa332c8e9d66d6678fa9a231d9ead04c`  
		Last Modified: Wed, 31 Jan 2024 22:39:27 GMT  
		Size: 49.6 MB (49583754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638eb245e4649122c3cde175020b7b674960d80dc7cec3f2975ba51d86bc7a4d`  
		Last Modified: Thu, 01 Feb 2024 00:05:10 GMT  
		Size: 103.6 MB (103591896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:247569ce3765ac5a207b33bf6619b9e0eff651091aecb584637c81c310934ce7`  
		Last Modified: Thu, 01 Feb 2024 00:05:03 GMT  
		Size: 5.5 MB (5530435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bcc08d66368a8d8536c47d65b13634e7988e0d2a4987b8c8874c6308fac1ce`  
		Last Modified: Thu, 01 Feb 2024 00:05:05 GMT  
		Size: 58.8 MB (58821012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:85672d5dfd5da67d35dd1f9b9ad1f77140b8256b6e1053a407c3e2040e6f4201
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216464986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:006cb92f7808356672ea8393c0e32b596b92e87aa5f4460e16259a3856bf6264`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:33 GMT
ADD file:051a18650d326af1d23e30c93370e647e62f94887ce43b22e1808052bce4f2a6 in / 
# Thu, 11 Jan 2024 02:40:34 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 07:57:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:06:46 GMT
COPY dir:d67e1a8d4006c4d31bb089f955cdf6054ae46936c41fb4bbc9c830e6a49d11d6 in /opt/java/openjdk 
# Wed, 24 Jan 2024 22:06:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 22:06:49 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 24 Jan 2024 22:06:49 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 24 Jan 2024 22:06:49 GMT
WORKDIR /tmp
# Wed, 24 Jan 2024 22:06:54 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 24 Jan 2024 22:06:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jan 2024 22:06:54 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 24 Jan 2024 22:07:10 GMT
RUN boot
# Wed, 24 Jan 2024 22:07:11 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:5665c1f9a9e17acd68ae05b2839df402eac34afdd095f8c115f09886d757840c`  
		Last Modified: Thu, 11 Jan 2024 02:43:41 GMT  
		Size: 49.6 MB (49592247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64825c6125ababf4dccfeece93eb85e9eebe1896e11602c3484af5db3423db29`  
		Last Modified: Wed, 24 Jan 2024 22:32:08 GMT  
		Size: 102.7 MB (102703042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c7862baa2d7c76f3745fe2722443f30105124feb759e611f18d0d9bfaa382b`  
		Last Modified: Wed, 24 Jan 2024 22:32:01 GMT  
		Size: 5.3 MB (5349375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c1079cef3a549246f60a623245a9f9c90ea71089c48d1965d207aa77913185`  
		Last Modified: Wed, 24 Jan 2024 22:32:05 GMT  
		Size: 58.8 MB (58820322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
