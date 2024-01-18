## `clojure:temurin-17-boot-bookworm-slim`

```console
$ docker pull clojure@sha256:f0ea298d31e6241874a0eb493bd3742beb1b837206dce2ef7c42a85acb55c68c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8fc47099b7ca8c7f961835cbc391d45d993da6ecd7c18cbefa340555d150f0c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.3 MB (236318870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9496f509fb6b6d7ad97f4e74ea7c3881ff6dd98bb9c2885b669fe2c744b94b74`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:52:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 14:19:46 GMT
COPY dir:df4bc774e538040069d2de3701d4e1bdcb670139eb43073b03a326d09099ff77 in /opt/java/openjdk 
# Wed, 17 Jan 2024 14:19:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 14:19:47 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 17 Jan 2024 14:19:47 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 17 Jan 2024 14:19:48 GMT
WORKDIR /tmp
# Wed, 17 Jan 2024 14:19:54 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 17 Jan 2024 14:19:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 17 Jan 2024 14:19:54 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 17 Jan 2024 14:20:12 GMT
RUN boot
# Wed, 17 Jan 2024 14:20:13 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 17 Jan 2024 14:20:13 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 17 Jan 2024 14:20:13 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253a46fd3dbe7a206ac008f95cf1f4bf7a0a42da2fe3654b652e9c9dae11d877`  
		Last Modified: Wed, 17 Jan 2024 14:56:59 GMT  
		Size: 144.9 MB (144873978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53f7672bdf38ce62beaf286055bee8ded39306222c9de14e76147d0772d8c51`  
		Last Modified: Wed, 17 Jan 2024 14:56:48 GMT  
		Size: 3.5 MB (3498046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f341449d2890ae3aad754f3a895d6a08ce5f88b3b14ed62738a7cdbbcf6dd8`  
		Last Modified: Wed, 17 Jan 2024 14:56:51 GMT  
		Size: 58.8 MB (58820526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93402a901193350fd12e1f1eff6379acf3e98e1e17d77d8629dc6ce1ea10eb73`  
		Last Modified: Wed, 17 Jan 2024 14:56:47 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e1c7f7a81e7bd5f399c1d3bbec8e76e9bc43a7b96b882c2ea4e58cf00db28524
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (234981895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c1c4d9e763cd962226aff3060c8fb63547d06c0d3b932da6d1bdc60928ae579`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:44 GMT
ADD file:70e4f0c71f88c97c8db279b998c10d4943954d304ff9f51875c3699a4dc5ee4e in / 
# Thu, 11 Jan 2024 02:40:45 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 07:59:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:28:39 GMT
COPY dir:5c06fb4b5daaa6784ba170c718d211b83c290b42eddb2ce95b7a2b1603c507ca in /opt/java/openjdk 
# Wed, 17 Jan 2024 09:28:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:28:42 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 17 Jan 2024 09:28:42 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 17 Jan 2024 09:28:42 GMT
WORKDIR /tmp
# Wed, 17 Jan 2024 09:28:47 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 17 Jan 2024 09:28:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 17 Jan 2024 09:28:47 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 17 Jan 2024 09:29:03 GMT
RUN boot
# Wed, 17 Jan 2024 09:29:03 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 17 Jan 2024 09:29:03 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 17 Jan 2024 09:29:03 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a5573528b1f0cf2f5d87c94fe0aee9d8967d5de98258be9303c3c6fa477824ec`  
		Last Modified: Thu, 11 Jan 2024 02:44:04 GMT  
		Size: 29.2 MB (29157335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ec6808b922620606ea5e24590df6eaa935e6797301a16b35c7cca4bd3a011c`  
		Last Modified: Wed, 17 Jan 2024 09:42:10 GMT  
		Size: 143.7 MB (143681766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2672ba4c87899b501f0f582e4e302b2ca0b75dce8d0f32323f7bbc1148f45f`  
		Last Modified: Wed, 17 Jan 2024 09:42:01 GMT  
		Size: 3.3 MB (3321996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ea260b01bfbbc88b11ec1279887fdb4bc2bddba38192b264069812089c9b7b`  
		Last Modified: Wed, 17 Jan 2024 09:42:04 GMT  
		Size: 58.8 MB (58820399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e22e9c201e9b6c31751dd77217eb182ac753c242bc8aa2e08b60666008fbe4d6`  
		Last Modified: Wed, 17 Jan 2024 09:42:01 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
