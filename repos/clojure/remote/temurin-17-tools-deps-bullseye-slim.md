## `clojure:temurin-17-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:faba8a1aedca7c98bed31dc237925b8ca774d4655f0fc1de00092dae6292edf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b24bce46e05d935e4970f6504f36ae0f2f74c61a43612a7223dfeb09fd39996d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234940787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fef81ad9f8bf8df85a04209db92c6cac2da11edb5e71b9af1b6633bd28f40e3f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:48:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 05:23:02 GMT
COPY dir:6673b976fb9ccd391df2de00f5738789bfa84c9bc068b98b869cb1d7436fd333 in /opt/java/openjdk 
# Fri, 16 Feb 2024 05:23:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 05:27:23 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Fri, 16 Feb 2024 05:27:24 GMT
WORKDIR /tmp
# Fri, 16 Feb 2024 05:27:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 16 Feb 2024 05:27:42 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 16 Feb 2024 05:27:42 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 16 Feb 2024 05:27:42 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Feb 2024 05:27:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f0fc78b66d4b42be2ff0a23e21d3d64cf400961852ccf277b2f8c893c9409d`  
		Last Modified: Fri, 16 Feb 2024 05:37:27 GMT  
		Size: 144.9 MB (144892535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5081c987277e373500e6b546d3aad96eef22a6ca8c8495cf0edafb2b250cac0`  
		Last Modified: Fri, 16 Feb 2024 05:39:50 GMT  
		Size: 58.6 MB (58624808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a9f33b214b0a815b9646c395291bd6bdd01a4b9e65de6c2862c43ca5a3470cf`  
		Last Modified: Fri, 16 Feb 2024 05:39:42 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656c0ccb96f0d809a5739b7c1700261f25e12a576272d761d93f10693c5f60ee`  
		Last Modified: Fri, 16 Feb 2024 05:39:42 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e7b5ebd4a46861a6b79e65eb1b3c0b2240f31cc411eeb5403270ee134148e56e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232543960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6f8bd6a23956e04f43ac056c0ea774c6c8fe15d02a566e742627e9030b9f24f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:56:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 02:06:04 GMT
COPY dir:1e33e1b9b4d5ff1fcafcf70a5b147d046ddd08f2a0ffd21b97536e3a6e636c5f in /opt/java/openjdk 
# Tue, 13 Feb 2024 02:06:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 02:08:54 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Tue, 13 Feb 2024 02:08:54 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 02:09:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 13 Feb 2024 02:09:08 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 13 Feb 2024 02:09:08 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 13 Feb 2024 02:09:08 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Feb 2024 02:09:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74289f9f740a9505d946ab19759485775a376db053cd1cbdb734c25d84eb93a9`  
		Last Modified: Tue, 13 Feb 2024 02:21:29 GMT  
		Size: 143.7 MB (143720893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375adcf3717df7baa35fc412a44a1e2e8221c4f02a119d1baf05d637b0f7cb34`  
		Last Modified: Tue, 13 Feb 2024 02:23:30 GMT  
		Size: 58.8 MB (58750974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f3831c6d0ea718a2bf458bf19fc6cc2f68f2852b4027d264a5b51e0b36c08a`  
		Last Modified: Tue, 13 Feb 2024 02:23:23 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2dbc4997f68f44e703d2b7cb6d0d85c245f17283cba9d1da7da977a0525661`  
		Last Modified: Tue, 13 Feb 2024 02:23:23 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
