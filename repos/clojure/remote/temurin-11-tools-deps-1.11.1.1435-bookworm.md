## `clojure:temurin-11-tools-deps-1.11.1.1435-bookworm`

```console
$ docker pull clojure@sha256:e00039828695232039f485d22abbfad824e699783df2e831b7ab684a30808325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-1.11.1.1435-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:0241b7635f96f620e0ec12c2a16643b528086196f33b7757b14979e177182dca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275349191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7504e92efb8f71edf9d939ce073ae23e3ec60032b33f02f85a9d7d0b1ebfecca`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:05 GMT
ADD file:6d9e71f0d3afb0b288cf2c06425795d528a142872692072ab1cd1ad275b67d1f in / 
# Wed, 31 Jan 2024 22:35:06 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:41:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 17:09:55 GMT
COPY dir:b67fa5b31406358a1c40465f439a0fe28f2585d2aa41aff7249c3c30b266c578 in /opt/java/openjdk 
# Fri, 02 Feb 2024 17:09:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 17:15:34 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Fri, 02 Feb 2024 17:15:34 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 17:15:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 02 Feb 2024 17:15:58 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 02 Feb 2024 17:15:58 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6a299ae9cfd996c1149a699d36cdaa76fa332c8e9d66d6678fa9a231d9ead04c`  
		Last Modified: Wed, 31 Jan 2024 22:39:27 GMT  
		Size: 49.6 MB (49583754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93311b9f1dccdb9ed4e27ec9e72dff9468583e68756f160ae709603707528b12`  
		Last Modified: Fri, 02 Feb 2024 17:31:02 GMT  
		Size: 145.3 MB (145271022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eadaea5e05d0920de2c862bec3b6b397473316fefac7f440913a13cd0f03a023`  
		Last Modified: Fri, 02 Feb 2024 17:33:57 GMT  
		Size: 80.5 MB (80493795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4def6e3513af6e8d29ec9d84517893d40d151dcaa91a1a324724c70397ae84b`  
		Last Modified: Fri, 02 Feb 2024 17:33:47 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-1.11.1.1435-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b4cfaf61f906fcba5d18f0652b2afb827cf615d80667b1a4212c42381b5914ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271880975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11f1a120f209a8fc8d5972e28961fa407b6f981d85b740ad4e8afa5a1786f74d`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:15 GMT
ADD file:8bc7f537dd3dc4b92ec9006080fd563cc79205ee1ec3f456d03e869125a5bc21 in / 
# Wed, 31 Jan 2024 22:44:15 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:18:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 08:19:38 GMT
COPY dir:66e2d93ab60a4ef1bb1a1f0fa29608c8835186fbe657955fddda78ed144821fc in /opt/java/openjdk 
# Fri, 02 Feb 2024 08:19:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 08:24:56 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Fri, 02 Feb 2024 08:24:56 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 08:25:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 02 Feb 2024 08:25:18 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 02 Feb 2024 08:25:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:66932e2b787d33a94ee3eb8b489be6e6838b29f5c1d732262da306da9b1f2eed`  
		Last Modified: Wed, 31 Jan 2024 22:47:40 GMT  
		Size: 49.6 MB (49615296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d300b593857f6a07a4266828dbbe1e03ed64d43a6bf503b48194d30675f3a069`  
		Last Modified: Fri, 02 Feb 2024 08:38:08 GMT  
		Size: 142.0 MB (142006417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9605259b1b1c191363b776832cccb2ae691c004db8dfda0192c527070bd627`  
		Last Modified: Fri, 02 Feb 2024 08:40:45 GMT  
		Size: 80.3 MB (80258645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6bb88f82eec00ab6aa9d8166686e47efa7a99c8ff0616519bf4c06713882a63`  
		Last Modified: Fri, 02 Feb 2024 08:40:37 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
