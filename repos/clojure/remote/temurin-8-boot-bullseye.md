## `clojure:temurin-8-boot-bullseye`

```console
$ docker pull clojure@sha256:dd6065667e3290fd4f4dc11ae4d0b7ff65fee01226eefd6acc8c3462e615dc10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e54c1f611ff7581f4978d8e6bd107df2e2712c2313e346e9efa5158069589e0e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.9 MB (170880727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7a8816e3bef8256602b6405c3f523bb3c5112ea4e6185781ca7c5b269fbd6e0`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:09 GMT
ADD file:b7c0be2bb90e88689b1c16da78dea0b85760b55b90ef2e5bc4a529c89e4fa25b in / 
# Tue, 04 Jul 2023 01:20:10 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:59:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 03:59:16 GMT
COPY dir:715eb4123a1bd94a1f232c902a6f3cdcc4011195a3e566c0f0ddc35dd1e83095 in /opt/java/openjdk 
# Tue, 04 Jul 2023 03:59:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 03:59:16 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 04 Jul 2023 03:59:16 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 04 Jul 2023 03:59:16 GMT
WORKDIR /tmp
# Tue, 04 Jul 2023 03:59:26 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 04 Jul 2023 03:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Jul 2023 03:59:26 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 04 Jul 2023 04:00:10 GMT
RUN boot
# Tue, 04 Jul 2023 04:00:10 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:34df401c391c7595044379e04e8ad4856a5a3974cdbf5a160f0a204d761e88aa`  
		Last Modified: Tue, 04 Jul 2023 01:25:21 GMT  
		Size: 55.1 MB (55055300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d61b0f812c98f508ec37433e62016886d535505339cfed6344cdf96af107c13`  
		Last Modified: Tue, 04 Jul 2023 04:11:45 GMT  
		Size: 54.6 MB (54642124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e7e5bdd5bc711fc9d90b5f4867e7d9f88dc36edb12c0cb68c848d5eeb34244`  
		Last Modified: Tue, 04 Jul 2023 04:11:39 GMT  
		Size: 2.4 MB (2362037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4266b9ce37f51b5381184b19c058de60cc84b80114974a8828f411c8a375b0f`  
		Last Modified: Tue, 04 Jul 2023 04:11:42 GMT  
		Size: 58.8 MB (58821266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:23b07e2d2a08eaa914fb9ccf28cd8dc48f4849943d99ae1e4b8461b7ffaebe00
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.6 MB (168618876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4264e9725120b561c0cdd1bfdc65b926a2a45ac09fae7c66e99609837c106074`
-	Default Command: `["boot","repl"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:22 GMT
ADD file:caddd2f40296ec5c1bf7487617ca8694cfff9a1d9b7484159e203b6514cb5f5f in / 
# Mon, 12 Jun 2023 23:40:23 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:50:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jun 2023 04:50:40 GMT
COPY dir:f6bbe63c81e220d954915791686219263d8c45918fd81b238f7c9f6b21f076f8 in /opt/java/openjdk 
# Tue, 13 Jun 2023 04:50:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jun 2023 04:50:41 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 13 Jun 2023 04:50:41 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 13 Jun 2023 04:50:41 GMT
WORKDIR /tmp
# Tue, 13 Jun 2023 04:50:46 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 13 Jun 2023 04:50:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jun 2023 04:50:46 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 13 Jun 2023 04:51:08 GMT
RUN boot
# Tue, 13 Jun 2023 04:51:08 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:663ccfaf62a5d7b997bca03d1dc6d5dfff01b9e0de08d86dbea8957ea92d7d16`  
		Last Modified: Mon, 12 Jun 2023 23:44:25 GMT  
		Size: 53.7 MB (53704136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcca61eb6313d4e5e7eaa5a1e052d334113c44736b5940de5eec6f3f49baaeed`  
		Last Modified: Tue, 13 Jun 2023 05:00:19 GMT  
		Size: 53.7 MB (53742661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f31771693c191dbf9d4b4aa365cdc1dfda92365d6d503225234d5cf1cf7ba4`  
		Last Modified: Tue, 13 Jun 2023 05:00:14 GMT  
		Size: 2.4 MB (2351317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:494ee230f412503b61f537a832cf45ba7962fb80995714fea5a9f9ace60d0d79`  
		Last Modified: Tue, 13 Jun 2023 05:00:17 GMT  
		Size: 58.8 MB (58820762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
