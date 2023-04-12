## `clojure:temurin-8-boot-bullseye`

```console
$ docker pull clojure@sha256:56f154a840f1f96152f42ae151e20e1e7731985e82effa6421c7ac4a1370ac49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:7867bf8807ac92b7d761888cbbed4dc5f335821b372ba21411c079bd78b1910d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.9 MB (170863475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb424d3cca19da319b2de290a57c37efaca375a6865c06e8894997b01425559f`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:15 GMT
ADD file:459d1e92eb8c24ff4758f974d289ca8a2abe04cf50b6fe2bd760aa4589478289 in / 
# Thu, 23 Mar 2023 01:30:15 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:16:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 Mar 2023 06:17:00 GMT
COPY dir:bbb84183d7ea38d81d8401f01e29d08935ee4c8bf6f90c6527579a1554c3bde1 in /opt/java/openjdk 
# Thu, 23 Mar 2023 06:17:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Mar 2023 06:17:01 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 23 Mar 2023 06:17:01 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 23 Mar 2023 06:17:01 GMT
WORKDIR /tmp
# Thu, 23 Mar 2023 06:17:06 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 23 Mar 2023 06:17:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 23 Mar 2023 06:17:07 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 23 Mar 2023 06:17:37 GMT
RUN boot
# Thu, 23 Mar 2023 06:17:38 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:3e440a7045683e27f8e2fa04000e0e078d8dfac0c971358ae0f8c65c13321c8e`  
		Last Modified: Thu, 23 Mar 2023 01:34:00 GMT  
		Size: 55.0 MB (55045608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a5629480cb1323c2f01db8609391416fe9380f0b3fc3c8da30bdfaf6c963d0c`  
		Last Modified: Thu, 23 Mar 2023 06:29:13 GMT  
		Size: 54.6 MB (54635545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1407e444e98c37386fdf3fca3f50a789ba69be7685c5e11cecfb9753ecde1420`  
		Last Modified: Thu, 23 Mar 2023 06:29:07 GMT  
		Size: 2.4 MB (2361567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5efe9fc4970a55d8d9c9fd53ea16e20248284e131811779b5b69d6fa669f7ffe`  
		Last Modified: Thu, 23 Mar 2023 06:29:10 GMT  
		Size: 58.8 MB (58820755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4cf274344e9842496936770cf37810b67d7aaa31037caafa966ac2bd5d838054
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.6 MB (168605509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f5e4395e67be1dbc17339a2b440757307205f6b3d3925dc7b55fa515e19d423`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:42 GMT
ADD file:dd3d4e5fe819950e7d01b44a29dbd790438cd722ba76198910e2597448ab0c6f in / 
# Wed, 12 Apr 2023 00:39:43 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:18:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Apr 2023 01:18:07 GMT
COPY dir:b6d7e5613532d986930216de9e0fece0632e82564ce7a6a98baf63b4115f840d in /opt/java/openjdk 
# Wed, 12 Apr 2023 01:18:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 01:18:08 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 12 Apr 2023 01:18:08 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 12 Apr 2023 01:18:08 GMT
WORKDIR /tmp
# Wed, 12 Apr 2023 01:18:13 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 12 Apr 2023 01:18:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 12 Apr 2023 01:18:13 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 12 Apr 2023 01:18:43 GMT
RUN boot
# Wed, 12 Apr 2023 01:18:43 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:dc80b8cdbfd36cb20231d807a50d704945d1df4da8f6e23197ccfcb629970491`  
		Last Modified: Wed, 12 Apr 2023 00:42:14 GMT  
		Size: 53.7 MB (53705529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77229bf38387a79e392fbb99c62cf0fd3217ddff780898642fd3b9455fcd5530`  
		Last Modified: Wed, 12 Apr 2023 01:27:57 GMT  
		Size: 53.7 MB (53727903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69ada62ed0cd7f04cf989aa4a7a005b75c66716657268bdfb678a68634e541a`  
		Last Modified: Wed, 12 Apr 2023 01:27:53 GMT  
		Size: 2.4 MB (2351057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00397887f82b213a7948790ce163a7571b77c2e5c4e6ba88cb66c904025e0c52`  
		Last Modified: Wed, 12 Apr 2023 01:27:55 GMT  
		Size: 58.8 MB (58821020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
