## `clojure:temurin-8-bullseye`

```console
$ docker pull clojure@sha256:afd1d25c85b681c0eb73191599914bdc17b78f9f0e10bfd8d63c3a17a647b259
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:5feee77ec8ce104f5b1b1bf486d86a07491a6ca1de6499fcc89c369ddb0e0d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177865570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82c9fb4d3f78bd665394710ec82acfdae1447b97987416bed5c4e25d8be1ddd0`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1774e4582875ba2932dbcccaa5df9198f7fe57563244475e76804db5509d67`  
		Last Modified: Tue, 03 Jun 2025 05:15:36 GMT  
		Size: 54.7 MB (54716189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a3116a21ebfeae7ed632e765e1ef8d58e9d9c4450b6727047fc746e5d23987`  
		Last Modified: Tue, 03 Jun 2025 05:15:38 GMT  
		Size: 69.4 MB (69398544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5778f503e1fa1747bff5265e9fc4291be8853eec89adeb4be0e2604ee6c019e9`  
		Last Modified: Tue, 03 Jun 2025 05:15:34 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1a3abc7fbae798904637fd068e428234b1c94d42b65516d254f67ac073c9338e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7392033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ac7ae4b001e0d0b9fcbe6dc5f35bc0d7ea9247c8a4917397bac9e258699e78`

```dockerfile
```

-	Layers:
	-	`sha256:2d19aac52a15dd3d0704bce511e7d7aefea5d6d6c2c23492d8c9854b6cd57a1c`  
		Last Modified: Tue, 03 Jun 2025 05:15:34 GMT  
		Size: 7.4 MB (7377796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3b5b515d0dc0e4beac3f4a49cc5985598be512fab429c209e017a2b15fbc365`  
		Last Modified: Tue, 03 Jun 2025 05:15:34 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:edc83e8218d064de18165887991c3658bc93a62a575b593e571e87a4477821be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.6 MB (175609638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e692eeb797ec23abbb8abf6368ffc0351051e49a522a9116ee77e6f9bfba01`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a5f701bfcb264810d9aa404e8040ce22b5b531c7f91508b60b5eea297f126c`  
		Last Modified: Tue, 03 Jun 2025 10:29:12 GMT  
		Size: 53.8 MB (53830516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55e33ec3b2df34155d2280bcb0835aa7b07102ead4c0b6edb8569f673fa8382`  
		Last Modified: Tue, 03 Jun 2025 10:35:33 GMT  
		Size: 69.5 MB (69530723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf876330208db03cd8edf5e78eb5e8835f607b79b49008e4eada6f3e43f190ee`  
		Last Modified: Tue, 03 Jun 2025 10:35:31 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7aec2b9d30a0c6f26a201517e6c81729889499c4ffc7f4632479125533672198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d2e4cb0d641aac92df3027cb7120e58579d26fc836d0720fac9bd2506ba7ea`

```dockerfile
```

-	Layers:
	-	`sha256:11443f32e3bee7ee01a54dd047cb00937784c21bd6f08127b9466dc11c43b09c`  
		Last Modified: Tue, 03 Jun 2025 10:35:32 GMT  
		Size: 7.4 MB (7383593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5ef335abb3b6f5e61ab3b1800c9692365ab55c449dc81cd99b5fc2db978d4f3`  
		Last Modified: Tue, 03 Jun 2025 10:35:31 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json
