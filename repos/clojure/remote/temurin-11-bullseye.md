## `clojure:temurin-11-bullseye`

```console
$ docker pull clojure@sha256:467c0f3a9d46aeefe7d83e42f679729b726d2d9cff6accbfa736b1a7340c1e11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `clojure:temurin-11-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:f1b63e827b574ac06f72bab50249930eefae5610b5c7ec266d63dd467fe23d3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269421292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9f6e4c4dd2dbeb650ea06f8f9304aa605b25c78c16da4d25565a9ba5d99fd0`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 01:28:14 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 14 May 2024 01:28:14 GMT
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
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b36057bb4fe1b73e315df52d3becfa479c00dca1fb735459751fb10a1b7c55`  
		Last Modified: Wed, 29 May 2024 19:57:09 GMT  
		Size: 145.5 MB (145504827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf183e8c272679131f5d90146115164f329bd4cc3e1c0fc325552f336c814d3`  
		Last Modified: Wed, 29 May 2024 19:57:05 GMT  
		Size: 68.8 MB (68816417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f39fddff9ba16d1d6c1e6aa64363a6a2d6d80b044efa3e893b15d8f47902de`  
		Last Modified: Wed, 29 May 2024 19:57:05 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:4d27560b2eeafbda02fe4a6455494c464c1546f128423306a9b5a90ae6eee1ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7013567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b567641afc1aca0b31fab6c840c33fe457dcdc6ecedd4ec78f98b72e71d0ae`

```dockerfile
```

-	Layers:
	-	`sha256:3a2525c8332bcd093fc0364412fcd6b4baddbb7fc7586406b5e82d8780c924b7`  
		Last Modified: Wed, 29 May 2024 19:57:05 GMT  
		Size: 7.0 MB (6999752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5216c45c6e9f93b3ce1fbd75ccce72fd97a5aac4d1a22a02772e7d4a2631d44`  
		Last Modified: Wed, 29 May 2024 19:57:05 GMT  
		Size: 13.8 KB (13815 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:da443693358214f65c2c17b808281f6547a5d49532943ba080bca2e8aff71e02
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.2 MB (265181989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45950f7e8f7a13092eaf6917ca1605cbb6f483cb68adce82744ff7955431483`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 00:39:47 GMT
ADD file:43721c605da3f74f0c3f71384780fc0e57e2478b88197672caaf4baa3eddab23 in / 
# Tue, 14 May 2024 00:39:48 GMT
CMD ["bash"]
# Tue, 28 May 2024 19:44:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 19:51:12 GMT
COPY dir:c867ad1ba9e7953ae7814a5cf0e0df40f8d206a8555f8375af9a181bfc9862b9 in /opt/java/openjdk 
# Tue, 28 May 2024 19:51:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 19:53:18 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 19:53:18 GMT
WORKDIR /tmp
# Tue, 28 May 2024 19:53:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 28 May 2024 19:53:33 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 28 May 2024 19:53:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:078d9526cc72763b2db16388f6b511c18a73e3e7f9d229364b3b85a6b5277bc8`  
		Last Modified: Tue, 14 May 2024 00:43:13 GMT  
		Size: 53.7 MB (53738990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41300a45baf921f06ceff01d7f8768386cd63199f648ab8199ea83df7ae9a8b`  
		Last Modified: Tue, 28 May 2024 20:11:45 GMT  
		Size: 142.3 MB (142304355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85216a2e83984b081475c9b5ced5fdb54fcb97098bc7b4ef49d223ebaafe3cb2`  
		Last Modified: Tue, 28 May 2024 20:13:19 GMT  
		Size: 69.1 MB (69138027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1395338197fafdcb839fe7999225aee914b6f3fbc99fb629e41d424f2ea9e1db`  
		Last Modified: Tue, 28 May 2024 20:13:12 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
