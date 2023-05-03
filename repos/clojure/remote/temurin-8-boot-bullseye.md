## `clojure:temurin-8-boot-bullseye`

```console
$ docker pull clojure@sha256:7852c3b0eaf6a50648486e4bae99b0aa25004b5cc20c44607501584c30c3d500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:623d815f137414d74a1b2c62003cacac2a6a9b52203be2808641f3e20598bf6c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.9 MB (170877387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2c9c4744eb1ed51e8f91da10560d70745cd9add98846a3c6b31e7f710edbecb`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 12 Apr 2023 00:19:55 GMT
ADD file:f2d012660f882f319a5878a3f9ce285f488b8f90fad49ad238541cf72089e035 in / 
# Wed, 12 Apr 2023 00:19:56 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:10:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Apr 2023 19:57:54 GMT
COPY dir:715eb4123a1bd94a1f232c902a6f3cdcc4011195a3e566c0f0ddc35dd1e83095 in /opt/java/openjdk 
# Wed, 26 Apr 2023 19:57:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Apr 2023 19:57:54 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 26 Apr 2023 19:57:54 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 26 Apr 2023 19:57:54 GMT
WORKDIR /tmp
# Wed, 26 Apr 2023 19:58:00 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 26 Apr 2023 19:58:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Apr 2023 19:58:00 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 26 Apr 2023 19:58:47 GMT
RUN boot
# Wed, 26 Apr 2023 19:58:47 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:b0248cf3e63c73d0e496a67807d056ca41d5e968b61087e8eca2cf4b9b4d7b99`  
		Last Modified: Wed, 12 Apr 2023 00:23:20 GMT  
		Size: 55.1 MB (55052736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7012d2eddb96550ad314f8dd31810e3b6623fb5b245468e7416bb6ee11361e4`  
		Last Modified: Wed, 26 Apr 2023 20:17:20 GMT  
		Size: 54.6 MB (54642102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b690979216e16bc1808d9a7d19996f60724a92db1da1581de391561090c0dc6`  
		Last Modified: Wed, 26 Apr 2023 20:17:14 GMT  
		Size: 2.4 MB (2361677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88987d9597cbbe78b300d4d90c429f6bdf3113394c48b8e66d6af91d729d989`  
		Last Modified: Wed, 26 Apr 2023 20:17:17 GMT  
		Size: 58.8 MB (58820872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bullseye` - linux; arm64 variant v8

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
