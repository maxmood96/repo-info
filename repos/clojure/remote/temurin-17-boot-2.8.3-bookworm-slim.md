## `clojure:temurin-17-boot-2.8.3-bookworm-slim`

```console
$ docker pull clojure@sha256:4bb5ce2c3fe039d11853dca16197ec7a5b07bbb633b580b61e9fe05c17af1d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7b7d373cf25a5759133c7ef9fd3f126c8a4b4f8018fde46ac6b90e46be112f5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.3 MB (236336250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6136644dbe3192f3d8f031d312cf494d7aa67ee451cf394f0003d907c1fd6065`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:11:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 Mar 2024 06:23:06 GMT
COPY dir:3be96ae7faea81e90455993c99b71c9b45986c7e71f70fc577ab97699c92b508 in /opt/java/openjdk 
# Tue, 12 Mar 2024 06:23:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 06:23:07 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 12 Mar 2024 06:23:07 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 12 Mar 2024 06:23:07 GMT
WORKDIR /tmp
# Tue, 12 Mar 2024 06:23:13 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 12 Mar 2024 06:23:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 12 Mar 2024 06:23:14 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 12 Mar 2024 06:23:31 GMT
RUN boot
# Tue, 12 Mar 2024 06:23:31 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 12 Mar 2024 06:23:31 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 12 Mar 2024 06:23:31 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccdab3494cdaf5946d15fe4624cb49b52470aafe67e35adf4bcaeef7a1db50f8`  
		Last Modified: Tue, 12 Mar 2024 06:40:51 GMT  
		Size: 144.9 MB (144893191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a1597534a1271109beffae6fefbffd7f1957c4c9b6c6a6af84bb4e3239a604`  
		Last Modified: Tue, 12 Mar 2024 06:40:41 GMT  
		Size: 3.5 MB (3498163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ee005d6c283e9c3061ed33ea7dca0d099c1a6d213bc74091c1ab877bd891d8`  
		Last Modified: Tue, 12 Mar 2024 06:40:43 GMT  
		Size: 58.8 MB (58820317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4066822990b8894ccf62358405b26e08d3f35361c2de23bf8dcf3a2ca4700f`  
		Last Modified: Tue, 12 Mar 2024 06:40:40 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:03d8f3e3f8e7d266be5716228d03eba0ac2e7aad1b1a8edc9418010f359a7c4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235020197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c5cbc6f4aa3c408df449d93e31067bc57766b589ec732414c6168d78139008`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:44:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 02:39:31 GMT
COPY dir:a5d0039514ccd79689a0ea6094d70ca92113e8cbcc38d473b7c0fcc04a1f496a in /opt/java/openjdk 
# Thu, 28 Mar 2024 02:39:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 02:39:34 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 28 Mar 2024 02:39:35 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 28 Mar 2024 02:39:35 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 02:39:40 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 28 Mar 2024 02:39:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 28 Mar 2024 02:39:40 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 28 Mar 2024 02:39:55 GMT
RUN boot
# Thu, 28 Mar 2024 02:39:56 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 28 Mar 2024 02:39:56 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 28 Mar 2024 02:39:56 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76dbb1a530d50bcec96fcd7bbb7abc3fb7a765a01bdf5b5dd96e07107640e6b8`  
		Last Modified: Thu, 28 Mar 2024 02:54:00 GMT  
		Size: 143.7 MB (143720921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57798a7d7194808a8032f1cb5d13ed7404793ca6d5f2ea9f780667eda43d714`  
		Last Modified: Thu, 28 Mar 2024 02:53:52 GMT  
		Size: 3.3 MB (3322134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72732e3eb7b63eaa6b3dad29ec4776a6a60744df8946415c887afb9ef22ac76f`  
		Last Modified: Thu, 28 Mar 2024 02:53:54 GMT  
		Size: 58.8 MB (58820307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38f6603cd2809c168c0de0611fe1249c255355f80a69ae7700b8d3e888a8b7c0`  
		Last Modified: Thu, 28 Mar 2024 02:53:51 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
