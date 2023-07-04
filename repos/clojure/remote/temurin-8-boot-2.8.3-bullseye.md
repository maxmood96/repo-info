## `clojure:temurin-8-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:2e87e1acefb6cfcc71c6070941b0c94ea17622f6aec1e6bbaec710f0b08a0395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-2.8.3-bullseye` - linux; amd64

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

### `clojure:temurin-8-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:781e4a3ededd0e707e1c959334e10be77d951e8f019d8d4b6aac6dafedef11e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.6 MB (168618676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d83d0f8418fe8f9f63e036a4f9060b33070e0c3a780b75af2ec2454392c5fa3`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:43 GMT
ADD file:e626446584d8094b7b58d72a717380ca64d3e9ab924fc625406fe26a83fe1d8b in / 
# Tue, 04 Jul 2023 01:57:43 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:43:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 06:43:39 GMT
COPY dir:f6bbe63c81e220d954915791686219263d8c45918fd81b238f7c9f6b21f076f8 in /opt/java/openjdk 
# Tue, 04 Jul 2023 06:43:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 06:43:41 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 04 Jul 2023 06:43:41 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 04 Jul 2023 06:43:41 GMT
WORKDIR /tmp
# Tue, 04 Jul 2023 06:43:46 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 04 Jul 2023 06:43:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Jul 2023 06:43:47 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 04 Jul 2023 06:44:08 GMT
RUN boot
# Tue, 04 Jul 2023 06:44:08 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:29279ac7c19f9c667f1c6b07bfba6fba20ca0d945b9fbc6edad6f75d13361fae`  
		Last Modified: Tue, 04 Jul 2023 02:01:38 GMT  
		Size: 53.7 MB (53703979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a952e7f7b69157dc62e9b0f020a4c17e46f7508fa5415a079eef7242d1af239c`  
		Last Modified: Tue, 04 Jul 2023 06:53:36 GMT  
		Size: 53.7 MB (53742700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e695322dfe4b16414bef56486531d3a286a348b604124654772e060291ffe8d3`  
		Last Modified: Tue, 04 Jul 2023 06:53:30 GMT  
		Size: 2.4 MB (2351391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72bc81802e4d363864efb3d454664b6a1b7ae857963a83a5bd4bdcb4b40d9120`  
		Last Modified: Tue, 04 Jul 2023 06:53:33 GMT  
		Size: 58.8 MB (58820606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
