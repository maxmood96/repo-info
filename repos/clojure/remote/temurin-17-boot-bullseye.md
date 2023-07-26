## `clojure:temurin-17-boot-bullseye`

```console
$ docker pull clojure@sha256:8a67742756b99946c458c5ab00913dd97a1c8a14025dbbedd42fe70225adb67e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:7d735fe9c9dce59bdcca8d2e32e6def4213e18209d293784da93f8b972b4faba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.0 MB (261012156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18f3636479d83af5d69cf49b7a38c7963e16ceda6e5ef22ba8280b2d80608d98`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:09 GMT
ADD file:b7c0be2bb90e88689b1c16da78dea0b85760b55b90ef2e5bc4a529c89e4fa25b in / 
# Tue, 04 Jul 2023 01:20:10 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:59:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Jul 2023 23:32:00 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Tue, 25 Jul 2023 23:32:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jul 2023 23:32:01 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 25 Jul 2023 23:32:01 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 25 Jul 2023 23:32:01 GMT
WORKDIR /tmp
# Tue, 25 Jul 2023 23:32:07 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 25 Jul 2023 23:32:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 25 Jul 2023 23:32:07 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 25 Jul 2023 23:32:26 GMT
RUN boot
# Tue, 25 Jul 2023 23:32:26 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 25 Jul 2023 23:32:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 25 Jul 2023 23:32:26 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:34df401c391c7595044379e04e8ad4856a5a3974cdbf5a160f0a204d761e88aa`  
		Last Modified: Tue, 04 Jul 2023 01:25:21 GMT  
		Size: 55.1 MB (55055300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92cd483271903c7fa46b78975e71796541dd2c0716e96e558fb9b36d3d485a14`  
		Last Modified: Tue, 25 Jul 2023 23:42:00 GMT  
		Size: 144.8 MB (144773747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4befee9cd6cecd03b3860faf02ac8388fb9ba705a060de20466e12360f46039`  
		Last Modified: Tue, 25 Jul 2023 23:41:49 GMT  
		Size: 2.4 MB (2362067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1fcad263defa1f6c275e2de09080e579b97e724a4b8307543812eabf600550`  
		Last Modified: Tue, 25 Jul 2023 23:41:52 GMT  
		Size: 58.8 MB (58820643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8f22320944d4afe9e0cf9edc815c01f08a010c4c86c23fe4823a3199583306`  
		Last Modified: Tue, 25 Jul 2023 23:41:48 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:88241e76b501d7bc6ec51098d1d797720497875c21d02d31ab19ae622f682f08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258415120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57d08a32a98b5a80e9aae34aad42134fcde916ec0078c57646677d1af4be6c8f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:43 GMT
ADD file:e626446584d8094b7b58d72a717380ca64d3e9ab924fc625406fe26a83fe1d8b in / 
# Tue, 04 Jul 2023 01:57:43 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:43:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 25 Jul 2023 22:57:36 GMT
COPY dir:ea833e6c6c81bc32cfded5d05d30b781acc802f6c770c2720afc9a9f14f4a7d5 in /opt/java/openjdk 
# Tue, 25 Jul 2023 22:57:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jul 2023 22:57:40 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 25 Jul 2023 22:57:40 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 25 Jul 2023 22:57:40 GMT
WORKDIR /tmp
# Tue, 25 Jul 2023 22:57:45 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 25 Jul 2023 22:57:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 25 Jul 2023 22:57:45 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 25 Jul 2023 22:58:33 GMT
RUN boot
# Tue, 25 Jul 2023 22:58:34 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 25 Jul 2023 22:58:34 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 25 Jul 2023 22:58:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:29279ac7c19f9c667f1c6b07bfba6fba20ca0d945b9fbc6edad6f75d13361fae`  
		Last Modified: Tue, 04 Jul 2023 02:01:38 GMT  
		Size: 53.7 MB (53703979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b469d5dede8623ac47ab736de70ff10f49d99695196860ab6ebfae053f40054`  
		Last Modified: Tue, 25 Jul 2023 23:04:55 GMT  
		Size: 143.5 MB (143538098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7090c25c7d78d4dae6213988c3fd13f8de36c3e92fcbbd51f9545ab0d14705`  
		Last Modified: Tue, 25 Jul 2023 23:04:46 GMT  
		Size: 2.4 MB (2351404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb30e181aebbb06c564242e45b2231e0f13672c43bcab69f17b10c5026379eb`  
		Last Modified: Tue, 25 Jul 2023 23:04:49 GMT  
		Size: 58.8 MB (58821239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30f12f6dada6655557ea30da2db6963304996ecc6c693abe851b910e7010d1b`  
		Last Modified: Tue, 25 Jul 2023 23:04:46 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
