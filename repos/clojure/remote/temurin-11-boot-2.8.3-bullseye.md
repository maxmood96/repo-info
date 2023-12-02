## `clojure:temurin-11-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:67c1369a6ec2620dc099386687856c0c37b03085a5e225492864184759725ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:df9473f1c8cb0b37b44e192b64157d555c73ab400493ff9c5a4eb532e644de7d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261513476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e87f6954d94f3a516f4cd02947027a0b93aeadef948abfe9f249638612ee080`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:46 GMT
ADD file:71543995e4d314b0c86da5ddf8e0cb74649767d30b3e5b6261360de354f0567b in / 
# Tue, 21 Nov 2023 05:21:46 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 09:55:14 GMT
COPY dir:d20aeb749bf0b3fe533952f7903b6aa08724fe8bf03e369130d4e2a6ff71bd3f in /opt/java/openjdk 
# Sat, 02 Dec 2023 09:55:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 09:55:16 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 02 Dec 2023 09:55:16 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 02 Dec 2023 09:55:16 GMT
WORKDIR /tmp
# Sat, 02 Dec 2023 09:55:22 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 02 Dec 2023 09:55:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 02 Dec 2023 09:55:22 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 02 Dec 2023 09:55:39 GMT
RUN boot
# Sat, 02 Dec 2023 09:55:39 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:d1da99c2f14827498c4a9bb3623ae909b44564bdabad1802f064169069df81fb`  
		Last Modified: Tue, 21 Nov 2023 05:26:17 GMT  
		Size: 55.1 MB (55057903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100270be7c7a032e8711a8951a07234acf8e56368673f84b3d9df6b333e239f7`  
		Last Modified: Sat, 02 Dec 2023 10:14:22 GMT  
		Size: 145.3 MB (145266419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286ff7c42896e17f1e4d033ec20bbaffae9da5a0fcdd9d976bdcc78df50f5bfd`  
		Last Modified: Sat, 02 Dec 2023 10:14:11 GMT  
		Size: 2.4 MB (2368745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bdddfb94c4f5be025956d673408d143b43ce42e5401751333089e6115bbcdeb`  
		Last Modified: Sat, 02 Dec 2023 10:14:14 GMT  
		Size: 58.8 MB (58820409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6551823c01e59ec11503948b22e69156619580585ef7a660783af1c0fbf10b1f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.9 MB (256887546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e784e18de9153b6c84170342bff836284a84ac85ecba5a058fdcd4e34027e00`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:13 GMT
ADD file:614987b9855939825ad2383e7bacbf14ea208d74906982bba3a67126702c8371 in / 
# Tue, 21 Nov 2023 06:27:13 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 08:45:30 GMT
COPY dir:201fdbb3aef6b177b9038d3dd5bbe865568281c78c7bc0c153b57943d571a0b6 in /opt/java/openjdk 
# Sat, 02 Dec 2023 08:45:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 08:45:33 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 02 Dec 2023 08:45:33 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 02 Dec 2023 08:45:33 GMT
WORKDIR /tmp
# Sat, 02 Dec 2023 08:45:39 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 02 Dec 2023 08:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 02 Dec 2023 08:45:39 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 02 Dec 2023 08:45:55 GMT
RUN boot
# Sat, 02 Dec 2023 08:45:55 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:bbf382c14c7b19b81c612f639e09e6a7b04eccd4481d0abac48b8ace9faae3b3`  
		Last Modified: Tue, 21 Nov 2023 06:30:47 GMT  
		Size: 53.7 MB (53707872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c831d867f0110557a683e007e761887afd75ea0947b774de2aedd6660dc51bc`  
		Last Modified: Sat, 02 Dec 2023 09:04:13 GMT  
		Size: 142.0 MB (142001789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d12b7149ec2be0f0a5580cae28762cbe7e53be9e57f0e70a4cc16a6284995db6`  
		Last Modified: Sat, 02 Dec 2023 09:04:04 GMT  
		Size: 2.4 MB (2357436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0adf65169126afd45b67a476ac08e81c96cca8dd40d62f9db4669ad0607d4f`  
		Last Modified: Sat, 02 Dec 2023 09:04:06 GMT  
		Size: 58.8 MB (58820449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
