## `clojure:temurin-17-boot-2.8.3-bookworm`

```console
$ docker pull clojure@sha256:9c24353bd73dd098cca8530b670571d7a9d1cfa1986bc7e29d2eea84b387a325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:5325799d4349e13dbc855835a881a28f951e454e99b867acf0eeb58aa6d01e17
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.8 MB (258807380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c41d6f29ca1fc009617ccf35aff9202a557a6c83013aead090acbb8f4791100`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:37 GMT
ADD file:1e4dd5dab602337b5d5ef8d84b8dbe8b1ac62225f077b29b27d045842486d8e2 in / 
# Wed, 11 Oct 2023 18:34:37 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 01:26:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:52:04 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Tue, 31 Oct 2023 00:52:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 00:52:06 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 31 Oct 2023 00:52:06 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 31 Oct 2023 00:52:06 GMT
WORKDIR /tmp
# Tue, 31 Oct 2023 00:52:12 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 31 Oct 2023 00:52:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 31 Oct 2023 00:52:12 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 31 Oct 2023 00:52:29 GMT
RUN boot
# Tue, 31 Oct 2023 00:52:29 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 31 Oct 2023 00:52:30 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 31 Oct 2023 00:52:30 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0a9573503463fd3166b5b1f34a7720dac28609e98d731e50e7068f92e79b8545`  
		Last Modified: Wed, 11 Oct 2023 18:39:10 GMT  
		Size: 49.6 MB (49582224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf57dbab86b78812253ab1badcea63f1d4cb3932af887bec964cc1ab69c7ad7`  
		Last Modified: Tue, 31 Oct 2023 01:12:11 GMT  
		Size: 144.9 MB (144873969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d3908d239c1d735ea2395b9ad12c053bd79d872438c2fdb08a5aac0e3d8b84`  
		Last Modified: Tue, 31 Oct 2023 01:12:00 GMT  
		Size: 5.5 MB (5530326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be01ff51cfb29eb2c85707ce5dcd2bed38519e98de069d68bb010bf14efac03e`  
		Last Modified: Tue, 31 Oct 2023 01:12:03 GMT  
		Size: 58.8 MB (58820460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94d2013e12475ac27a891875d687da773f4767dc6e16829d75c6dcd91fd4c51`  
		Last Modified: Tue, 31 Oct 2023 01:11:59 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:08af62daf7df0c72552a7bc4e98779995e752b99320035ad87aa01a233ceeecc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.5 MB (257468296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24bd9d5c640bff64913ae714c28eb6bd02812c65d89af984db61f8422f562769`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:43 GMT
ADD file:bf4264671bd91eb30c67d512144ebcf7f5c55a3e490ebe7876fa9b20d433bf7b in / 
# Wed, 11 Oct 2023 18:24:44 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 00:57:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 01:04:55 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 01:04:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 01:04:58 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 31 Oct 2023 01:04:58 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 31 Oct 2023 01:04:59 GMT
WORKDIR /tmp
# Tue, 31 Oct 2023 01:05:04 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 31 Oct 2023 01:05:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 31 Oct 2023 01:05:04 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 31 Oct 2023 01:05:22 GMT
RUN boot
# Tue, 31 Oct 2023 01:05:22 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 31 Oct 2023 01:05:22 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 31 Oct 2023 01:05:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e720f94321d63ecb6efa873b294dce7eaa1c3a5ddcd5bf7daddf375b955669a4`  
		Last Modified: Wed, 11 Oct 2023 18:28:04 GMT  
		Size: 49.6 MB (49612578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d8e5e52e2f4027035c0b4ddc5b921034970f50db7c28155054a83132fbde7fe`  
		Last Modified: Tue, 31 Oct 2023 01:22:19 GMT  
		Size: 143.7 MB (143681763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:accadede649a38524344312734d2daaa67f32761fbbaa3be0cf71b6b15c4ab95`  
		Last Modified: Tue, 31 Oct 2023 01:22:10 GMT  
		Size: 5.4 MB (5353199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084eb06903470ea283650cc84f73e6b02a9d0b9dce0081006f88194e20a7018c`  
		Last Modified: Tue, 31 Oct 2023 01:22:12 GMT  
		Size: 58.8 MB (58820356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d195559c1a2c3d65a92cc251809bc781a9bf130dc7a7d6a24b47e75702529fc`  
		Last Modified: Tue, 31 Oct 2023 01:22:09 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
