## `clojure:temurin-11-boot-2.8.3-bookworm`

```console
$ docker pull clojure@sha256:a6ee5d093ba3542534006cada7ba2086c848c7e0728a4ca133cd96cb635a1485
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:cb054f091083246d54d2c83c02a0ad3581a61182234927c1d433179af64dbeb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259175509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52d0713f0fb041a45cc2fc4cc57fbcd96c71ce7604d8e15f376a87c9980149a`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:42 GMT
ADD file:077a3156bd8271f26498ae6ac3800e68a42b9277581bc81eea31fec1a123dca5 in / 
# Thu, 11 Jan 2024 02:37:43 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:50:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 14:12:03 GMT
COPY dir:c80966d54ee599fa5b16f964e9342a0dab00f0ed4f5d18b7bebc8a71278b8b40 in /opt/java/openjdk 
# Wed, 17 Jan 2024 14:12:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 14:12:05 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 17 Jan 2024 14:12:05 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 17 Jan 2024 14:12:05 GMT
WORKDIR /tmp
# Wed, 17 Jan 2024 14:12:13 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 17 Jan 2024 14:12:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 17 Jan 2024 14:12:13 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 17 Jan 2024 14:12:34 GMT
RUN boot
# Wed, 17 Jan 2024 14:12:34 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:1b13d4e1a46e5e969702ec92b7c787c1b6891bff7c21ad378ff6dbc9e751d5d4`  
		Last Modified: Thu, 11 Jan 2024 02:42:04 GMT  
		Size: 49.6 MB (49561490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0533613fd9e72d97991f095a9afedf5cf8b7bee5c5241378a4e9a12b467ad72`  
		Last Modified: Wed, 17 Jan 2024 14:48:40 GMT  
		Size: 145.3 MB (145266475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b06cefb1bac1965ddffa066f57f3293dfab7244fbb5424377cd912097650c5c2`  
		Last Modified: Wed, 17 Jan 2024 14:48:29 GMT  
		Size: 5.5 MB (5527058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76af990e2efd40a70eba8faa33fd2112d7e3e982eea2fd3e611418631019a56`  
		Last Modified: Wed, 17 Jan 2024 14:48:31 GMT  
		Size: 58.8 MB (58820486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3d0d200ea1bcecd5a2bd90b7d4ea618661cc0fbe461cab5121559521b026e44b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255764170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709c954ff8e512cff56fdb57fb59d28449c6506e99b8a609d9ac0970c67fa6ee`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:33 GMT
ADD file:051a18650d326af1d23e30c93370e647e62f94887ce43b22e1808052bce4f2a6 in / 
# Thu, 11 Jan 2024 02:40:34 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 07:57:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:22:18 GMT
COPY dir:de5568efb2f4de409b0bbafecabebfd7b12106c4b1a8ded40ebb723247056709 in /opt/java/openjdk 
# Wed, 17 Jan 2024 09:22:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:22:21 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 17 Jan 2024 09:22:21 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 17 Jan 2024 09:22:21 GMT
WORKDIR /tmp
# Wed, 17 Jan 2024 09:22:28 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 17 Jan 2024 09:22:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 17 Jan 2024 09:22:28 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 17 Jan 2024 09:22:45 GMT
RUN boot
# Wed, 17 Jan 2024 09:22:46 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:5665c1f9a9e17acd68ae05b2839df402eac34afdd095f8c115f09886d757840c`  
		Last Modified: Thu, 11 Jan 2024 02:43:41 GMT  
		Size: 49.6 MB (49592247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b4f3d43c834c7c7e4af9762d75271ce81d581decd71927aad4c61e7964a2f82`  
		Last Modified: Wed, 17 Jan 2024 09:37:46 GMT  
		Size: 142.0 MB (142002057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff2956786ec68aa9c4dcdd2e5db3d3f4ec2a239175da058080d8c5e41eb5e48`  
		Last Modified: Wed, 17 Jan 2024 09:36:52 GMT  
		Size: 5.3 MB (5349303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9406490afde4d3375adbfe61d8e8dba660b392e6a48a07815008a589438200b2`  
		Last Modified: Wed, 17 Jan 2024 09:36:54 GMT  
		Size: 58.8 MB (58820563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
