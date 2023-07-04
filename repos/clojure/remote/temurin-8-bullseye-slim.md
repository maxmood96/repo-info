## `clojure:temurin-8-bullseye-slim`

```console
$ docker pull clojure@sha256:913da30741bee4b82ac9930f9f79e26a33cb94c4270935a9fba7507068559d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:dfbf854557681ce2aee2ddee9bcc64153e5fd3c97234289fbbfd20c77d0af8be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.6 MB (147556748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d3d97f602345927e7ac375021a4d09f04f8b22be2f9336218a769c11d5a1b1`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:23 GMT
ADD file:4a063d4e089ef10c6806d7042a0040078674ac2db61df02df8bbb8fa4894910a in / 
# Tue, 04 Jul 2023 01:20:23 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:00:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 04:00:25 GMT
COPY dir:715eb4123a1bd94a1f232c902a6f3cdcc4011195a3e566c0f0ddc35dd1e83095 in /opt/java/openjdk 
# Tue, 04 Jul 2023 04:00:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 04:02:32 GMT
ENV CLOJURE_VERSION=1.11.1.1347
# Tue, 04 Jul 2023 04:02:32 GMT
WORKDIR /tmp
# Tue, 04 Jul 2023 04:02:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "d9158bf3a1d92fbf8551656e47a86f42e93d10f1db9defa2124bfee206ce8c8f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 04 Jul 2023 04:02:48 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 04 Jul 2023 04:02:49 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9d21b12d5fab9ab82969054d72411ce627c209257df64b6057016c981e163c30`  
		Last Modified: Tue, 04 Jul 2023 01:25:43 GMT  
		Size: 31.4 MB (31417388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ccffc950a8b498b94fe1759b3349b3af9e7c64526ddf777677aa45c612160b7`  
		Last Modified: Tue, 04 Jul 2023 04:11:59 GMT  
		Size: 54.6 MB (54642103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba38d04011d6443a5115e5f58dc6970df0caa94cfcca969e42f19cba00ab867`  
		Last Modified: Tue, 04 Jul 2023 04:12:56 GMT  
		Size: 61.5 MB (61496642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93f66fe566fbf86a7d426fcd86bcdcc3cdb70ac56185c99d694452271e59737`  
		Last Modified: Tue, 04 Jul 2023 04:12:49 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:81291b87673a035c20328844a6cb3a70c78b67a77d6276f28618e7c687b21369
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.4 MB (145417302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf13628c799edc352d9d09e59de0a0348dc50297ea85db8fc3b3cdc58214cbce`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:33 GMT
ADD file:10af42ddb9f028c5418d370fe2b841aa61e81f37de1ffe76900a783ba3926646 in / 
# Mon, 12 Jun 2023 23:40:33 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:28:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jun 2023 04:51:12 GMT
COPY dir:f6bbe63c81e220d954915791686219263d8c45918fd81b238f7c9f6b21f076f8 in /opt/java/openjdk 
# Tue, 13 Jun 2023 04:51:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jun 2023 04:52:49 GMT
ENV CLOJURE_VERSION=1.11.1.1347
# Tue, 13 Jun 2023 04:52:49 GMT
WORKDIR /tmp
# Tue, 13 Jun 2023 04:53:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "d9158bf3a1d92fbf8551656e47a86f42e93d10f1db9defa2124bfee206ce8c8f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 13 Jun 2023 04:53:04 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 13 Jun 2023 04:53:04 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:92ad4775570054c645678402c8b75eb489b8e05313c9ccd7867bb591266db4d8`  
		Last Modified: Mon, 12 Jun 2023 23:44:45 GMT  
		Size: 30.1 MB (30062834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c42dbe9973fad0e5db82fff74ab48ee24033b2296cd2ca6fdcba69bad893d2`  
		Last Modified: Tue, 13 Jun 2023 05:00:32 GMT  
		Size: 53.7 MB (53742662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83123ae7dbdc6814d261f5910bda01787c980f6179a4aca95b5070b9b9aaba1d`  
		Last Modified: Tue, 13 Jun 2023 05:01:25 GMT  
		Size: 61.6 MB (61611193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9739d6480312a102f7e45f5fc05b678a8c5d32566a33f9ec06b9b5dd0b973240`  
		Last Modified: Tue, 13 Jun 2023 05:01:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
