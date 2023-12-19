## `clojure:temurin-8-boot-2.8.3-bookworm`

```console
$ docker pull clojure@sha256:c17811c5605d20de227800c999e3bba4dc84a1a89bf68829ca0f6ff34399edf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-2.8.3-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:488733bfee28e751286fb02d7c0188f0f66eedaed90e3d2ef54bce6bd0ff45ad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 MB (217508295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9d5207fbd60c938e10296bb2291091b2cc53824aa342a86ea70412899737bb2`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:15 GMT
ADD file:7d8adf68670e8dc2af6b8603870ea610fc65ecbb08799f2ca6a3134f5d47d289 in / 
# Tue, 19 Dec 2023 01:20:16 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:51:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 06:52:02 GMT
COPY dir:a294625293e4e40913c98181a9aeff55bc5e737b728d424dfdc884f576bd8f8d in /opt/java/openjdk 
# Tue, 19 Dec 2023 06:52:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 06:52:03 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 19 Dec 2023 06:52:03 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 19 Dec 2023 06:52:04 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 06:52:10 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 19 Dec 2023 06:52:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 Dec 2023 06:52:10 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 19 Dec 2023 06:53:08 GMT
RUN boot
# Tue, 19 Dec 2023 06:53:08 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:bc0734b949dcdcabe5bfdf0c8b9f44491e0fce04cb10c9c6e76282b9f6abdf01`  
		Last Modified: Tue, 19 Dec 2023 01:24:35 GMT  
		Size: 49.6 MB (49561579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ece076bc6b8caf0e5211820bb849ba687839e45c5a423e30909adb899009fb9`  
		Last Modified: Tue, 19 Dec 2023 07:14:54 GMT  
		Size: 103.6 MB (103598261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3baabcc5ee904ad72ab29f94503517042c1343f14c5dcfe909e836213f85d52`  
		Last Modified: Tue, 19 Dec 2023 07:14:47 GMT  
		Size: 5.5 MB (5527136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc56d234efeefd3995a463de3414163bbbf43cfcca9dbbacb25f95b6c4b4def2`  
		Last Modified: Tue, 19 Dec 2023 07:14:49 GMT  
		Size: 58.8 MB (58821319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-2.8.3-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:745ce9f058ea66390c32fd7a2cea050f24e6093d903fa4a11cd33301897c19a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216463593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c0084b7c5c2a0686c6ef5b6fc1e0c1903fe941c8aae5e8a51d6f9160baa3d6`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:02 GMT
ADD file:412f80f75ed3e520f767e70b6b27fc81807f62fc5c6e5adf756507e33af9fa6b in / 
# Tue, 19 Dec 2023 01:41:02 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:53:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 06:54:25 GMT
COPY dir:95966e8772805277b939f0a555f93ce7d7e01898449cdb0fb69c182fe80d4021 in /opt/java/openjdk 
# Tue, 19 Dec 2023 06:54:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 06:54:27 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 19 Dec 2023 06:54:27 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 19 Dec 2023 06:54:27 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 06:54:32 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 19 Dec 2023 06:54:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 Dec 2023 06:54:32 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 19 Dec 2023 06:54:49 GMT
RUN boot
# Tue, 19 Dec 2023 06:54:49 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:b66b4ecd3ecfb67b3b7a2a44b0199cbdfc94965c8bd3fefab75cd2e612799740`  
		Last Modified: Tue, 19 Dec 2023 01:44:14 GMT  
		Size: 49.6 MB (49592259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebd83395931034d8cc43b9c1210837008aa4d9f602c045c8c2f80b89be5b9e2`  
		Last Modified: Tue, 19 Dec 2023 07:12:44 GMT  
		Size: 102.7 MB (102701533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486bc581fec8cf9127552a0c670f1ade77753be94ce3bd64fb33bc5008643c81`  
		Last Modified: Tue, 19 Dec 2023 07:12:38 GMT  
		Size: 5.3 MB (5349257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d269201e4fa5e82b9626b17ee530a54a968b9b4fd18f5f57cbc2aeb948898464`  
		Last Modified: Tue, 19 Dec 2023 07:12:41 GMT  
		Size: 58.8 MB (58820544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
