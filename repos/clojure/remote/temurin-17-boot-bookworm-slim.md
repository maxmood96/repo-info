## `clojure:temurin-17-boot-bookworm-slim`

```console
$ docker pull clojure@sha256:e1ad51aa3d1c9374434f249e9b5051d0ee72ef2b85b45f606396e5aea271ec2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:bf80b081007ddb26e7050455c5fcb878e60514b10973679d3a7267c86a720779
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.3 MB (236343343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe226ec356ff6c2b35e5c13fc4a29bb08f5c6bb40773316eb57c926ce27c29f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:17:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 06:28:57 GMT
COPY dir:88c5118aff6896f6ed535dcde576d68ef88ded459cca013e0f9beb3e430ebb52 in /opt/java/openjdk 
# Wed, 10 Apr 2024 06:28:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:28:58 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 10 Apr 2024 06:28:59 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 10 Apr 2024 06:28:59 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 06:29:05 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 10 Apr 2024 06:29:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 10 Apr 2024 06:29:05 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 10 Apr 2024 06:29:23 GMT
RUN boot
# Wed, 10 Apr 2024 06:29:23 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 10 Apr 2024 06:29:23 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 10 Apr 2024 06:29:23 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9330ece2b18c5aab4f640b1856df6879bdb1041bb0b0f67a4d3195236bed4e0`  
		Last Modified: Wed, 10 Apr 2024 06:45:59 GMT  
		Size: 144.9 MB (144893073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b81fecd7b599040a8ced80f00ced9f2fa6b3be224cd3eca42529a72592c082`  
		Last Modified: Wed, 10 Apr 2024 06:45:49 GMT  
		Size: 3.5 MB (3498207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0589d1cc80d6b5fb2f6525d7bcd4c0774bf89021e7fc755bd34386afc71e76`  
		Last Modified: Wed, 10 Apr 2024 06:45:51 GMT  
		Size: 58.8 MB (58820305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1588e02b0b7af2b3639a505fa812431c6e93663a20b4b08cd4cca3c293dc538`  
		Last Modified: Wed, 10 Apr 2024 06:45:48 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bookworm-slim` - linux; arm64 variant v8

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
