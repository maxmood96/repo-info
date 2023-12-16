## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:81d7a825f36940aaab0025d2f99391f233d47ae8234a691aa0121f5f0581c339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:53ac6d10358763bba88006f5d2d504e4dd8c66a96333f27300538726a2140d0e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.4 MB (272421513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f3d8cf0286e45e0b656c78caffcfa6b458188b8d0818bb871fe76ab68e14bc`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:46 GMT
ADD file:71543995e4d314b0c86da5ddf8e0cb74649767d30b3e5b6261360de354f0567b in / 
# Tue, 21 Nov 2023 05:21:46 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 15:25:48 GMT
COPY dir:7cbebf37ba11e5c859b49d766118c0899546d922ac426dfa1230f08ebde784dc in /opt/java/openjdk 
# Sat, 16 Dec 2023 15:25:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 15:30:59 GMT
ENV CLOJURE_VERSION=1.11.1.1429
# Sat, 16 Dec 2023 15:30:59 GMT
WORKDIR /tmp
# Sat, 16 Dec 2023 15:31:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bf08cfeb007118b7277aa7423734f5d507604b868f7fc44c0f9929ca9cd94ed4 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Sat, 16 Dec 2023 15:31:18 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 16 Dec 2023 15:31:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d1da99c2f14827498c4a9bb3623ae909b44564bdabad1802f064169069df81fb`  
		Last Modified: Tue, 21 Nov 2023 05:26:17 GMT  
		Size: 55.1 MB (55057903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9702745df0f994c9330f46f592ee18df8d4a2d46378b8cf5cd6e1abd161c0e0`  
		Last Modified: Sat, 16 Dec 2023 15:44:54 GMT  
		Size: 145.3 MB (145266339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1220d5ccf94ca7d2d09a7242544e74a8cb66697ee4455f4c45b37d435593719`  
		Last Modified: Sat, 16 Dec 2023 15:47:27 GMT  
		Size: 72.1 MB (72096652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98565c3bf3757829f9b90c568ee09c002fa4963fd3f976218dd6b9616e9893b1`  
		Last Modified: Sat, 16 Dec 2023 15:47:19 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d8f8598a5caa7ca698029c45b47b191d86954a49efefc86587fcab59b6b5b913
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.9 MB (267925898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3649b20dab06e2834415cb3876d9dcd66dc11cc1ee123eadb191c1647a902f3`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:13 GMT
ADD file:614987b9855939825ad2383e7bacbf14ea208d74906982bba3a67126702c8371 in / 
# Tue, 21 Nov 2023 06:27:13 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 13:03:25 GMT
COPY dir:679954ac595f0d76b401a9a7d1ae039330e7231cb1c29892d5f56a0e84534783 in /opt/java/openjdk 
# Sat, 16 Dec 2023 13:03:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 13:08:04 GMT
ENV CLOJURE_VERSION=1.11.1.1429
# Sat, 16 Dec 2023 13:08:04 GMT
WORKDIR /tmp
# Sat, 16 Dec 2023 13:08:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bf08cfeb007118b7277aa7423734f5d507604b868f7fc44c0f9929ca9cd94ed4 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Sat, 16 Dec 2023 13:08:22 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 16 Dec 2023 13:08:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:bbf382c14c7b19b81c612f639e09e6a7b04eccd4481d0abac48b8ace9faae3b3`  
		Last Modified: Tue, 21 Nov 2023 06:30:47 GMT  
		Size: 53.7 MB (53707872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af54c8e663dc85f64ce40fefa66d7c03c32ea39f2b5b91b849f62df8782494b`  
		Last Modified: Sat, 16 Dec 2023 13:16:08 GMT  
		Size: 142.0 MB (142001837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a2473b6dc45e93d6b5500fa93057fb4a9835024d97614983b965570b0b405d`  
		Last Modified: Sat, 16 Dec 2023 13:18:44 GMT  
		Size: 72.2 MB (72215569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8c2f9ec187d87b2f1156044124ab49796b254a34d083122e318989ff11d2c3`  
		Last Modified: Sat, 16 Dec 2023 13:18:37 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
