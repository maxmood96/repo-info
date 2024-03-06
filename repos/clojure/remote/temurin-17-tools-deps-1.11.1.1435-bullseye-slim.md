## `clojure:temurin-17-tools-deps-1.11.1.1435-bullseye-slim`

```console
$ docker pull clojure@sha256:312f1ea9e163955b806c38675fe4aa524110227acd03c9a076a64ddc660e36ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.1.1435-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1413d90030c3b0f29498fce2478034387025e70044a9e885319197da2319b1ca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234941403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ed1012067ec22cb47639621aabb64b463dc13c9fa007fd624055ecbf3d4d00f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:48:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 14:11:44 GMT
COPY dir:3be96ae7faea81e90455993c99b71c9b45986c7e71f70fc577ab97699c92b508 in /opt/java/openjdk 
# Wed, 06 Mar 2024 14:11:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 14:16:52 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 06 Mar 2024 14:16:53 GMT
WORKDIR /tmp
# Wed, 06 Mar 2024 14:17:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 06 Mar 2024 14:17:10 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 06 Mar 2024 14:17:11 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 06 Mar 2024 14:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 06 Mar 2024 14:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d972ea79502e7e2f800aa3c0a6f461338ca6315edfd2710e566531c30a8da3d1`  
		Last Modified: Wed, 06 Mar 2024 14:29:14 GMT  
		Size: 144.9 MB (144893135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423876815691e8bab13bd17e9ecc52fb8b8ea889c3470fb88d6c519612bda08b`  
		Last Modified: Wed, 06 Mar 2024 14:32:02 GMT  
		Size: 58.6 MB (58624826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936bd0b13448ef4c22a4c7d5b7212afdfb89448bfe60730d54586e2516d5eb15`  
		Last Modified: Wed, 06 Mar 2024 14:31:54 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391e5bee696c2ac9b9a2566763055cdc705ffc0a273283e0734bf2253410d1c5`  
		Last Modified: Wed, 06 Mar 2024 14:31:54 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-1.11.1.1435-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8f1bde366e319c022da070d3d0eb0dd45c3e6d2cf699fdede7febfeb9acf4674
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232543947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d640a1e5cc19324f2c2b6a5c8231c0bde3bd094147e610ddbe304368a8dd1d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:56:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 13:24:27 GMT
COPY dir:4a8c697909e89d854b955537d3c80fbcec33336dd00fb9805f3c0a9edf3861db in /opt/java/openjdk 
# Wed, 06 Mar 2024 13:24:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 13:28:45 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 06 Mar 2024 13:28:45 GMT
WORKDIR /tmp
# Wed, 06 Mar 2024 13:28:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 06 Mar 2024 13:29:00 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 06 Mar 2024 13:29:00 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 06 Mar 2024 13:29:00 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 06 Mar 2024 13:29:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46cf35eb2bf4fc602ed30acd3561a79fab4f053e204653890e517eb9ffbcbb39`  
		Last Modified: Wed, 06 Mar 2024 13:38:51 GMT  
		Size: 143.7 MB (143720928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab79a00dec1d32630c86cbe3f10b52ae575a400f02bff6817c8c291d01d1e97`  
		Last Modified: Wed, 06 Mar 2024 13:41:21 GMT  
		Size: 58.8 MB (58750925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22312ef3a59e7860dc48a34803da12e438115de58df708480fab14e0ff731e4`  
		Last Modified: Wed, 06 Mar 2024 13:41:16 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ee0c13fed94cdaad65f2c6477abbca85b758943a361b9973fe5a7833c92b5a`  
		Last Modified: Wed, 06 Mar 2024 13:41:15 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
