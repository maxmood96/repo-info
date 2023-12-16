## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:6a006f1628d057eed61e9525cf9f6ffcbcda34380bc4f02c16a5c4dc21e65432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:75dd19b4ea65fe6544decdadc9448ef2753759105a7222bd95ecc8459bd2a388
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 MB (248871744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af6ee33209153cdfcf3bcc6954d2fc60ae0cda2ac82df49c4eaa358166a24e3e`
-	Default Command: `["clj"]`

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
# Sat, 16 Dec 2023 15:30:35 GMT
ENV CLOJURE_VERSION=1.11.1.1429
# Sat, 16 Dec 2023 15:30:35 GMT
WORKDIR /tmp
# Sat, 16 Dec 2023 15:30:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bf08cfeb007118b7277aa7423734f5d507604b868f7fc44c0f9929ca9cd94ed4 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Sat, 16 Dec 2023 15:30:55 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 16 Dec 2023 15:30:55 GMT
CMD ["clj"]
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
	-	`sha256:240d78ab1c89103db22cdc15ead4a7d23d3e25bea1000d02bb3ff821ec2ce290`  
		Last Modified: Sat, 16 Dec 2023 15:47:09 GMT  
		Size: 74.5 MB (74454850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8bacf45089b093e6f79d1da228a4065a77c30e11cbc61cb5c7f5d61f8e0a7a`  
		Last Modified: Sat, 16 Dec 2023 15:47:01 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:42ea633d03b0cc6e3cb84c791049c3d86c8b675861127dec497b9b9ded5d1c5e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 MB (245349673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77c802c9dd3e52e5e9b696b4187a17e664d33a3528e9c22c6288e3cf17e0153`
-	Default Command: `["clj"]`

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
# Sat, 16 Dec 2023 13:07:44 GMT
ENV CLOJURE_VERSION=1.11.1.1429
# Sat, 16 Dec 2023 13:07:44 GMT
WORKDIR /tmp
# Sat, 16 Dec 2023 13:08:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bf08cfeb007118b7277aa7423734f5d507604b868f7fc44c0f9929ca9cd94ed4 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Sat, 16 Dec 2023 13:08:02 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 16 Dec 2023 13:08:02 GMT
CMD ["clj"]
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
	-	`sha256:3e3b960fe7b4858bb4a84bce119be98887a9f8bc8b8ed5b4260f7c9c2a5ebed0`  
		Last Modified: Sat, 16 Dec 2023 13:18:26 GMT  
		Size: 74.2 MB (74167944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72948823875ceb74ff7b2e3f5565e68bab833e1b7b3b08805bb2ecd58f3bbf74`  
		Last Modified: Sat, 16 Dec 2023 13:18:20 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
