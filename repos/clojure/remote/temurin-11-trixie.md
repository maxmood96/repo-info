## `clojure:temurin-11-trixie`

```console
$ docker pull clojure@sha256:1ed496ee538a16609d60641d5c1d3cba6be7903f550d5e72aa1e27d564cfb5bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-11-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:29e0d7f1ec6e76f05da3bcf44619fee605cac64fa65071591bfd1005ea52e3c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279793395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88be23444cd343d36ec8c1bd5692a829f95067766968755043b06e60b7a4c1c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 18:42:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:42:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:42:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:42:03 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:42:03 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:42:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:42:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:42:19 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14914803bcda809e133f7cfc129306502739b572cb1ae6be5c77767fac07c06`  
		Last Modified: Sun, 09 Nov 2025 03:26:39 GMT  
		Size: 145.0 MB (144966518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908503eff7ce0292875b37e61b177d64a53d22a222eeac7d3475af55c9c3db3e`  
		Last Modified: Sat, 08 Nov 2025 18:43:28 GMT  
		Size: 85.5 MB (85540604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b286988e5f06c099ab5baa0ee6b7ea5958536176b8a315927df9b181f46d1a`  
		Last Modified: Sat, 08 Nov 2025 18:42:59 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ec6b8dd0d66bc81f44b18741453baa9dbebf9190315b27e69d97dfb7302d94ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7501225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:652cd9a69294a28b775c8d935d23316129d0c8764e5064b4e78b86e48e97f56a`

```dockerfile
```

-	Layers:
	-	`sha256:0fc9cee8f3034197f5f7bcf2b2598d5016d25ec24fdcbedfc33bfd6e00c97ccd`  
		Last Modified: Sat, 08 Nov 2025 22:39:56 GMT  
		Size: 7.5 MB (7487040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:487528876e3746e8df64da4fff359b3d5ea201b89519629d72d5fbc793f4bc44`  
		Last Modified: Sat, 08 Nov 2025 22:39:57 GMT  
		Size: 14.2 KB (14185 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:46d0a9dd9f369cb02801f3755e2a2341e6aa5c2d53d0ad6a7a0fe3cad3bf4162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.7 MB (276746162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1deb4e6df08c343e1e9f8b43bc982b4d5922933f79fc4336117ddf8c32810015`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 18:41:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:41:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:41:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:41:28 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:41:29 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:41:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:41:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:41:47 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1fd68e96726e7e0d5fd03c295247d8534b5f99a6ceccf8c2650812b80ccd83`  
		Last Modified: Sat, 08 Nov 2025 18:42:11 GMT  
		Size: 141.7 MB (141731672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239735e9706c2b1e519d7b12738a1d819272cbc2b446d89913572b07a573bd7c`  
		Last Modified: Sat, 08 Nov 2025 18:42:10 GMT  
		Size: 85.4 MB (85363416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af856ef0fbcff772cd513775b3e3f2f925fda95cbf9233739e74b300725a631`  
		Last Modified: Sat, 08 Nov 2025 18:42:38 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f97fd44c0701f17cfa984fcd58462c0eebce7836725a3379dcaf5181af1f63a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7508990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48431035e712876f05e43b10458d543a2b83f0bd6933266be8ca397f1557d85d`

```dockerfile
```

-	Layers:
	-	`sha256:53eb7383df44f2d17cf13b14aba9ba13d0048ca59817b724ec3263f3ffcf28f8`  
		Last Modified: Sat, 08 Nov 2025 22:40:03 GMT  
		Size: 7.5 MB (7494688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cb67f7ffd2b8fe0d1df301c7df5908947c67167106e62aa18022405cdd51db8`  
		Last Modified: Sat, 08 Nov 2025 22:40:04 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:9b5e9130f0e1309e6658284e42cf1535cb8ce34ba0adb74fc65d155f244c571e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.1 MB (276140624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e2b8ddba60a83b1b1f0f7d78570cdd11d15c75701009d1107b03640a944c1ba`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 19:28:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 19:28:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 19:28:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:28:28 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 19:28:28 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 19:36:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 19:36:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 19:36:37 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3c335bb15935da0eae5ce30111cfa6a289c813162bada9fd389d8ae5510d5d66`  
		Last Modified: Tue, 04 Nov 2025 00:20:22 GMT  
		Size: 53.1 MB (53110127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e8e3e02a4f5bce482ee6878197966e1ab6c51d874ce72ba1d61ebbe633711f`  
		Last Modified: Sat, 08 Nov 2025 19:29:39 GMT  
		Size: 132.1 MB (132079844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1ffd42d12a415e2c9e359d008400ae32ddf72824b7f12df8637cfdaa195810`  
		Last Modified: Sat, 08 Nov 2025 19:37:41 GMT  
		Size: 91.0 MB (90950008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145fe4c69a08adffa317c99a2cd50d85e89ef750a87a78f4e164bd55e8f264b5`  
		Last Modified: Sat, 08 Nov 2025 19:37:25 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e529feff6780aeaf039d1cb92d870998b8b8afa8b8cb0f19d2d2390293cd6d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7505076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5234a9d293e1b95284fd5e5093d8a4320e314caefdabf990e657011dad0bd1ef`

```dockerfile
```

-	Layers:
	-	`sha256:d843b3e8b5c364eaf573e485744e50a581e0f23df1df900c581b8c074b253693`  
		Last Modified: Sat, 08 Nov 2025 22:40:10 GMT  
		Size: 7.5 MB (7490844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b893afc4e1533672ed333784a60ad8f95599f253a074ad67ad5095dadc015d06`  
		Last Modified: Sat, 08 Nov 2025 22:40:10 GMT  
		Size: 14.2 KB (14232 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:87a2c92edd8ee24c3d223974c194603406b5491071c8feaacd9e99de21167eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261555286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e52ff82214dbbb40c91485edc47ae6513418a5a420bde2857138f0f2eba431`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 19:27:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 19:27:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 19:27:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:27:44 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 19:27:44 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 19:34:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 19:34:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 19:34:03 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:48bd359f940d437208e8579c571291503fa327e04a66a6c8d918cfe93cae2e1e`  
		Last Modified: Tue, 04 Nov 2025 00:19:45 GMT  
		Size: 49.4 MB (49352299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13576e2e4394f64e1066c692607d63be0dd492e012c5dd0b09da178823c04b8a`  
		Last Modified: Sat, 08 Nov 2025 19:28:44 GMT  
		Size: 125.7 MB (125694367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b967bdfc9a2b36a5754416240f21cad6cea10f5df58279427e53280c2da5edfd`  
		Last Modified: Sat, 08 Nov 2025 19:34:45 GMT  
		Size: 86.5 MB (86507977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c7d82fbf306cfb86ec5f80a958a1ac857290caf687a9b5f36f4218e66b7723`  
		Last Modified: Sat, 08 Nov 2025 19:34:37 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:be2f53d9a02e3d5d1f5b67cc75668ebe8a1d9379a98c6fd2350de9d3779b21d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7497151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95db5c783639e0fd4ab267bf06b1cbc7f7bbfbdbd859ffaa7fb226dc5e02712d`

```dockerfile
```

-	Layers:
	-	`sha256:1d3043267932b470dd8b923cc9822b072683e5a3ffce1c3d5cd7bfb64442cac4`  
		Last Modified: Sat, 08 Nov 2025 22:40:16 GMT  
		Size: 7.5 MB (7482966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e00162bc0d3c96860fdf086de08d04a33ec19ca877899dfa498653547666033b`  
		Last Modified: Sat, 08 Nov 2025 22:40:17 GMT  
		Size: 14.2 KB (14185 bytes)  
		MIME: application/vnd.in-toto+json
