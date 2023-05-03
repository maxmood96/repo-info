## `clojure:temurin-11-tools-deps-1.11.1.1273-bullseye`

```console
$ docker pull clojure@sha256:2e1e4943aeeb4daa51b20364435d48e9b1b6b5ae2652800a0f63f17e86945782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-1.11.1.1273-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:1af30cacf29dc7e761f855c8d5c470393c3941f64f5be5864db573381a87324f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325483453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30d8fc57dc2493566dc3668f2144791370e3f2fa7ca3a34bcc5c49535a41630d`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 12 Apr 2023 00:19:55 GMT
ADD file:f2d012660f882f319a5878a3f9ce285f488b8f90fad49ad238541cf72089e035 in / 
# Wed, 12 Apr 2023 00:19:56 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:10:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Apr 2023 20:03:36 GMT
COPY dir:df592a42a629b9630bdf0ab57a63e6c60f66d91934439985e01efbb58723e9ee in /opt/java/openjdk 
# Wed, 26 Apr 2023 20:03:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Apr 2023 20:07:19 GMT
ENV CLOJURE_VERSION=1.11.1.1273
# Wed, 26 Apr 2023 20:07:19 GMT
WORKDIR /tmp
# Wed, 26 Apr 2023 20:07:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4938afe6c0690d2a6553141857742d94a7350c02b4fa57cd6a9c1b7cbe66492e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 26 Apr 2023 20:07:36 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 26 Apr 2023 20:07:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b0248cf3e63c73d0e496a67807d056ca41d5e968b61087e8eca2cf4b9b4d7b99`  
		Last Modified: Wed, 12 Apr 2023 00:23:20 GMT  
		Size: 55.1 MB (55052736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcef585044f2e536739897cb58b63d90fd8259705b2ea701d530f9eb0462baf4`  
		Last Modified: Wed, 26 Apr 2023 20:20:37 GMT  
		Size: 198.5 MB (198549498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7947d1b73586220eb1832a2797fe0d4e9843fd6cf15dd5ce245004c892e5db14`  
		Last Modified: Wed, 26 Apr 2023 20:22:44 GMT  
		Size: 71.9 MB (71880603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ae5e88300b981c927d81aa878d5b03b6294effe5ac7748940bd51b97885f43`  
		Last Modified: Wed, 26 Apr 2023 20:22:36 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-1.11.1.1273-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c87900e2fbae4571d4cf631fd160e7b7f74313fad1c2048acd6fda753946be8a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.0 MB (321014288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7931f1775829ade53fcc30d4a914628a3913bf0bb8bf27954de8d240972a0e74`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 03 May 2023 00:22:41 GMT
ADD file:f930fdb659332a615b0042ca415d6d7feda9ba6b2f58222e3e5bbed326db4d40 in / 
# Wed, 03 May 2023 00:22:42 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:43:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 03 May 2023 17:46:17 GMT
COPY dir:8d5d0106b2c3fe64c4905be44080473b7828ffb48e0e107739a7ba7a3cb627cf in /opt/java/openjdk 
# Wed, 03 May 2023 17:46:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 17:47:58 GMT
ENV CLOJURE_VERSION=1.11.1.1273
# Wed, 03 May 2023 17:47:58 GMT
WORKDIR /tmp
# Wed, 03 May 2023 17:48:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4938afe6c0690d2a6553141857742d94a7350c02b4fa57cd6a9c1b7cbe66492e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 03 May 2023 17:48:12 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 03 May 2023 17:48:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d677c78be691f8dcbe9d44ce576b97ad205b3dd78557dc62794e59eb19553ee9`  
		Last Modified: Wed, 03 May 2023 00:25:31 GMT  
		Size: 53.7 MB (53692705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f4d5e76f4319fe5a3ea2caf1641913a58d75b0a1015af977eb92876edf0d64e`  
		Last Modified: Wed, 03 May 2023 17:54:48 GMT  
		Size: 195.3 MB (195324181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46dcab43b0e50e50c13c4231a858e0b1d9d304a09f6a31c5eb59a3356ecb3c0c`  
		Last Modified: Wed, 03 May 2023 17:55:43 GMT  
		Size: 72.0 MB (71996787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3188fa36d9f6f49f5c047366d2b4db2d6a0027813134d971bc47f7c12eba1866`  
		Last Modified: Wed, 03 May 2023 17:55:37 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
