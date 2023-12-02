## `clojure:temurin-11-bullseye`

```console
$ docker pull clojure@sha256:e35a445dad8c1ca02ce2e273702071b0326f8ddd9b529151bbc8e9b5f6b5c5ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:303c79c3f7ae0f77d608b04ba2005f182456f28f0e5416a1563d505e4b3c1078
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272226135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a522d9ba0d2b9abb3bdfe45a05d874ee2f90b9b88b92276f98dd7c16ae1266`
-	Default Command: `["clj"]`

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
# Sat, 02 Dec 2023 10:00:21 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Sat, 02 Dec 2023 10:00:21 GMT
WORKDIR /tmp
# Sat, 02 Dec 2023 10:00:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Sat, 02 Dec 2023 10:00:41 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 02 Dec 2023 10:00:41 GMT
CMD ["clj"]
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
	-	`sha256:9accf16316f6ab29e38b002283d8a9d444b332ee440c7b2c9a6bc4b859442e3f`  
		Last Modified: Sat, 02 Dec 2023 10:17:01 GMT  
		Size: 71.9 MB (71901196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4191f43388ea42f638371b8cf3600abe2f58959d32103c173097494c6853110`  
		Last Modified: Sat, 02 Dec 2023 10:16:53 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6d7597640f72ac8db5a8a0a6c44927a733a88c9703d4a6338209e71ec6ae32fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.7 MB (267727083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6900d23e15b7fee428f4ef5b99e1268917a85a52ebc569b04195e618107207a7`
-	Default Command: `["clj"]`

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
# Sat, 02 Dec 2023 08:51:42 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Sat, 02 Dec 2023 08:51:42 GMT
WORKDIR /tmp
# Sat, 02 Dec 2023 08:52:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Sat, 02 Dec 2023 08:52:00 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 02 Dec 2023 08:52:00 GMT
CMD ["clj"]
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
	-	`sha256:59355003b6cdb70af724f365c1efbde64d6b7e144069fb768b9de8a2b4f769fb`  
		Last Modified: Sat, 02 Dec 2023 09:06:43 GMT  
		Size: 72.0 MB (72016805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21a91af43f458958782be8c5cf0ca6bfbd617a66f56a9650ad426630f23f889`  
		Last Modified: Sat, 02 Dec 2023 09:06:37 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
