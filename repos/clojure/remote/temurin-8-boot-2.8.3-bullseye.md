## `clojure:temurin-8-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:fabbd6777222953667fffd9def8ef86d8633be3dda69cf69505e5fa307cca686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:bb837fe68a51973ca026584a09ed203f1f8befa80eddff78f8442ddef3871848
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.9 MB (170873637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85eb2183b80411b5d7eb779ddab14059a0a0c426d3b85fa3b9adfd60f2ed43e6`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 02 May 2023 23:46:50 GMT
ADD file:fc290cf8ddb984325474583faa79c5a98c5ea0ec7f606bf360251f63acecf389 in / 
# Tue, 02 May 2023 23:46:51 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:24:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 03 May 2023 20:24:11 GMT
COPY dir:715eb4123a1bd94a1f232c902a6f3cdcc4011195a3e566c0f0ddc35dd1e83095 in /opt/java/openjdk 
# Wed, 03 May 2023 20:24:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 20:24:11 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 03 May 2023 20:24:11 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 03 May 2023 20:24:11 GMT
WORKDIR /tmp
# Wed, 03 May 2023 20:24:17 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 03 May 2023 20:24:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 03 May 2023 20:24:17 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 03 May 2023 20:24:39 GMT
RUN boot
# Wed, 03 May 2023 20:24:39 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:918547b9432687b1e1d238e82dc1e0ea0b736aafbf3c402eea98c6db81a9cb65`  
		Last Modified: Tue, 02 May 2023 23:49:58 GMT  
		Size: 55.0 MB (55049070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df5e2c1247e792b32dfc253554b769e50b9d0e00b87bda347fdad278b672e1b2`  
		Last Modified: Wed, 03 May 2023 20:35:03 GMT  
		Size: 54.6 MB (54642112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ab8563a7ff31d93d93455ba91350716d4445e104a74c3f5fc95d0eb7aa215e`  
		Last Modified: Wed, 03 May 2023 20:34:57 GMT  
		Size: 2.4 MB (2361754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c4ddd1d7de4f32089310a1123d6b78fe0eb67138f159baed76a66d6f7621a4`  
		Last Modified: Wed, 03 May 2023 20:35:00 GMT  
		Size: 58.8 MB (58820701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:98cde0c53ce3660b89153ea2d941459765ec790af946105ab81ab02ef0da369e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.6 MB (168607419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a01573f97ff87068e98cc3f1ce9016f2e28163650bcd698babddc8b99ea90343`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 03 May 2023 00:22:41 GMT
ADD file:f930fdb659332a615b0042ca415d6d7feda9ba6b2f58222e3e5bbed326db4d40 in / 
# Wed, 03 May 2023 00:22:42 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:43:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 03 May 2023 17:43:30 GMT
COPY dir:f6bbe63c81e220d954915791686219263d8c45918fd81b238f7c9f6b21f076f8 in /opt/java/openjdk 
# Wed, 03 May 2023 17:43:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 17:43:32 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 03 May 2023 17:43:32 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 03 May 2023 17:43:32 GMT
WORKDIR /tmp
# Wed, 03 May 2023 17:43:37 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 03 May 2023 17:43:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 03 May 2023 17:43:37 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 03 May 2023 17:44:14 GMT
RUN boot
# Wed, 03 May 2023 17:44:15 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:d677c78be691f8dcbe9d44ce576b97ad205b3dd78557dc62794e59eb19553ee9`  
		Last Modified: Wed, 03 May 2023 00:25:31 GMT  
		Size: 53.7 MB (53692705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17195ab6dd6b55d9432639a70d6906e4d7fe48e30d722b8d64ebe522206b3b30`  
		Last Modified: Wed, 03 May 2023 17:53:20 GMT  
		Size: 53.7 MB (53742673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f21359f2521287e483c284576e8f920ad0e25e907585d73d11743dd94db15f3`  
		Last Modified: Wed, 03 May 2023 17:53:16 GMT  
		Size: 2.4 MB (2351068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134f125a9ff4dcf6525cc0a4813c5288f67f1cceeb7e78605b8b4c756b862905`  
		Last Modified: Wed, 03 May 2023 17:53:18 GMT  
		Size: 58.8 MB (58820973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
