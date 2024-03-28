## `clojure:temurin-17-boot-bookworm-slim`

```console
$ docker pull clojure@sha256:d243fa2cdef634164b5a7298652987d4e831b24358e88d3c60aa4275a4a159f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3a8864fc58e6f5ae5863a29b6201296f8d918ab4a5343eb38a7b47ecad13b4bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.3 MB (236336501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16f9cbfb5206e1a48b3bc6b87357e381435d50e4b25df6b001483c3f768c4d32`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:11:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 03:06:45 GMT
COPY dir:88c5118aff6896f6ed535dcde576d68ef88ded459cca013e0f9beb3e430ebb52 in /opt/java/openjdk 
# Thu, 28 Mar 2024 03:06:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 03:06:47 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 28 Mar 2024 03:06:47 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 28 Mar 2024 03:06:47 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 03:06:53 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 28 Mar 2024 03:06:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 28 Mar 2024 03:06:53 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 28 Mar 2024 03:07:10 GMT
RUN boot
# Thu, 28 Mar 2024 03:07:10 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 28 Mar 2024 03:07:10 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 28 Mar 2024 03:07:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db34d09da7ef0b7c10d1180bf5afb0a7cc04cfc2fef22a109260b226f6f0804c`  
		Last Modified: Thu, 28 Mar 2024 03:24:38 GMT  
		Size: 144.9 MB (144893128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a27288ee4940bc79895d78f50acd814dbd070038c5ec294921e162ed47cf4a`  
		Last Modified: Thu, 28 Mar 2024 03:24:27 GMT  
		Size: 3.5 MB (3498223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f222ec1e0face72cd4faf2c29985a8dfbc1afc98b22b5cdff42256f9e0c42f00`  
		Last Modified: Thu, 28 Mar 2024 03:24:30 GMT  
		Size: 58.8 MB (58820569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc088ebeabfbf744927a69f4818382f4b49f0d8a9dd5cdeb18afeb829f6a975`  
		Last Modified: Thu, 28 Mar 2024 03:24:26 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bookworm-slim` - linux; arm64 variant v8

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
