## `clojure:temurin-8-boot-bookworm`

```console
$ docker pull clojure@sha256:6eab10d54dbf5c0d258a6af37657b29a4fa3c61b5e055be4cde030b8695c1a38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:ca6b000784746a3c0d0b98ccbb5bbb87cb25c608136bdaeb07314c61a85c27ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 MB (217491832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea683d28d62b20887cc2bacac7140b7962c9d01d21fe64763f19112f852fe4a`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 12 Mar 2024 01:20:46 GMT
ADD file:b18b4c32dd8042f45097997c732dc29b3917fd7d5f337f9e772eee5875fbe6f1 in / 
# Tue, 12 Mar 2024 01:20:46 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:10:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 Mar 2024 06:11:12 GMT
COPY dir:7a6a87e7bb8d56b27d71b1f614847d2afb4282190a48214e2e48b164fbef7bc7 in /opt/java/openjdk 
# Tue, 12 Mar 2024 06:11:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 06:11:13 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 12 Mar 2024 06:11:13 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 12 Mar 2024 06:11:13 GMT
WORKDIR /tmp
# Tue, 12 Mar 2024 06:11:19 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 12 Mar 2024 06:11:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 12 Mar 2024 06:11:20 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 12 Mar 2024 06:11:41 GMT
RUN boot
# Tue, 12 Mar 2024 06:11:42 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:71215d55680cf0ab2dcc0e1dd65ed76414e3fb0c294249b5b9319a8fa7c398e4`  
		Last Modified: Tue, 12 Mar 2024 01:25:15 GMT  
		Size: 49.6 MB (49552196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f31bb2ac672ca1059b0a6512d1f8cff2a7c1903786626e25efe760c3e928e3`  
		Last Modified: Tue, 12 Mar 2024 06:34:20 GMT  
		Size: 103.6 MB (103591905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f51fe6c1e668f011dc11198e1ceba56b316bcfd3a4418768995ee2d1630f6e35`  
		Last Modified: Tue, 12 Mar 2024 06:34:12 GMT  
		Size: 5.5 MB (5527084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec152c1665dc00614a8f0f660d815f4553137a610c097dd70a7e7dd2f830ec36`  
		Last Modified: Tue, 12 Mar 2024 06:34:14 GMT  
		Size: 58.8 MB (58820647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:559c2dc2c52f3d0b77428cd11ab7f07f9f632c8d36ffde538b9021949755031b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216464737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85350a330ed5cb3675fdb7c2845bdede55afbb27a366e1ec550c59069af9c00b`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:26 GMT
ADD file:9b51ed214f9332acf3126d841440c24eed0beac4062487fb360b288f628454dc in / 
# Tue, 12 Mar 2024 00:45:27 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:42:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 Mar 2024 01:42:58 GMT
COPY dir:d67e1a8d4006c4d31bb089f955cdf6054ae46936c41fb4bbc9c830e6a49d11d6 in /opt/java/openjdk 
# Tue, 12 Mar 2024 01:42:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 01:42:59 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 12 Mar 2024 01:43:00 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 12 Mar 2024 01:43:00 GMT
WORKDIR /tmp
# Tue, 12 Mar 2024 01:43:05 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 12 Mar 2024 01:43:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 12 Mar 2024 01:43:05 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 12 Mar 2024 01:43:58 GMT
RUN boot
# Tue, 12 Mar 2024 01:43:58 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:6ee0baa58a3d368515336c1b5c1cade29c975e1b49a832f19e22f4c46f4a23a7`  
		Last Modified: Tue, 12 Mar 2024 00:48:33 GMT  
		Size: 49.6 MB (49590984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1f067e69dadc5cc2c2ed5898b9d04f2ab2b78246ccfd096e8de3302a96c807`  
		Last Modified: Tue, 12 Mar 2024 02:02:41 GMT  
		Size: 102.7 MB (102703043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1264b2e4138fe82751939c065c595614d2e516a29eca22f88473bd2a2f461fbf`  
		Last Modified: Tue, 12 Mar 2024 02:02:35 GMT  
		Size: 5.3 MB (5349396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:974a076573ef01bd12d41fc3ac6944f4819085fcf043386f8b5753d86228fd8e`  
		Last Modified: Tue, 12 Mar 2024 02:02:36 GMT  
		Size: 58.8 MB (58821314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
