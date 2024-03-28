## `clojure:temurin-17-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:df6f404542e5942304a357519712f4b661676dfa389a89bc3326c48451cd6d0c
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
$ docker pull clojure@sha256:968832b8e882f4457d0409c8f9bcacd36c8908fefb49b05dbdaf3e004d4116f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233677845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51100e9ea43e9bdf4a50c23c73cc6d838750c7b940ae4194c72c728a39767c1d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:45:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 02:40:27 GMT
COPY dir:a5d0039514ccd79689a0ea6094d70ca92113e8cbcc38d473b7c0fcc04a1f496a in /opt/java/openjdk 
# Thu, 28 Mar 2024 02:40:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 02:40:31 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 28 Mar 2024 02:40:31 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 28 Mar 2024 02:40:31 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 02:40:36 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 28 Mar 2024 02:40:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 28 Mar 2024 02:40:36 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 28 Mar 2024 02:40:51 GMT
RUN boot
# Thu, 28 Mar 2024 02:40:51 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 28 Mar 2024 02:40:51 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 28 Mar 2024 02:40:51 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:357c1070edd1560e2fca055cc1853bc6786248dbfbf2c71f7238747ddd407d1c`  
		Last Modified: Thu, 28 Mar 2024 02:54:36 GMT  
		Size: 143.7 MB (143720921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e8e46ea45de342ec1d29ed2040d8c7f7b1f7bcfb85671da60762b02be3abe5e`  
		Last Modified: Thu, 28 Mar 2024 02:54:26 GMT  
		Size: 1.1 MB (1065009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afeca64414fb509646385272faab89e7e3946d373f23164dce43d105d4fb774b`  
		Last Modified: Thu, 28 Mar 2024 02:54:29 GMT  
		Size: 58.8 MB (58820399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bc51ccb49014430e00c4e68dc39132ce2f7f520ce4c9399109105f57fedd75d`  
		Last Modified: Thu, 28 Mar 2024 02:54:26 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
