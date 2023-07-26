## `clojure:temurin-17-boot-bullseye`

```console
$ docker pull clojure@sha256:5fb6f14b7e6bb5b585df03197080aeabf40e0ddb30d898a6652b2bf76de67e26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:13f5627e7f09064ddfa235a73fc0eb9321cdfda8eb0c9f76319e4d991960b280
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.8 MB (308818542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c829c88425639ce1be22a83bb65dadcbea6cbb9c8cc1357b238e69eacbff14`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:09 GMT
ADD file:b7c0be2bb90e88689b1c16da78dea0b85760b55b90ef2e5bc4a529c89e4fa25b in / 
# Tue, 04 Jul 2023 01:20:10 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:59:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Jul 2023 11:23:59 GMT
COPY dir:4f02f3c240ecc691ff41263b0454f619d51a2ba11a57fe51c0e31e7ff62a9194 in /opt/java/openjdk 
# Wed, 05 Jul 2023 11:24:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 11:24:00 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 05 Jul 2023 11:24:00 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 05 Jul 2023 11:24:00 GMT
WORKDIR /tmp
# Wed, 05 Jul 2023 11:24:06 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 05 Jul 2023 11:24:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 05 Jul 2023 11:24:06 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 05 Jul 2023 11:24:23 GMT
RUN boot
# Wed, 05 Jul 2023 11:24:23 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 05 Jul 2023 11:24:23 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 05 Jul 2023 11:24:23 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:34df401c391c7595044379e04e8ad4856a5a3974cdbf5a160f0a204d761e88aa`  
		Last Modified: Tue, 04 Jul 2023 01:25:21 GMT  
		Size: 55.1 MB (55055300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a077e746244337006bc6abb6a75eb4ea69a610ed50b6256900329e7736acfc`  
		Last Modified: Wed, 05 Jul 2023 11:35:40 GMT  
		Size: 192.6 MB (192580432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449371bb5f5fe6e3bc135abaceafebd7d7b8b206f30070c7c792c489e56444a9`  
		Last Modified: Wed, 05 Jul 2023 11:35:27 GMT  
		Size: 2.4 MB (2362029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc54c41e9f5d4a8f5460f721afdfbd9725c775ea4f903dfa9d7da7cba3452be`  
		Last Modified: Wed, 05 Jul 2023 11:35:30 GMT  
		Size: 58.8 MB (58820383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2621c8d1608802bfc5301b4c3c93b3acf1626149262d0f3d3352b040f3d41e44`  
		Last Modified: Wed, 05 Jul 2023 11:35:27 GMT  
		Size: 398.0 B  
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
