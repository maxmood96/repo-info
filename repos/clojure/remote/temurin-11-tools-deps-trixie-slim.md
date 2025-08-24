## `clojure:temurin-11-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:8e6124abbec7691af604f828ec9da4b441464a72d7e63b0af075c39ada675eeb
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

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d75c0b6b6bec19d69317b2c722f287c1d34fab1d74a114aa97464ad6c3c7289a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.3 MB (247321246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57fed01cb94394f1e63f95d4684f8bac68af1dae9240675c81d43818f18071d2`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8592d9a295950b81d74b83080a0a10100277f4acb2d1a2c3a1e55573fd561661`  
		Last Modified: Tue, 19 Aug 2025 03:59:46 GMT  
		Size: 145.7 MB (145658140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d53740457621df30b79f9a189cfc3937c95917b2ad013251502fac0b93b9132`  
		Last Modified: Mon, 18 Aug 2025 16:53:19 GMT  
		Size: 71.9 MB (71889175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97b1e6a4bea4ef19c8a243e8e6e45553434e1f98dd27684b9559eae3cab1c4c`  
		Last Modified: Mon, 18 Aug 2025 16:53:01 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3ab5792490d408c9817fdd648dd26c265874d8216a406df3dbadf210e5c97127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f0f2e3cac3c6ebd3c226461edf196e65e82b1fe136c17c31ca16d9cc1a163b`

```dockerfile
```

-	Layers:
	-	`sha256:f910cbdabfbbe0558b8588ea4828b1f2b5024a7c4f333a51ab64f990fc81e2ee`  
		Last Modified: Mon, 18 Aug 2025 18:36:45 GMT  
		Size: 5.3 MB (5275378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c0da89d99ccc040a30bd6ff8f05c4f8974f8cf571719272b0b938cb6a8e3e2f`  
		Last Modified: Mon, 18 Aug 2025 18:36:46 GMT  
		Size: 14.3 KB (14286 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ee2eae30c5ffbeb1c024cef8ced3fcef94a5d53a0e9cc627616a046ef0851eec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.3 MB (244304032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d49912f1dec821a5333c03286f2475bbd48e0f3f1a74213e130dfcc84959f84`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d575fc3fc33f3212c68f0b4bce5426cd5a68295ab95b0f84cdc65794583043dc`  
		Last Modified: Tue, 19 Aug 2025 04:00:33 GMT  
		Size: 142.5 MB (142460557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b92c5e0632b1cdb30d00afac945beeed0fb6f9d8a3fef93dc6d69b967160d9`  
		Last Modified: Mon, 18 Aug 2025 17:05:51 GMT  
		Size: 71.7 MB (71706785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b92c80a993b2456929b36084cb61fc10320ac4ed22a3026df8298f8d13d4a64`  
		Last Modified: Mon, 18 Aug 2025 17:05:41 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ec866795334af1848e607d471dd72633221646832ef45534a48a3adc8a229de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5296169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e93827a926f709d6e658053cf1842b2afa3c58e397a850c88ffff401b4d987`

```dockerfile
```

-	Layers:
	-	`sha256:0def30ea31a34322919c0dd6a6d2360197e235d71dfc11779b091b8e4b4f00e4`  
		Last Modified: Mon, 18 Aug 2025 18:36:51 GMT  
		Size: 5.3 MB (5281765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f42598ab97190ad4503a114e4f3bde003308f4bb421090ef78aafb3a2d8d2674`  
		Last Modified: Mon, 18 Aug 2025 18:36:52 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:08e0e37e4430c0a6de30d3fc5d3e1e2ada9ba0367a94de64a348f242594f483f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243736679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8160ea3a09eada237c6d8ee8d754b3737098d7190c706a51c3904bc2dd31586c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d40da39c1e05974afe8d7dc7c9ee044827e979d78538852469cea98a61ef8ff`  
		Last Modified: Sun, 24 Aug 2025 06:19:53 GMT  
		Size: 132.9 MB (132853302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9e3effd08229d05747c4f7246b1b5d5e169466fe116a4526d0b7cfa2d9ba3a`  
		Last Modified: Sun, 24 Aug 2025 06:19:53 GMT  
		Size: 77.3 MB (77288517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed12ddad8bfb6ccf57156155039393e36b889f025bc183abfca46e86ffd78b1`  
		Last Modified: Mon, 18 Aug 2025 17:20:35 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cc0378bc1c95bac491ca370b3edc984dc0f8618ffb45bc6471d59f986ead5be0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5293468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7199809fadf1c846f5230a1b6e937162ffb99c44e02c535063ad18158f3f1755`

```dockerfile
```

-	Layers:
	-	`sha256:4a29df063b79fd0f7d11f6d470bfe860ec97460ce8ea5326c0893b2b4779271d`  
		Last Modified: Mon, 18 Aug 2025 18:36:58 GMT  
		Size: 5.3 MB (5279134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c9c0f315509c3886388f2591ddf8ea0726def0c7f30173bb24f89c5108db266`  
		Last Modified: Mon, 18 Aug 2025 18:37:00 GMT  
		Size: 14.3 KB (14334 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:03cc1148f6f3cb5bfdee31c29f4bc02360fae1a4135f55e6ae24d74d25da962b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228306729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fed089c0aebf637ae99cf0f74c8cd85fc9f7bac64617484a1179087368dd83f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1941fd0e14005c4b3a4ceb8cc960f8885714e1070af13e09c47c856d2a283b`  
		Last Modified: Sun, 24 Aug 2025 06:20:46 GMT  
		Size: 125.6 MB (125622148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a7a634bafe9ee54ae717e2acfe7704e68f475fe430fc272be7a6d1993132a3`  
		Last Modified: Sun, 24 Aug 2025 06:20:41 GMT  
		Size: 72.9 MB (72850877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d32fe9ed729f967bb544899359e477a73274a2391c60ca94a81caa932f222e0`  
		Last Modified: Mon, 18 Aug 2025 17:44:29 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2b93c2422abb51551b31564001c89a2d39f99e4a7771b9d47f6ec2261b55ebf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5285592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01e3af47e74d1d12a222f7f442a39fd64d8c5db6a35f30855e2c3ba7a49ca01e`

```dockerfile
```

-	Layers:
	-	`sha256:5a7afae068f06df09b83ad18d947ce7ba590de0b81124f5bbc24b2613da6d077`  
		Last Modified: Mon, 18 Aug 2025 18:37:05 GMT  
		Size: 5.3 MB (5271306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:567d3af9414453979e26c9cb56d7d10479bcd542b076cbc901eba69230c04476`  
		Last Modified: Mon, 18 Aug 2025 18:37:05 GMT  
		Size: 14.3 KB (14286 bytes)  
		MIME: application/vnd.in-toto+json
