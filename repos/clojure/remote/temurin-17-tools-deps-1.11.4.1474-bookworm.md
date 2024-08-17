## `clojure:temurin-17-tools-deps-1.11.4.1474-bookworm`

```console
$ docker pull clojure@sha256:9b970df4aef77d005dd8d2474bdaaecb3a7446160c272c0103b16ec5a015ea65
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.11.4.1474-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:7571685914bd6dff5b2c6ea4de59f5a578a1eb586a8489a83c0e3889f6ccd85b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.2 MB (275174011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7f20e7e39a9cf01587e37c401ec713817ac836cc38a08b4d3a2099a4ab5a87`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cca736b79d1a678667526d9959899a651db629fd809819a6e6659367558a7f7`  
		Last Modified: Sat, 17 Aug 2024 01:59:55 GMT  
		Size: 145.2 MB (145164842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff10a60b1b1e6f6a9f39120d59c159142c5d8733c7803bd7d774416fb7f9c9c`  
		Last Modified: Sat, 17 Aug 2024 01:59:54 GMT  
		Size: 80.5 MB (80454047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3edc6a816ccc580ce33f726dc3a4ed099aac959605dc1bf59fe4559c407560`  
		Last Modified: Sat, 17 Aug 2024 01:59:51 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94d16ff5e046317604c08f048c7e6a583374cbda6fadddf825a9bf0d6a7794a`  
		Last Modified: Sat, 17 Aug 2024 01:59:51 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.11.4.1474-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9e4ef986d7afd5da21b2b21568a47eec54fe0a66427fdbaedb28e3c0e08f9a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7015525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9688d5f847cef0057de39bdb4d84f2fed086c83b3021f3865daf0e9c5a9ec5ff`

```dockerfile
```

-	Layers:
	-	`sha256:63b793986e95e8308db549bdb6d35e334648927f1c6031fe408cf5dfc3b12239`  
		Last Modified: Sat, 17 Aug 2024 01:59:52 GMT  
		Size: 7.0 MB (7000086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d06daf8fbceda7ecb9c95488356ed060b6e9125c3607440b7c0ccec92421f8b6`  
		Last Modified: Sat, 17 Aug 2024 01:59:51 GMT  
		Size: 15.4 KB (15439 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.11.4.1474-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fee346ed2ad44f33434ac77704bd97c9bf4b950a6794e1ec951ab6ec7b5490d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.7 MB (273747567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da50f4896ccd5245e8ccf7bd41060cd40ae15aebb5f01fd7f25d7313fdc7bc73`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6465967d1033737f70c62068d5cd9ed1c2542e4efe62e3f0cf90698130c0951d`  
		Last Modified: Tue, 13 Aug 2024 06:30:32 GMT  
		Size: 144.0 MB (143959507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edad346054246e7687e9fcd4ad5da296ff7e6da48447d37afb361f98b3b2b2f8`  
		Last Modified: Tue, 13 Aug 2024 06:34:41 GMT  
		Size: 80.2 MB (80198429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a9d079dfe22dcd3f3102e8c1fa033d3cfcf8721c2e2b4c38fdf90506ab1626`  
		Last Modified: Tue, 13 Aug 2024 06:34:39 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6473f62f558ef1b2c75b1271830eb342ead842370281476fe26451dbc56a210d`  
		Last Modified: Tue, 13 Aug 2024 06:34:39 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.11.4.1474-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:340cb0872415cf052d27f6cdbc5aaa017d7d7cf48ff9a9671c5d369c689ef982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7022449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196685ef2f177e8161f4f855bcb5cd2a8cd0211ab0974ab85137f87133a9d869`

```dockerfile
```

-	Layers:
	-	`sha256:98591ceb334ed8078a71342dedff64bb6256010d18748d77e886bf1c3da62db9`  
		Last Modified: Tue, 13 Aug 2024 06:34:39 GMT  
		Size: 7.0 MB (7006473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:481f7a0d7707ad1f09c365c1a5e3639130ea124c9cab2ce178c07f2d68fdd15c`  
		Last Modified: Tue, 13 Aug 2024 06:34:39 GMT  
		Size: 16.0 KB (15976 bytes)  
		MIME: application/vnd.in-toto+json
