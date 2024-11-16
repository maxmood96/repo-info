## `clojure:temurin-8-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:eb245e453c7821a14165acd557f4aeb6a43cf1e237abff63b157529b9f518f6f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:eb4089eaf66461c33d1357ed53d77e7a76c8c8949a26c20e2a00b7fd1db6577f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234148301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c46b1efcd5df7be6f8ab9545a2114f9af721e674594f2a72e43d2e0c4fffce4`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f708487934f91eee8af5f0114e3acf7b1ad23b777a0ca9856e785398164a8ef4`  
		Last Modified: Sat, 16 Nov 2024 03:51:34 GMT  
		Size: 103.6 MB (103633964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54da1deebe6102deeeabd8951b189fb5887f5ced61ff854dc4f4a69006935880`  
		Last Modified: Sat, 16 Nov 2024 03:51:33 GMT  
		Size: 80.9 MB (80937999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06442f7add82a8846d4a7167972702288cea40acbb91a71e7fbd531120678cae`  
		Last Modified: Sat, 16 Nov 2024 03:51:32 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ccc3d94d30fd0b9df1d34bfdeb6d533a85ac4b81e08c3e0b85bd6170f333eb20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7318835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a984b2361bc7a060bd641aec2a4363313ec1d6f48828bc7286b479ba9124c4d`

```dockerfile
```

-	Layers:
	-	`sha256:ae0d3e3e4849c6552240dc1c059a12ce3a5b23decbb79c893478802a5ab3a164`  
		Last Modified: Sat, 16 Nov 2024 03:51:32 GMT  
		Size: 7.3 MB (7304593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a468b9190a967c1b8f3dd750c744932eae8df18fcde5b7e908d61bfec2d91cc`  
		Last Modified: Sat, 16 Nov 2024 03:51:32 GMT  
		Size: 14.2 KB (14242 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:75fb6ccbfe3a065eda7137da6650e5adce5153be3940aaa486515896c87539b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233133641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e013a5279b65a78fab0c7002adf32e84a0a3f8ae1bff4aab93dbe90ab45a4c`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27189750e14ce1c29681e47d9469dd8c2a66d939a975563f578cda090c27b4bd`  
		Last Modified: Sat, 16 Nov 2024 05:11:00 GMT  
		Size: 102.7 MB (102747706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a58e9f441e15a322b18f947ad179525da3c4709a5c6acca42801977e9f41c9`  
		Last Modified: Sat, 16 Nov 2024 05:15:45 GMT  
		Size: 80.8 MB (80798090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13cff59b386112042106e9d1ea9130509e182aef89906338cdb316e56964cefa`  
		Last Modified: Sat, 16 Nov 2024 05:15:43 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8600c8be048a99c1e2cc1e28209045213296580e5e8750aca8f567fd635558d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7325420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c891c3482e42785a4b8e6bd340d8a1a8a74ff7073fdb69a3f4357e3839ce41`

```dockerfile
```

-	Layers:
	-	`sha256:4c939eb1e74268750c2b350fb9aaa252b4aec956f196bed4e153a7af9eadf118`  
		Last Modified: Sat, 16 Nov 2024 05:15:43 GMT  
		Size: 7.3 MB (7311060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b57ca8355bf780ae01ceb1050c77a9efdd746b41bfb49408bff61a4152b1a40`  
		Last Modified: Sat, 16 Nov 2024 05:15:43 GMT  
		Size: 14.4 KB (14360 bytes)  
		MIME: application/vnd.in-toto+json
