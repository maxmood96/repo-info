## `clojure:temurin-17-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:1be560806c19d3688fee99abd363809dedd24e3ab6e6a93aa037430e9450425d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1e898ddbd5d969c09dae958f806c54d1cab48e50e1c4373dd9ec48c970b6b7fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.2 MB (236210749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40065ebd33e9bfda7274c923e91940ff5aa6d0726fe7bef375679fd9bb145502`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:19:03 GMT
COPY dir:f32129cdf16cd5eee81dc24c5e5457011e489f134c2a5ee643ddf8ee33a43952 in /opt/java/openjdk 
# Wed, 24 Jan 2024 22:19:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 22:19:04 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 24 Jan 2024 22:19:04 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 24 Jan 2024 22:19:04 GMT
WORKDIR /tmp
# Wed, 24 Jan 2024 22:19:10 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 24 Jan 2024 22:19:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jan 2024 22:19:10 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 24 Jan 2024 22:19:27 GMT
RUN boot
# Wed, 24 Jan 2024 22:19:27 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 24 Jan 2024 22:19:28 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jan 2024 22:19:28 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f6a169c7b2e3bcb5d7cd2f5e20b14951a9a4de6a9a37fb9deae3f60abdfdfc`  
		Last Modified: Wed, 24 Jan 2024 22:42:54 GMT  
		Size: 144.9 MB (144892540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72caf191f18c0881e1bd1daccdf66bdabf527b2d18943849cee9bf296783f2fb`  
		Last Modified: Wed, 24 Jan 2024 22:42:42 GMT  
		Size: 1.1 MB (1079483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7832cf575dfdc39b69dc25c376a284b8f2498378714995f0cfbb9f91b4148744`  
		Last Modified: Wed, 24 Jan 2024 22:42:45 GMT  
		Size: 58.8 MB (58820371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b298f4dc16194e888198f70d9d1c5b30fe653db911f346b8d8ee00209481222`  
		Last Modified: Wed, 24 Jan 2024 22:42:42 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:084981b127db64e8b051954cc56fb60e9f952df9ad40c62a5f12ff2cb0fa81a2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233672522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1d00bfe8412f3acf08735279d2f95c4e6469797d3f0f65e9a9ca785a9acdece`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:22:05 GMT
COPY dir:7c9e57a7678108e8f16bbe5ccb6616df59216fd52f6dd8321cc6163370ace185 in /opt/java/openjdk 
# Wed, 24 Jan 2024 22:22:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 22:22:09 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 24 Jan 2024 22:22:09 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 24 Jan 2024 22:22:09 GMT
WORKDIR /tmp
# Wed, 24 Jan 2024 22:22:13 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 24 Jan 2024 22:22:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jan 2024 22:22:14 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 24 Jan 2024 22:22:28 GMT
RUN boot
# Wed, 24 Jan 2024 22:22:29 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 24 Jan 2024 22:22:29 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jan 2024 22:22:29 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0c3b9adaf68b2614f4af45d6b1026884d5f113942c4d76b2763cebc39e27ca`  
		Last Modified: Wed, 24 Jan 2024 22:42:21 GMT  
		Size: 143.7 MB (143720871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7788e0490d2b2fa8b837175a198776ee16acffd004eae1a6bf332246b5de097e`  
		Last Modified: Wed, 24 Jan 2024 22:42:11 GMT  
		Size: 1.1 MB (1066838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0ab61a6ca8b90ab0060400c12dbd77f2f9ff54ad084f52319d23e5916d9fc2`  
		Last Modified: Wed, 24 Jan 2024 22:42:14 GMT  
		Size: 58.8 MB (58820403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d96ee137699e7345e7a26c20bfa9516a78d65e491d4c77980bd20b3e64196ab`  
		Last Modified: Wed, 24 Jan 2024 22:42:10 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
