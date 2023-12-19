## `clojure:temurin-8-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:b6b0a84a0cc624194c4e815613e38a79a68f2a6db17f36de6d2f0b3c136964a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:25df6fb296b6b65048f2aed3ee876a2a4a20fed9e5c5bf9f751d24a1bf17ac4b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.9 MB (194916040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3155d16b21988f22debe3e82041a05c8bedeb3ee9ca85bd14974758f1a47eeb7`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:50 GMT
ADD file:bb44d67b03db8efaeb0c4171474f441d14ff35f328f13add32b289fca062fa2f in / 
# Tue, 19 Dec 2023 01:20:50 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 06:54:34 GMT
COPY dir:a294625293e4e40913c98181a9aeff55bc5e737b728d424dfdc884f576bd8f8d in /opt/java/openjdk 
# Tue, 19 Dec 2023 06:54:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 06:54:35 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 19 Dec 2023 06:54:35 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 19 Dec 2023 06:54:35 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 06:54:41 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 19 Dec 2023 06:54:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 Dec 2023 06:54:41 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 19 Dec 2023 06:55:00 GMT
RUN boot
# Tue, 19 Dec 2023 06:55:00 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:b5a0d5c14ba9ece1eecd5137c468d9a123372b0af2ed2c8c4446137730c90e5b`  
		Last Modified: Tue, 19 Dec 2023 01:25:40 GMT  
		Size: 31.4 MB (31417873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a81e534e5dbde731b8b44557c08ef958dbcfc1c7d5b67de1bc642afc5613f6`  
		Last Modified: Tue, 19 Dec 2023 07:15:47 GMT  
		Size: 103.6 MB (103598260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29fc694b560a7bf380f7b59dfcdec36f28284ecae9ffafa2d5c36c52d6de162`  
		Last Modified: Tue, 19 Dec 2023 07:15:39 GMT  
		Size: 1.1 MB (1079512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f2ee1dd346f16bfb323c71b752ec29d2a3eda2b2ae3b2eaf7f224ff08d85866`  
		Last Modified: Tue, 19 Dec 2023 07:15:42 GMT  
		Size: 58.8 MB (58820395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:de03e0aa48f4ef5f074c5eb5c4f1f23fc733a7db824308575d427a6d9c9a3799
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.7 MB (192652803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5028fcc577261bc47d168d1641521f6bc8cccab85e23c30db1777bc5ab98c9fa`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:00:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 06:55:48 GMT
COPY dir:95966e8772805277b939f0a555f93ce7d7e01898449cdb0fb69c182fe80d4021 in /opt/java/openjdk 
# Tue, 19 Dec 2023 06:55:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 06:55:50 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 19 Dec 2023 06:55:50 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 19 Dec 2023 06:55:50 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 06:55:55 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 19 Dec 2023 06:55:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 Dec 2023 06:55:55 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 19 Dec 2023 06:56:12 GMT
RUN boot
# Tue, 19 Dec 2023 06:56:12 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8460c2429b384c138ca104a8d205038e1877169d7a2d55c0430c97fdacb19c12`  
		Last Modified: Tue, 19 Dec 2023 07:13:30 GMT  
		Size: 102.7 MB (102701538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5605ae6b7e71b74e3ff77b98011364d9ce7ba940c2c1f4ce8968b34911765fc1`  
		Last Modified: Tue, 19 Dec 2023 07:13:23 GMT  
		Size: 1.1 MB (1066838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5efa6c46d6810ba6f00c1a865ba87daa0a3fa5cdfd82e9d8525e0d457ae61c7b`  
		Last Modified: Tue, 19 Dec 2023 07:13:27 GMT  
		Size: 58.8 MB (58820375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
