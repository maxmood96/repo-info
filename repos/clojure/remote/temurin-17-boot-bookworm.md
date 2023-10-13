## `clojure:temurin-17-boot-bookworm`

```console
$ docker pull clojure@sha256:b128cbcb38f60a35b90711d41086d139f1a4c1869c9d53e504e7b440b37bddc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:c4f5250830f74b89462ac74e1d805d986372a02b0fd09d8f53fb07a061ed3eea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.7 MB (258711297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7252051ac456b9a3f10098f251c9a90b8fd04a5e671223dd2ee74320bc0c93`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:37 GMT
ADD file:1e4dd5dab602337b5d5ef8d84b8dbe8b1ac62225f077b29b27d045842486d8e2 in / 
# Wed, 11 Oct 2023 18:34:37 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 01:26:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 01:34:01 GMT
COPY dir:762e280751e9eaacf2bfae42d6a8cb2a49846426bd7c5675b21a4c0c8ae8fb71 in /opt/java/openjdk 
# Fri, 13 Oct 2023 01:34:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:34:02 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 13 Oct 2023 01:34:02 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 01:34:02 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:34:08 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 13 Oct 2023 01:34:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 01:34:08 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 13 Oct 2023 01:34:26 GMT
RUN boot
# Fri, 13 Oct 2023 01:34:26 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 01:34:27 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 01:34:27 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0a9573503463fd3166b5b1f34a7720dac28609e98d731e50e7068f92e79b8545`  
		Last Modified: Wed, 11 Oct 2023 18:39:10 GMT  
		Size: 49.6 MB (49582224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9297dc0c7fb70cdbd48c6c16e128659b9836a465fe2755e7b24f636c965ca5b1`  
		Last Modified: Fri, 13 Oct 2023 01:48:16 GMT  
		Size: 144.8 MB (144775739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d72726ed0dd2f667acc72901d01be1660048ac4f7863409ed04a64e5d121ebb`  
		Last Modified: Fri, 13 Oct 2023 01:48:05 GMT  
		Size: 5.5 MB (5532602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19bdd9516c5c3e0a12380c9e7325cf0857d175091e63d695ce57d1e7d00ba906`  
		Last Modified: Fri, 13 Oct 2023 01:48:08 GMT  
		Size: 58.8 MB (58820333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220651609596690b1c30d057286e93b26473f40b19005927915aca9cee86a5cb`  
		Last Modified: Fri, 13 Oct 2023 01:48:04 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6b70c111964d0686e9291af062842f1d76a739443de114be6a63393ecbd88783
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.3 MB (257332580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58f7bc8850cb1bc3766ceb5fb7ff1c8e6063797a5dc8eaa54b8b88f58e3b79d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:43 GMT
ADD file:bf4264671bd91eb30c67d512144ebcf7f5c55a3e490ebe7876fa9b20d433bf7b in / 
# Wed, 11 Oct 2023 18:24:44 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 00:57:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 10:18:40 GMT
COPY dir:3557de79388a35bdf2852c0a661b5338e655c1b5c590eb501d2be4fa10ef826e in /opt/java/openjdk 
# Fri, 13 Oct 2023 10:18:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 10:18:44 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 13 Oct 2023 10:18:44 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 10:18:44 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 10:18:49 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 13 Oct 2023 10:18:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 10:18:49 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 13 Oct 2023 10:19:07 GMT
RUN boot
# Fri, 13 Oct 2023 10:19:07 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 10:19:07 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 10:19:07 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e720f94321d63ecb6efa873b294dce7eaa1c3a5ddcd5bf7daddf375b955669a4`  
		Last Modified: Wed, 11 Oct 2023 18:28:04 GMT  
		Size: 49.6 MB (49612578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82d651a3fb90463baef37e8108569d81355c0974d68da3cce0e70482f66c93d`  
		Last Modified: Fri, 13 Oct 2023 10:34:04 GMT  
		Size: 143.5 MB (143543493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54561214b0a54647aa2a297566bba99b4156f5629829970d4c94bee9f95b05a7`  
		Last Modified: Fri, 13 Oct 2023 10:33:55 GMT  
		Size: 5.4 MB (5355512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f88c8fe7289ab64d648a3bc6c90653d564519d97d6b4e8d698c10adcbb80dd`  
		Last Modified: Fri, 13 Oct 2023 10:33:58 GMT  
		Size: 58.8 MB (58820598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c49242bd272a1a231d4cabd25d73b301578704f65982eb43ffeb165b17aecff7`  
		Last Modified: Fri, 13 Oct 2023 10:33:54 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
