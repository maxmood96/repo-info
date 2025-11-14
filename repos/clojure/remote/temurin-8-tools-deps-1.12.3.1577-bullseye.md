## `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye`

```console
$ docker pull clojure@sha256:9d8498764531ba98979ff5db4b64cfee1561dc0257d1c5014f58fae1be9e37e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:26898cb466ad9108cc9c44f8602e1f62d011b5611f34578fd4920b1d904267d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.1 MB (178051829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a785e85f6787d4c972892f7f4decf51a61314a6fbb72a8a5a8e8d697c3869db`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Fri, 14 Nov 2025 00:49:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:49:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:49:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:49:53 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:49:53 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:50:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:50:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:50:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b4e2e04e62e990bbd4081568b379c097b49a6f4aac5584d9160a47e0df7ba6`  
		Last Modified: Fri, 14 Nov 2025 00:50:37 GMT  
		Size: 54.7 MB (54733362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3298304f169d612593ce03765f403cf4c7148d43b01a2b14bd150028398dae2e`  
		Last Modified: Fri, 14 Nov 2025 00:50:42 GMT  
		Size: 69.6 MB (69561126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d95b5e094b5cb0304aca133de6d2aa3229647db301a67471d09f68e52f79b2f`  
		Last Modified: Fri, 14 Nov 2025 00:50:32 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:976494e7d973171233b5dbe9b3588c0e2ed43c667ab4220825d57ee91ec6dedf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7531471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a66009d4f6d37ab7d8d1729ded8b737eae26839cfce72516f6f0ad3efdb8b63c`

```dockerfile
```

-	Layers:
	-	`sha256:3e29063e94a891068704982a19e412c8a7482fc1d89eb8ae4a4a8903caac7f7d`  
		Last Modified: Fri, 14 Nov 2025 01:49:23 GMT  
		Size: 7.5 MB (7517277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30223eb340241904b35c9b5a05d5a8e615f8e0f7da880216899e554f56b85816`  
		Last Modified: Fri, 14 Nov 2025 01:49:24 GMT  
		Size: 14.2 KB (14194 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d83a3cd6ea2fb187528253d2428404038e820e5bdf8719db56c20b1415f453cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.8 MB (175762239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aacb0f11f32b8ad8949cbb2924e39f7d97c1f803516837a6f84e187afbf9e40`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Fri, 14 Nov 2025 00:50:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:50:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:50:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:50:45 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:50:45 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:51:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:51:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:51:58 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763a439751c897c3dbcd6588ff81986d9c801802573c58d32d8e8051c119554d`  
		Last Modified: Fri, 14 Nov 2025 00:51:39 GMT  
		Size: 53.8 MB (53814998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69bb2fe81ed5e399920067fff2536fc51dab344f024d41518002a8669c1372d`  
		Last Modified: Fri, 14 Nov 2025 00:52:29 GMT  
		Size: 69.7 MB (69688625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8435c90bde46290ea8deb6144ef8b1f07fff5159bcaf511b0bbaa3ac3812f8`  
		Last Modified: Fri, 14 Nov 2025 00:52:21 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f8a636cb19185b94fa50cc7a91ee647c0fbdf58c4c973895a21b58fc465cf726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7536586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eb5fff64509e258103af6e3e045f954982557a052b1fa6b5dea65959e19ab27`

```dockerfile
```

-	Layers:
	-	`sha256:02b37d819a500f2fb2fe26775557502707dc08bed61ddcb6a08b48f2e436d2b5`  
		Last Modified: Fri, 14 Nov 2025 01:49:31 GMT  
		Size: 7.5 MB (7523074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7ca3e738bed8af5376bd9cd0161ffbb162cde3219cbd10f5ad495aa7c606edf`  
		Last Modified: Fri, 14 Nov 2025 01:49:32 GMT  
		Size: 13.5 KB (13512 bytes)  
		MIME: application/vnd.in-toto+json
