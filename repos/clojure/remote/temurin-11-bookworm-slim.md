## `clojure:temurin-11-bookworm-slim`

```console
$ docker pull clojure@sha256:bae0a81fe52915521f9a44ba4866472b4f20c55bba2d1b7fc108e9cb11b99950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b1f3d28bfba507034ca60e8a56a446dd6d2824db2a95afc3fa33a3e82b566313
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243487272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8647c530aafca88bb846f0f523f719c75b0fe18ada8908ab819a4f010e291da7`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:18 GMT
ADD file:af0f4e41d68b67ca88a1ce6297326159e18e27670d7bfc0bf5804a4e2b268cc8 in / 
# Wed, 31 Jan 2024 22:35:18 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:43:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 17:10:34 GMT
COPY dir:b67fa5b31406358a1c40465f439a0fe28f2585d2aa41aff7249c3c30b266c578 in /opt/java/openjdk 
# Fri, 02 Feb 2024 17:10:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 17:16:03 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Fri, 02 Feb 2024 17:16:03 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 17:16:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 02 Feb 2024 17:16:22 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 02 Feb 2024 17:16:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c57ee5000d61345aa3ee6684794a8110328e2274d9a5ae7855969d1a26394463`  
		Last Modified: Wed, 31 Jan 2024 22:39:55 GMT  
		Size: 29.2 MB (29150465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:575fad5380f55c159ccfbe24fb0dca8cc435788398d5e90f186fbe5108ff4842`  
		Last Modified: Fri, 02 Feb 2024 17:31:23 GMT  
		Size: 145.3 MB (145271007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a495328b4b986854fd0f71d3481bc08fb4362284abeebf22d5dfe5b0625d684`  
		Last Modified: Fri, 02 Feb 2024 17:34:18 GMT  
		Size: 69.1 MB (69065182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a67f0bf98127ae59795fd2f1910ac3ad0436658b731d180364c1b8b20d9a71a`  
		Last Modified: Fri, 02 Feb 2024 17:34:09 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3becd02f804eb0ad3ebff9214757895c671ed68bd83093cfd4d109c0dd2dfecb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.0 MB (240007541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1440bdf1fcab32beca1a2e2aabffefec5167ce9ce12d56c2e39449ab9b9d71c6`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:26 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
# Wed, 31 Jan 2024 22:44:27 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:20:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 08:20:17 GMT
COPY dir:66e2d93ab60a4ef1bb1a1f0fa29608c8835186fbe657955fddda78ed144821fc in /opt/java/openjdk 
# Fri, 02 Feb 2024 08:20:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 08:25:24 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Fri, 02 Feb 2024 08:25:24 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 08:25:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 02 Feb 2024 08:25:40 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 02 Feb 2024 08:25:40 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00498bb373c7ab039d3c50e9ee01de46ff61000a6e4866749566b453c520b9fc`  
		Last Modified: Fri, 02 Feb 2024 08:38:25 GMT  
		Size: 142.0 MB (142006400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8184a1a450db549e763590e1e04b27b8ede54170e1167229a31143004bd6b289`  
		Last Modified: Fri, 02 Feb 2024 08:41:02 GMT  
		Size: 68.8 MB (68819690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7fc9d43e32b7728ea27693c5c9fee2fcefd335001bf83c0df166cd09d75a1a`  
		Last Modified: Fri, 02 Feb 2024 08:40:55 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
