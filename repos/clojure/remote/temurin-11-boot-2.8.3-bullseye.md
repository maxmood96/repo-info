## `clojure:temurin-11-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:45f6bcc1de5f3490fd901f40f2f25d14b6defe0029771906246b56d265ca0992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e41dd35bd58e1d471b6a95cbbf1db97ccbd9f20d16843702ee515373d18b7d0c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261067483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aace3894b5a99004f4717fb924b81caf4a13900f81c1b589398bc97c743586b8`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:09 GMT
ADD file:b7c0be2bb90e88689b1c16da78dea0b85760b55b90ef2e5bc4a529c89e4fa25b in / 
# Tue, 04 Jul 2023 01:20:10 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:59:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Jul 2023 02:40:54 GMT
COPY dir:2fc258758bb2c25982e4c8348cffe5a1ab54f4c54e52ff852a817cdf5bd62215 in /opt/java/openjdk 
# Wed, 26 Jul 2023 02:40:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 02:40:56 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 26 Jul 2023 02:40:56 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 26 Jul 2023 02:40:56 GMT
WORKDIR /tmp
# Wed, 26 Jul 2023 02:41:02 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 26 Jul 2023 02:41:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Jul 2023 02:41:02 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 26 Jul 2023 02:41:26 GMT
RUN boot
# Wed, 26 Jul 2023 02:41:26 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:34df401c391c7595044379e04e8ad4856a5a3974cdbf5a160f0a204d761e88aa`  
		Last Modified: Tue, 04 Jul 2023 01:25:21 GMT  
		Size: 55.1 MB (55055300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973fced5ae624f57d1b1d94457bbc1b8a2cbd2e473cd90b80736c518cf648d50`  
		Last Modified: Wed, 26 Jul 2023 02:49:01 GMT  
		Size: 144.8 MB (144829489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9263d5fbdaf9d312e9fa0dcbfacb91ac976b71c3fff48e6689592258319eaedf`  
		Last Modified: Wed, 26 Jul 2023 02:48:50 GMT  
		Size: 2.4 MB (2362150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef06cb70afe5704dc0c05fcefb72eb339f1f3117fe96abc168a880dc50cc675`  
		Last Modified: Wed, 26 Jul 2023 02:48:53 GMT  
		Size: 58.8 MB (58820544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2249e9fb7909d950c7577c7f4f8adcbe7b7a41a90342bd8bf6b13efb92f59977
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256441215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:201e691361556a9a6b136d714fe1bd23bb68b13a8228b0ac58fe91ab2c898bf0`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:43 GMT
ADD file:e626446584d8094b7b58d72a717380ca64d3e9ab924fc625406fe26a83fe1d8b in / 
# Tue, 04 Jul 2023 01:57:43 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:43:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Jul 2023 01:07:04 GMT
COPY dir:e71da8247d58ed4b0dfbf219951c863c79ac94b7f45cb60320ea827dfa699275 in /opt/java/openjdk 
# Wed, 26 Jul 2023 01:07:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jul 2023 01:07:07 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 26 Jul 2023 01:07:08 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 26 Jul 2023 01:07:08 GMT
WORKDIR /tmp
# Wed, 26 Jul 2023 01:07:13 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 26 Jul 2023 01:07:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Jul 2023 01:07:13 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 26 Jul 2023 01:07:32 GMT
RUN boot
# Wed, 26 Jul 2023 01:07:33 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:29279ac7c19f9c667f1c6b07bfba6fba20ca0d945b9fbc6edad6f75d13361fae`  
		Last Modified: Tue, 04 Jul 2023 02:01:38 GMT  
		Size: 53.7 MB (53703979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a099a46124988665742eae84cd51e5a2ec69ba12a5a0324bfdecb15c9fcca0ec`  
		Last Modified: Wed, 26 Jul 2023 01:13:29 GMT  
		Size: 141.6 MB (141565305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b34da4dc58b8551e76f9c5e3c916466191bf7ac36466592eabfa5fc42b738c`  
		Last Modified: Wed, 26 Jul 2023 01:13:20 GMT  
		Size: 2.4 MB (2351394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f357330e1bb51be8f74c4f777503bc25b17ba6494113f8c22da6676ec2c430`  
		Last Modified: Wed, 26 Jul 2023 01:13:22 GMT  
		Size: 58.8 MB (58820537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
