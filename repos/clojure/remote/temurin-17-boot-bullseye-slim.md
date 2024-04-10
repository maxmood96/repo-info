## `clojure:temurin-17-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:e18b8887d8978ba53ab0889bf068595f696d4b9687edb3ad4e85d93e4a1293df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0e070ed55518ef057c118338d2061d7250245b9ec7746021d2d7459d1388a39d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.2 MB (236219578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee912f527565de31deb9ed8c4b5becc1c8ce0d688d365236f2aecd8217f9a9af`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 06:30:06 GMT
COPY dir:88c5118aff6896f6ed535dcde576d68ef88ded459cca013e0f9beb3e430ebb52 in /opt/java/openjdk 
# Wed, 10 Apr 2024 06:30:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:30:08 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 10 Apr 2024 06:30:08 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 10 Apr 2024 06:30:08 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 06:30:13 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 10 Apr 2024 06:30:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 10 Apr 2024 06:30:14 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 10 Apr 2024 06:30:31 GMT
RUN boot
# Wed, 10 Apr 2024 06:30:31 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 10 Apr 2024 06:30:31 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 10 Apr 2024 06:30:32 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b214aac1e4f25666ac6825b94aba5501d4d8f133c4457fbbf9fa5777dcf69a2`  
		Last Modified: Wed, 10 Apr 2024 06:46:40 GMT  
		Size: 144.9 MB (144893128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7f54c255e26cf8ba1cf47bd464a62c39c5421dec181a035fd493295cb62c2c`  
		Last Modified: Wed, 10 Apr 2024 06:46:28 GMT  
		Size: 1.1 MB (1077693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db37a45837299f646616dad349fe761f026e8b34f457c2e13c87fc51543dc769`  
		Last Modified: Wed, 10 Apr 2024 06:46:31 GMT  
		Size: 58.8 MB (58820618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c355548f3576e6e8a261be6b432865cba12db59d3f11523b873d9acb7d4ad258`  
		Last Modified: Wed, 10 Apr 2024 06:46:28 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bc2bed43f427efdf490208f8387033101e02ba41c2eeec16947fca9d72bba40e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233683140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ab134dc565da6bf647cd98b1dabfafc6ecd15653a39d5a2f5397afb6f4b8800`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:39:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 04:49:50 GMT
COPY dir:a5d0039514ccd79689a0ea6094d70ca92113e8cbcc38d473b7c0fcc04a1f496a in /opt/java/openjdk 
# Wed, 10 Apr 2024 04:49:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 04:49:54 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 10 Apr 2024 04:49:54 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 10 Apr 2024 04:49:54 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 04:49:58 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 10 Apr 2024 04:49:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 10 Apr 2024 04:49:59 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 10 Apr 2024 04:50:15 GMT
RUN boot
# Wed, 10 Apr 2024 04:50:16 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 10 Apr 2024 04:50:16 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 10 Apr 2024 04:50:16 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b297b0c3afc17da47d0f29478d0d2915f1dbc665d37c692e3982a3ce7ab9574c`  
		Last Modified: Wed, 10 Apr 2024 05:05:18 GMT  
		Size: 143.7 MB (143720891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09176940e7bb16e509f5acfdcc23051e124868f0bb2e2d7462eba60b42eb7c75`  
		Last Modified: Wed, 10 Apr 2024 05:05:09 GMT  
		Size: 1.1 MB (1064964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a60a2d5b355376ae3bea45fe4f4c080e310f5ec655944ab519c21ed66f4a4a`  
		Last Modified: Wed, 10 Apr 2024 05:05:12 GMT  
		Size: 58.8 MB (58820580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1628351235890b716dd691fb08d96fb04f9921ed4b3cbb060f11751907d052`  
		Last Modified: Wed, 10 Apr 2024 05:05:09 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
