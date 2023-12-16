## `clojure:temurin-11-tools-deps-1.11.1.1429-bookworm`

```console
$ docker pull clojure@sha256:6ba7d536186b9681154685fe9a611d83c5f6636e75abc3a9e69dbb94f72522a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-1.11.1.1429-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:4dcd448f7aff23ed5f2564e19fc10036e2598603d25e5a2d85475acb11f084a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280775833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc5af58fae528b4c0f174c76725ca985d8ec6ef20889ad771038d6dfabeb6bb`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:24 GMT
ADD file:39d17d28c5de0bd629e5b7c8190228e5a445d61d668e189b7523e90e68f78244 in / 
# Tue, 21 Nov 2023 05:21:25 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:07:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 15:24:39 GMT
COPY dir:7cbebf37ba11e5c859b49d766118c0899546d922ac426dfa1230f08ebde784dc in /opt/java/openjdk 
# Sat, 16 Dec 2023 15:24:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 15:30:06 GMT
ENV CLOJURE_VERSION=1.11.1.1429
# Sat, 16 Dec 2023 15:30:06 GMT
WORKDIR /tmp
# Sat, 16 Dec 2023 15:30:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bf08cfeb007118b7277aa7423734f5d507604b868f7fc44c0f9929ca9cd94ed4 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Sat, 16 Dec 2023 15:30:31 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 16 Dec 2023 15:30:32 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:90e5e7d8b87a34877f61c2b86d053db1c4f440b9054cf49573e3be5d6a674a47`  
		Last Modified: Tue, 21 Nov 2023 05:25:34 GMT  
		Size: 49.6 MB (49582225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1a771d9b6c5f4bde297158365f39ffd096a67247a2c15605592e73738745d1`  
		Last Modified: Sat, 16 Dec 2023 15:44:15 GMT  
		Size: 145.3 MB (145266405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e14e1f2c3eb4ce59401c9217ae4f53879b9fe9b7d24d7bf6a154fc1b1e752005`  
		Last Modified: Sat, 16 Dec 2023 15:46:51 GMT  
		Size: 85.9 MB (85926583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164ccc3b862ff5b57b0a2b5d30bea9de61e07b1fafd6c7f8cd4d6801d617c26b`  
		Last Modified: Sat, 16 Dec 2023 15:46:41 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-1.11.1.1429-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:76b9bb96fd67c63a82630dbc1523ebffd6cc55c5ccc34ca7ff48a36827f8b99b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277255081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec0411f0b4dfcf5621d062c95ee8ccc529afd0fa6720d57cac668eec09cebca1`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Nov 2023 06:26:54 GMT
ADD file:6550a7c17e64067114283d098e85f9a74d4707f2879b53c2e4cae99f329c9025 in / 
# Tue, 21 Nov 2023 06:26:55 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:20:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 13:02:26 GMT
COPY dir:679954ac595f0d76b401a9a7d1ae039330e7231cb1c29892d5f56a0e84534783 in /opt/java/openjdk 
# Sat, 16 Dec 2023 13:02:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 13:07:16 GMT
ENV CLOJURE_VERSION=1.11.1.1429
# Sat, 16 Dec 2023 13:07:16 GMT
WORKDIR /tmp
# Sat, 16 Dec 2023 13:07:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bf08cfeb007118b7277aa7423734f5d507604b868f7fc44c0f9929ca9cd94ed4 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Sat, 16 Dec 2023 13:07:39 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 16 Dec 2023 13:07:39 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:df2021ddb7d686bdbb125598b2a6163d63035f080356b3014595f354ea0b40d6`  
		Last Modified: Tue, 21 Nov 2023 06:30:07 GMT  
		Size: 49.6 MB (49612650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:612d125f1849f90f4e047bb3ef55b198f35368f7a1ad3522a435d47de1c8e908`  
		Last Modified: Sat, 16 Dec 2023 13:15:32 GMT  
		Size: 142.0 MB (142001834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d185021f93460e9267020dae744c7769304a9664fd5b1560665406fe03450775`  
		Last Modified: Sat, 16 Dec 2023 13:18:09 GMT  
		Size: 85.6 MB (85639979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a414a68d425e1bab2fe611a51def0d2fa039f012f24b9a1bea4f04464048864`  
		Last Modified: Sat, 16 Dec 2023 13:18:01 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
