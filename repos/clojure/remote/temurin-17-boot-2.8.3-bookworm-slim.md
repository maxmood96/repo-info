## `clojure:temurin-17-boot-2.8.3-bookworm-slim`

```console
$ docker pull clojure@sha256:35add764d439d7735cafe8daef77d2b5f1705929af1e237c1f0b88f542847b42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bookworm-slim` - linux; amd64

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

### `clojure:temurin-17-boot-2.8.3-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c4c9e532e326c282cca4d60bd5b3ba98f94cd210441690a672144acc2f07bcaf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235026177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f628f3a8554997c335aad900624f4f02c87cf15a9c30e6618790d798b01473af`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:23 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Wed, 10 Apr 2024 00:40:23 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:38:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 04:48:43 GMT
COPY dir:a5d0039514ccd79689a0ea6094d70ca92113e8cbcc38d473b7c0fcc04a1f496a in /opt/java/openjdk 
# Wed, 10 Apr 2024 04:48:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 04:48:46 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 10 Apr 2024 04:48:46 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 10 Apr 2024 04:48:46 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 04:48:52 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 10 Apr 2024 04:48:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 10 Apr 2024 04:48:52 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 10 Apr 2024 04:49:09 GMT
RUN boot
# Wed, 10 Apr 2024 04:49:09 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 10 Apr 2024 04:49:09 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 10 Apr 2024 04:49:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9897cc6a50c882c12c7e31572662e5a0fcda5a92d038d300710856a372e1ad71`  
		Last Modified: Wed, 10 Apr 2024 05:04:42 GMT  
		Size: 143.7 MB (143720940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b13cf9f4b298094a1a1f264e24653f95c9068297fb66dcc9bc4e517a7f001ce3`  
		Last Modified: Wed, 10 Apr 2024 05:04:34 GMT  
		Size: 3.3 MB (3322181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8deb13108b4ddbdbd2805cc13717f209b9d983b13b9c87242fa8653e1bff3099`  
		Last Modified: Wed, 10 Apr 2024 05:04:36 GMT  
		Size: 58.8 MB (58820498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223510b34f46a274310d006dcbfea7e2302b21caec4cf9feca3e0fcbec191b3b`  
		Last Modified: Wed, 10 Apr 2024 05:04:33 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
