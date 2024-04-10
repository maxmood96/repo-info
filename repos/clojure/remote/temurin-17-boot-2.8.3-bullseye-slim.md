## `clojure:temurin-17-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:979ae4344f3ef74733a187130ca87f488892a5efab031856f1bbd14b4f455624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:04b0b0200fe6615cfa4650c547489ef0a5dc0866bee3de682f41a8cd81b61a54
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.2 MB (236214060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b670d7220fb73af0d5b199761a7948ce25a70a10c8947f3efbfdd9d8ecddddc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:12:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 03:07:49 GMT
COPY dir:88c5118aff6896f6ed535dcde576d68ef88ded459cca013e0f9beb3e430ebb52 in /opt/java/openjdk 
# Thu, 28 Mar 2024 03:07:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 03:07:50 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 28 Mar 2024 03:07:50 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 28 Mar 2024 03:07:50 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 03:07:56 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 28 Mar 2024 03:07:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 28 Mar 2024 03:07:56 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 28 Mar 2024 03:08:12 GMT
RUN boot
# Thu, 28 Mar 2024 03:08:13 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 28 Mar 2024 03:08:13 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 28 Mar 2024 03:08:13 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56dee0771562f1b4ec86637223b99c85058c85add467447be5a3635c7d84bfb9`  
		Last Modified: Thu, 28 Mar 2024 03:25:18 GMT  
		Size: 144.9 MB (144893095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e5914ce0da5a81069f92acf7d50c1e715a1e4b9ed08f393fdd8e5a1285079c`  
		Last Modified: Thu, 28 Mar 2024 03:25:07 GMT  
		Size: 1.1 MB (1077759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83bb629bbca9ddcbae10e221821c85dec344f7db5aaeb8c798459643ce831845`  
		Last Modified: Thu, 28 Mar 2024 03:25:10 GMT  
		Size: 58.8 MB (58820316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17fb3e5e711c7ee1fc4e06d23d0633195fdf44436e1a4c17fbcbf3cf77703b19`  
		Last Modified: Thu, 28 Mar 2024 03:25:06 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

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
