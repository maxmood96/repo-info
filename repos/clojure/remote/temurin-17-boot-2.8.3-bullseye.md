## `clojure:temurin-17-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:2a4f5ffe633cacf4a82014ce8613179c1a87f13e8e64552338f23ce355075ba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:f69ab445c548844ce51d89e909be54e43c85364bb33f35c864382d07b74abd44
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.2 MB (261166179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3527570b8afcf45cbc55d2dec0c172a724348fd03e74b0e555e15ec0d09cfe9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:11 GMT
ADD file:ff6bc341b5945acf6b9c190d70b5f5806fb3fae7b5c568ad6395aec1b95ba89c in / 
# Tue, 12 Mar 2024 01:21:11 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:12:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 03:07:20 GMT
COPY dir:88c5118aff6896f6ed535dcde576d68ef88ded459cca013e0f9beb3e430ebb52 in /opt/java/openjdk 
# Thu, 28 Mar 2024 03:07:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 03:07:21 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 28 Mar 2024 03:07:21 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 28 Mar 2024 03:07:21 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 03:07:27 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 28 Mar 2024 03:07:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 28 Mar 2024 03:07:27 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 28 Mar 2024 03:07:44 GMT
RUN boot
# Thu, 28 Mar 2024 03:07:44 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 28 Mar 2024 03:07:44 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 28 Mar 2024 03:07:44 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ec335f17d0c74f7a270925cb1bbd29acc72ae904c6f4570f9ae369e3eebb64ed`  
		Last Modified: Tue, 12 Mar 2024 01:25:59 GMT  
		Size: 55.1 MB (55084969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40bcd404f330742d08e449c864937a0247411adf1e0630d702b0d270a8c84eae`  
		Last Modified: Thu, 28 Mar 2024 03:24:58 GMT  
		Size: 144.9 MB (144893082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9decfce24eede648bd63be5c7b15fc6535a164fdf5fa89966110bc04239289`  
		Last Modified: Thu, 28 Mar 2024 03:24:47 GMT  
		Size: 2.4 MB (2367343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408cad15645ddc894e32ca3732e76d0f015e5447071d8a3f8d6c2e39b1e31bfa`  
		Last Modified: Thu, 28 Mar 2024 03:24:50 GMT  
		Size: 58.8 MB (58820384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574389fb16552f0c8a2ece16841f81c19ded6ee831473bec0128a9dd7227c8a9`  
		Last Modified: Thu, 28 Mar 2024 03:24:46 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:415bd993f23185dc8a4098b86159fb3e51728a710a81c98ac79e04bb12999488
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258626828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a55e5b157595a087f9a942538762d82b8b3b8404bd8a1f4eb36311790d997e6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:30 GMT
ADD file:6fedb173fe261ff0e13b004ca692b7edcc74dcc3c4384fee092b96ef9508992c in / 
# Wed, 10 Apr 2024 00:40:30 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:39:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 04:49:17 GMT
COPY dir:a5d0039514ccd79689a0ea6094d70ca92113e8cbcc38d473b7c0fcc04a1f496a in /opt/java/openjdk 
# Wed, 10 Apr 2024 04:49:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 04:49:20 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 10 Apr 2024 04:49:20 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 10 Apr 2024 04:49:20 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 04:49:25 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 10 Apr 2024 04:49:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 10 Apr 2024 04:49:25 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 10 Apr 2024 04:49:43 GMT
RUN boot
# Wed, 10 Apr 2024 04:49:43 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 10 Apr 2024 04:49:43 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 10 Apr 2024 04:49:43 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:197947a07d5f6c6ff020ca65dcea4e52671f85f67bee1b59af46cb0dc36580d9`  
		Last Modified: Wed, 10 Apr 2024 00:44:24 GMT  
		Size: 53.7 MB (53729176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2939a283289857fd9f4ea3521a7268b507e7bf734c8486df9de0c5819576db`  
		Last Modified: Wed, 10 Apr 2024 05:05:00 GMT  
		Size: 143.7 MB (143720921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c0ad40a0fcfa34c251611a0d9a60866796c4b50f03f5060f824b03518acd32`  
		Last Modified: Wed, 10 Apr 2024 05:04:51 GMT  
		Size: 2.4 MB (2355767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be277260a2c6bc246bcb53c637a59a37810f2966400852010ac38e4200ccd9b`  
		Last Modified: Wed, 10 Apr 2024 05:04:53 GMT  
		Size: 58.8 MB (58820565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d5344b39b82ab2c3da1f794d1788939e1cee9db980a28138cb10cfd565d025`  
		Last Modified: Wed, 10 Apr 2024 05:04:50 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
