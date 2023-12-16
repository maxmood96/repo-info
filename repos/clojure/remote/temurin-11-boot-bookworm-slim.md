## `clojure:temurin-11-boot-bookworm-slim`

```console
$ docker pull clojure@sha256:583192afcddccfc99524256d12c36fa9d8250f0d040ed20499b8427c75abdb5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:bf879665053ab2bc3d015ede7df091cf863fbf9cf7836f409d0e6156d757a537
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 MB (236738452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b695561a562811af92c4fa3387d8546ab5f6393d07679289bbdfc5f138119f`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:37 GMT
ADD file:d261a6f6921593f1e0b3f472ab1b1822e2c6deb0b369200f0b3370556bfad017 in / 
# Tue, 21 Nov 2023 05:21:37 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:08:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 15:25:14 GMT
COPY dir:7cbebf37ba11e5c859b49d766118c0899546d922ac426dfa1230f08ebde784dc in /opt/java/openjdk 
# Sat, 16 Dec 2023 15:25:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 15:25:15 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 16 Dec 2023 15:25:15 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 16 Dec 2023 15:25:15 GMT
WORKDIR /tmp
# Sat, 16 Dec 2023 15:25:21 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 16 Dec 2023 15:25:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 16 Dec 2023 15:25:22 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 16 Dec 2023 15:25:39 GMT
RUN boot
# Sat, 16 Dec 2023 15:25:39 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:1f7ce2fa46ab3942feabee654933948821303a5a821789dddab2d8c3df59e227`  
		Last Modified: Tue, 21 Nov 2023 05:25:58 GMT  
		Size: 29.1 MB (29149908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a268d5081a881af1000d0b98fde6898d055d544a3cdcfb9c71bf3cfa121ea05b`  
		Last Modified: Sat, 16 Dec 2023 15:44:35 GMT  
		Size: 145.3 MB (145266368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1b4edc41c8aad5edb0dd4c79df3180e8e814525d1eff84858dea027045bd78`  
		Last Modified: Sat, 16 Dec 2023 15:44:24 GMT  
		Size: 3.5 MB (3501710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a37ccb4e0cbc1f06aba189dffa34614bdbf5136b968e8c54f0515a81633600`  
		Last Modified: Sat, 16 Dec 2023 15:44:27 GMT  
		Size: 58.8 MB (58820466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c2aa5052c18f8377f0430ef23e0ce2c41dd43e2743c1a856864b394119d41a06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.3 MB (233326337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8936ebf9c707f2ba4706de2834cac3332a5620edc9130a6f25b39268e5cba8`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:06 GMT
ADD file:869c7d0747a17c53715581a2e862992eb8516c7f45f167821dfa80966a4870d1 in / 
# Tue, 21 Nov 2023 06:27:06 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 13:02:58 GMT
COPY dir:679954ac595f0d76b401a9a7d1ae039330e7231cb1c29892d5f56a0e84534783 in /opt/java/openjdk 
# Sat, 16 Dec 2023 13:03:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 13:03:01 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 16 Dec 2023 13:03:01 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 16 Dec 2023 13:03:01 GMT
WORKDIR /tmp
# Sat, 16 Dec 2023 13:03:06 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 16 Dec 2023 13:03:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 16 Dec 2023 13:03:07 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 16 Dec 2023 13:03:22 GMT
RUN boot
# Sat, 16 Dec 2023 13:03:22 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:2c6d21737d8318aa15c4cc838475029a5efc36c0429e3d8da80d97d0b96d9aaf`  
		Last Modified: Tue, 21 Nov 2023 06:30:30 GMT  
		Size: 29.2 MB (29179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f0b26aa8dbfe6e5e1a473a6a8045854f42236ecbe0b4ad8617e93e1a60c35a`  
		Last Modified: Sat, 16 Dec 2023 13:15:50 GMT  
		Size: 142.0 MB (142001835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07bc85fc7401a7c73140e22d45f217ef56f2cc8102d8b08f3aab28fa2c4a3e3d`  
		Last Modified: Sat, 16 Dec 2023 13:15:42 GMT  
		Size: 3.3 MB (3324865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd5457902a4db2c67fe3059bc642befc82b1ad98a36faaf37c19d0d4b65d2f1`  
		Last Modified: Sat, 16 Dec 2023 13:15:44 GMT  
		Size: 58.8 MB (58820360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
