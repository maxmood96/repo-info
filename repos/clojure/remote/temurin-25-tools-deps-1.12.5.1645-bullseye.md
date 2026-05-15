## `clojure:temurin-25-tools-deps-1.12.5.1645-bullseye`

```console
$ docker pull clojure@sha256:62e412adf50eb93a7e1c8b9dfd6e0f55c313994d177e88991559a44d19e18f72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-1.12.5.1645-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:f119ecd171db1959e602634e0f6e73f550805b06a39e50cef11406f11346d4a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.9 MB (215940916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f013d2acf90cfd395d23a19d5be39eb0216c6836262c76a75d633ddc41bfee7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 15 May 2026 20:16:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:16:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:16:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:16:02 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:16:02 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:16:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:16:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:16:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:16:14 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:16:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1c662d8f6b122c4f09d6ae1b210df55a5ba6e7b529807c0757ccba0c1ac508e0`  
		Last Modified: Fri, 08 May 2026 18:23:06 GMT  
		Size: 53.8 MB (53763343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb8432142ed7ace244c972b3a446d138c296b3199043980585163e45f59ac93`  
		Last Modified: Fri, 15 May 2026 20:16:36 GMT  
		Size: 92.6 MB (92574564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f59c16961aa57163af2eb377ca5e9e42ffda835335fb11658ad4676f62b35a`  
		Last Modified: Fri, 15 May 2026 20:16:36 GMT  
		Size: 69.6 MB (69601962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baee36a3195c6326d807958516a6c18aaf69236df2995e1729f5a4d79701ab72`  
		Last Modified: Fri, 15 May 2026 20:16:33 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdf2d87e36e421b7fb15b040a4589baa7b0ad52748c5aabee59ee4450b44fd6`  
		Last Modified: Fri, 15 May 2026 20:16:33 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.5.1645-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3c90bde07f94477a1f8e5b40458fe035b9c003e873fbd50211e398ef0ba33848
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7392949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:495d61d2286cbaa3825f69c57241214f13727ab805b33cd3ee9b5b48a8696982`

```dockerfile
```

-	Layers:
	-	`sha256:763bcb76808c558f86b65151cd1c75b60c4f6dea707c079ab92ed058a2e37762`  
		Last Modified: Fri, 15 May 2026 20:16:33 GMT  
		Size: 7.4 MB (7376348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:251f691e013af0e21b24625be7448edb2586c6e55592c77a44774ca6204bc777`  
		Last Modified: Fri, 15 May 2026 20:16:33 GMT  
		Size: 16.6 KB (16601 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.5.1645-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0eca6702f915d72c2f1db81539b3f12eae1b10ec2d66a7836c61994aa91f8fd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.6 MB (213567393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785328270e72b9e2c2a4509b36e5c8e48c1e950a897d7ba354c953a6609f2685`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 15 May 2026 20:16:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:16:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:16:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:16:07 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:16:07 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:16:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:16:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:16:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:16:21 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:16:21 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22001616a192526bf08414bb1d1366b3e86b62d49c3ef52add394d0b82ec1aeb`  
		Last Modified: Fri, 15 May 2026 20:16:43 GMT  
		Size: 91.5 MB (91542254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8adbd6a468f4a961eae3f783daeeaeb1987305b7c5263f49f52963c892218bc3`  
		Last Modified: Fri, 15 May 2026 20:16:43 GMT  
		Size: 69.8 MB (69770887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62714f22e127eac32f0c0dc9ba3fe400e3d84b21537a409fdc94f2d6ad55edfc`  
		Last Modified: Fri, 15 May 2026 20:16:39 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731918f325527119ff4496c91fca91d676e6cfc43cbb45901b1ce3b638cd8eb6`  
		Last Modified: Fri, 15 May 2026 20:16:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.5.1645-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e491bc5c70d991d5a139f83ba4e2a8de174f6a64eeae056360adfc86c193cd92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7398211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c00e8b6dba9bab9d3908bc23480cefe5104a5429096c521b2c717e2432727a55`

```dockerfile
```

-	Layers:
	-	`sha256:56ff190e803334a1d5797ebf0ca03b183e2627f7bed2d1d4819d6c96290de7f7`  
		Last Modified: Fri, 15 May 2026 20:16:40 GMT  
		Size: 7.4 MB (7381468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2807601ac75ceb7b2e8c42ad0dd6f316cac4988abd02258f3fc91875af8e04e`  
		Last Modified: Fri, 15 May 2026 20:16:39 GMT  
		Size: 16.7 KB (16743 bytes)  
		MIME: application/vnd.in-toto+json
