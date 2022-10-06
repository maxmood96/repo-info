## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:544b0609432bc82f53cd303e2f9df17be599f20c1e2fd2491d0a7ca09c13d0de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b80f7d13080a9febd8bf0a9e6a5fc763019283efe1da4d0491439c1521955c81
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291015911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9211e55a7dcb84ab79bd5b5c42bc62f77936d650adaff6c1bbdea0484a4448ca`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 03:51:16 GMT
COPY dir:e3c63d67b32fccda756dd62000a0cf47da966d18fe6f1f25cd1f37b60881f0ec in /opt/java/openjdk 
# Thu, 06 Oct 2022 03:51:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 03:54:55 GMT
ENV CLOJURE_VERSION=1.11.1.1165
# Thu, 06 Oct 2022 03:54:55 GMT
WORKDIR /tmp
# Thu, 06 Oct 2022 03:55:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "72d662bdc99b79037f9e34996272384de35e01e0416d8eb79cc940ee0f0fc808 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 06 Oct 2022 03:55:14 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 06 Oct 2022 03:55:14 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0411b6cb0e944ff13c8e89f4a886c731ea8293c8f3dbc5d78ed1df2e6fbef5b9`  
		Last Modified: Thu, 06 Oct 2022 04:08:54 GMT  
		Size: 198.1 MB (198124981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55053f5e4a98a242ad23f218c523e143d420546cb34b18d1df7be09bced1c57d`  
		Last Modified: Thu, 06 Oct 2022 04:10:54 GMT  
		Size: 61.5 MB (61470210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe6b7e5fd8d25031eea15bc3b4f3dadf2971a0569fbc4b71f5fc6d87c8e81b2`  
		Last Modified: Thu, 06 Oct 2022 04:10:46 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bbd97bae6eb3e2eb76ba245577098d51e06af6774fa10db03ea8cd05fda351f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286324515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb533a124bf0c29835a9444fb426836fdb18706df9fdbca17d2009fe33126411`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 02:32:30 GMT
COPY dir:0dc06d70d42a32ae203bdf41d3806f1204b90ca101c4efe4662ba862f2c76b8a in /opt/java/openjdk 
# Thu, 06 Oct 2022 02:32:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 02:37:06 GMT
ENV CLOJURE_VERSION=1.11.1.1165
# Thu, 06 Oct 2022 02:37:07 GMT
WORKDIR /tmp
# Thu, 06 Oct 2022 02:37:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "72d662bdc99b79037f9e34996272384de35e01e0416d8eb79cc940ee0f0fc808 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 06 Oct 2022 02:37:25 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 06 Oct 2022 02:37:25 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3bfdcb0b9c92e9c3da0e6ca913cb8d3cf77c13d55a20c234730a5896afdec4a`  
		Last Modified: Thu, 06 Oct 2022 02:57:34 GMT  
		Size: 194.9 MB (194866592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b815daa03c5050288716d4667c31867d57afb01519e122ca5200690d0fd22b8`  
		Last Modified: Thu, 06 Oct 2022 02:59:47 GMT  
		Size: 61.4 MB (61392911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e756d54c421b202f3a849e3f57d77174512b53b137b6a7e98b70b648a13a746`  
		Last Modified: Thu, 06 Oct 2022 02:59:39 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
