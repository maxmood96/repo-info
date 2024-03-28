## `clojure:temurin-17-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:2c9adf3da2c5f4da813c4215e82ae73f5f94c33bef82fb8f8c20abe24fb27441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:18fd27baf555eb8bee3400d6e18810e95d28ddc5e1707daf86be42b104f4af1c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.2 MB (236214158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d932f98cfedd5b25da0c3b260201482e229bdc9a2130c978d76b44250da1c84`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:12:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 Mar 2024 06:24:15 GMT
COPY dir:3be96ae7faea81e90455993c99b71c9b45986c7e71f70fc577ab97699c92b508 in /opt/java/openjdk 
# Tue, 12 Mar 2024 06:24:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 06:24:16 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 12 Mar 2024 06:24:16 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 12 Mar 2024 06:24:16 GMT
WORKDIR /tmp
# Tue, 12 Mar 2024 06:24:22 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 12 Mar 2024 06:24:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 12 Mar 2024 06:24:22 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 12 Mar 2024 06:24:39 GMT
RUN boot
# Tue, 12 Mar 2024 06:24:40 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 12 Mar 2024 06:24:40 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 12 Mar 2024 06:24:40 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa99337ab9effaa7179d80eb78de5d10c8c8d850b1473f6d62d507d309df157`  
		Last Modified: Tue, 12 Mar 2024 06:41:30 GMT  
		Size: 144.9 MB (144893175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d9a1233b232eb59fda982edbb11ef5a664d696e56eae43500f4d325bcdec77`  
		Last Modified: Tue, 12 Mar 2024 06:41:19 GMT  
		Size: 1.1 MB (1077712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e2e80a0311370540adbc517492e582fc6530d50935544002b1fbf50f06dc55`  
		Last Modified: Tue, 12 Mar 2024 06:41:22 GMT  
		Size: 58.8 MB (58820384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7181631927eaef0b10bfa3b783219ce36b3aa27d947c68a9aadb9430a7b68134`  
		Last Modified: Tue, 12 Mar 2024 06:41:18 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye-slim` - linux; arm64 variant v8

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
