## `clojure:temurin-17-boot-2.8.3-bookworm-slim`

```console
$ docker pull clojure@sha256:66fb2e6ccda1fd5ffb9f102ee63f2389b219033e3801cbcae6cd1c54ba24095a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:722bf2f80a2f51bc583604e3444faeb9c2adcc38014525e2afe0093d28173579
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.3 MB (236337219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad84e90fa06eccd5500fe2bf0e9188f363a71a1d02b6fb5359a899d74b71e07`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:52:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:17:59 GMT
COPY dir:f32129cdf16cd5eee81dc24c5e5457011e489f134c2a5ee643ddf8ee33a43952 in /opt/java/openjdk 
# Wed, 24 Jan 2024 22:18:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 22:18:01 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 24 Jan 2024 22:18:01 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 24 Jan 2024 22:18:01 GMT
WORKDIR /tmp
# Wed, 24 Jan 2024 22:18:07 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 24 Jan 2024 22:18:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jan 2024 22:18:07 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 24 Jan 2024 22:18:24 GMT
RUN boot
# Wed, 24 Jan 2024 22:18:24 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 24 Jan 2024 22:18:24 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jan 2024 22:18:25 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d23b553379c1c34e8a209662d4d06b0c36d1a2ef68847e67b884ce8ba6c997`  
		Last Modified: Wed, 24 Jan 2024 22:42:14 GMT  
		Size: 144.9 MB (144892539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2582a267c02b12e87ce5dfa4430c5a91db493c3f88327c77d8a60c64a09c5d5e`  
		Last Modified: Wed, 24 Jan 2024 22:42:02 GMT  
		Size: 3.5 MB (3498019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f9b080a70a542c78f428271db06ae9f768b0f65a0eeb5842293050a199cb21`  
		Last Modified: Wed, 24 Jan 2024 22:42:05 GMT  
		Size: 58.8 MB (58820340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a3b541863f4efd85d45bcb45dd4e4ac0fba89b8bed4a5cef59f587a5eef0cc`  
		Last Modified: Wed, 24 Jan 2024 22:42:01 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:be02f99ce26788c581b4569ebd60f1bfd1351d81e16f424a99dd90523b39af33
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235020945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849eaacdc47cf0868e2289851aa04b5ceda0a42299740b94d32a62b74ed79260`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:44 GMT
ADD file:70e4f0c71f88c97c8db279b998c10d4943954d304ff9f51875c3699a4dc5ee4e in / 
# Thu, 11 Jan 2024 02:40:45 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 07:59:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:21:09 GMT
COPY dir:7c9e57a7678108e8f16bbe5ccb6616df59216fd52f6dd8321cc6163370ace185 in /opt/java/openjdk 
# Wed, 24 Jan 2024 22:21:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 22:21:13 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 24 Jan 2024 22:21:13 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 24 Jan 2024 22:21:13 GMT
WORKDIR /tmp
# Wed, 24 Jan 2024 22:21:18 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 24 Jan 2024 22:21:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jan 2024 22:21:18 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 24 Jan 2024 22:21:33 GMT
RUN boot
# Wed, 24 Jan 2024 22:21:33 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 24 Jan 2024 22:21:33 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jan 2024 22:21:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a5573528b1f0cf2f5d87c94fe0aee9d8967d5de98258be9303c3c6fa477824ec`  
		Last Modified: Thu, 11 Jan 2024 02:44:04 GMT  
		Size: 29.2 MB (29157335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436f3867c97cc84e2f78eb80b1d2e104d0f0cbf0eef4964d7f57ea9e843f7da0`  
		Last Modified: Wed, 24 Jan 2024 22:41:41 GMT  
		Size: 143.7 MB (143720871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:671c6e1d1f6f79d0d26da2ce8d24c437050742fa1cf0fd3c8b48bafae2cfdb8d`  
		Last Modified: Wed, 24 Jan 2024 22:41:33 GMT  
		Size: 3.3 MB (3322035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7090bc01c9c1bb5326dfc5604342cb655fbf97e3d41b7499ac504c0ff55d5764`  
		Last Modified: Wed, 24 Jan 2024 22:41:35 GMT  
		Size: 58.8 MB (58820304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db9d93811e3d10c071f40606af38b15e6ae655e22ca2762e142976c414e1a999`  
		Last Modified: Wed, 24 Jan 2024 22:41:32 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
