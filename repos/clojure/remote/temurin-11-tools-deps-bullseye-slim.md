## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:e7015075d1e75338e6e7d3d9ca300e6141fb4c74c74e2e1ddd58256d4b5cc316
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:667d05f198e0bf1842f9059d990307e42a484af20829db6b8c63a3f7c717b1cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235359570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f268536191125462f8ac35bb75be00f6b73f7954cbc3059f5413359cf4c37a1c`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a35acecdf60bf898a7380a506b15f5e19be888f621c7dbd54348155e3935e00`  
		Last Modified: Wed, 29 May 2024 19:57:08 GMT  
		Size: 145.5 MB (145504874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f7ff7f379b4c794515e1050b17572b4f329b130505bb4ff356f630dd5f7ad3`  
		Last Modified: Wed, 29 May 2024 19:57:07 GMT  
		Size: 58.4 MB (58420116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46705aa55305f5a195e51b3558200105aa38c685a79443d5644c8ed18bac5f66`  
		Last Modified: Wed, 29 May 2024 19:57:05 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:81fbe61d5b5de3b9d215959940b5ed55d52f20cc952e5b5e816c39ded63a81de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4923122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:289b327081815716c82db5e8b36c208d89f679daba16db6b1aef8fdedc71a9e4`

```dockerfile
```

-	Layers:
	-	`sha256:7d503ca1c6fc1db7aed18ecf872d0218f10683630fbb712274f6bb90d83ca6ee`  
		Last Modified: Wed, 29 May 2024 19:57:06 GMT  
		Size: 4.9 MB (4909234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc24242327c56b0629e73e49a585b436db502f4f9abc1c0abb32fe25be6c2618`  
		Last Modified: Wed, 29 May 2024 19:57:06 GMT  
		Size: 13.9 KB (13888 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6660961f8f5df5f081e3ba5c416755775c008b57374d8b3f6b76764580b6268d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231140313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f79f063970b1b42cae8d54b05391bcee4380df05eda2dff29c5c826ae0dd818`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Tue, 28 May 2024 19:45:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 19:51:36 GMT
COPY dir:c867ad1ba9e7953ae7814a5cf0e0df40f8d206a8555f8375af9a181bfc9862b9 in /opt/java/openjdk 
# Tue, 28 May 2024 19:51:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 19:53:38 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 19:53:38 GMT
WORKDIR /tmp
# Tue, 28 May 2024 19:53:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 28 May 2024 19:53:52 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 28 May 2024 19:53:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24bd4bc2937004ae10f68cfc8b2d5998c24a900c7e5433a0bf9a1e459e3c329e`  
		Last Modified: Tue, 28 May 2024 20:12:03 GMT  
		Size: 142.3 MB (142304374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4f07cc54fe0b981ae699ae5f770f7c975b40427efd8bd415d5d6f684d8183c`  
		Last Modified: Tue, 28 May 2024 20:13:37 GMT  
		Size: 58.7 MB (58748414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420c78316c1a4e89024d74200141ef8ef8f0153d55d9cf23a8cf90014ce8df5f`  
		Last Modified: Tue, 28 May 2024 20:13:30 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
