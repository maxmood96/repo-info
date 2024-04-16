## `clojure:temurin-17-boot-bullseye`

```console
$ docker pull clojure@sha256:132644083a411873b2b1aa44a67f51c84669afb71d2421ac744704082132848e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:44cc1342a0b262e4d010531e2daccc5b21b7045dadf54b0d23a45a8c7adc75d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.2 MB (261171341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adc506d100fc5170f2be05f127e927cc4944f5ba38417b84c498f06bc429ec16`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:59 GMT
ADD file:8efdcc3201e79c8a09fc9c1ade08492ea33f838047332a7c61988f6357339dee in / 
# Wed, 10 Apr 2024 01:50:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:18:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 06:29:32 GMT
COPY dir:88c5118aff6896f6ed535dcde576d68ef88ded459cca013e0f9beb3e430ebb52 in /opt/java/openjdk 
# Wed, 10 Apr 2024 06:29:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:29:33 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 10 Apr 2024 06:29:33 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 10 Apr 2024 06:29:33 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 06:29:39 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 10 Apr 2024 06:29:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 10 Apr 2024 06:29:39 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 10 Apr 2024 06:29:57 GMT
RUN boot
# Wed, 10 Apr 2024 06:29:57 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 10 Apr 2024 06:29:57 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 10 Apr 2024 06:29:57 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ac323bdaa10f869bd9e7adecd8f5326e44acc4c59168868108b1cdf3891089cc`  
		Last Modified: Wed, 10 Apr 2024 01:55:52 GMT  
		Size: 55.1 MB (55090264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393cd74c5a04db4b44b2a067d9b1189890379df98935ac76bc29ae115eb06bca`  
		Last Modified: Wed, 10 Apr 2024 06:46:20 GMT  
		Size: 144.9 MB (144893081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c36e40a47991e5a45ca94b833e223ccc23f5a2a25c972f1032a8366631b7abf`  
		Last Modified: Wed, 10 Apr 2024 06:46:08 GMT  
		Size: 2.4 MB (2367278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724e9b5cf9c25f56a2bcf43f10e32cf04b227cd38f2d41611e15842287646330`  
		Last Modified: Wed, 10 Apr 2024 06:46:11 GMT  
		Size: 58.8 MB (58820319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44d2b94eac2e5c202ce2264d3287e465766a68934901936454e0adf2898e450`  
		Last Modified: Wed, 10 Apr 2024 06:46:08 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d213be22969d7e70338ce07e712caa3fd9a9931eb21fe68f88e67c5a4185b0e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258626835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07cd7b97ebddb6fd1ee4dadab5f5602902737e1e7cfca3c968872f2586d5b5c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:30 GMT
ADD file:6fedb173fe261ff0e13b004ca692b7edcc74dcc3c4384fee092b96ef9508992c in / 
# Wed, 10 Apr 2024 00:40:30 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:39:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Apr 2024 06:41:00 GMT
COPY dir:00f694ce512d2e49bdb0844fa7f6d54a4b39a35418d1c6b32b574b5d44cfc1da in /opt/java/openjdk 
# Tue, 16 Apr 2024 06:41:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 06:41:03 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 16 Apr 2024 06:41:03 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 16 Apr 2024 06:41:03 GMT
WORKDIR /tmp
# Tue, 16 Apr 2024 06:41:08 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 16 Apr 2024 06:41:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Apr 2024 06:41:08 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 16 Apr 2024 06:41:25 GMT
RUN boot
# Tue, 16 Apr 2024 06:41:25 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 16 Apr 2024 06:41:25 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Apr 2024 06:41:25 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:197947a07d5f6c6ff020ca65dcea4e52671f85f67bee1b59af46cb0dc36580d9`  
		Last Modified: Wed, 10 Apr 2024 00:44:24 GMT  
		Size: 53.7 MB (53729176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d38c21b09d53fed41b7bd3ec1a4b9e920db379f3c64904afb6272b7efd4be7ad`  
		Last Modified: Tue, 16 Apr 2024 06:57:09 GMT  
		Size: 143.7 MB (143720948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55b41418faecec6a291850752037d35cbda6872d7b59c4b608d2f78bd7f309a`  
		Last Modified: Tue, 16 Apr 2024 06:57:00 GMT  
		Size: 2.4 MB (2355803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb407eb11be28e79ad362e530d569f7e79118049c11ae2e38825a99c588ac32`  
		Last Modified: Tue, 16 Apr 2024 06:57:03 GMT  
		Size: 58.8 MB (58820509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94697b86ad7e57083a16dd6a3b6864d59ebb51ad4d3009200931c1d435617c5`  
		Last Modified: Tue, 16 Apr 2024 06:57:00 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
