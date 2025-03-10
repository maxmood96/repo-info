## `clojure:temurin-11-bookworm-slim`

```console
$ docker pull clojure@sha256:f5ee1093f3f8b4f78d514d3bbfae1ff79b0469bcb7d7e72db926572c4c4c21b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0742d4a230b28f2f680c07dff7bfd1a699d6428107518edc930486f16c7d25ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243346675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2044cf35effc009b06a5e352a682c00855ca76218ddccc4e241d6076cdbb41`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c46395e6572c6562033070591920a54c30f0dd5976661d0fff379397e3a85ec`  
		Last Modified: Mon, 10 Mar 2025 17:40:06 GMT  
		Size: 145.6 MB (145598924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f433d0cf5d2641471b3ef8d2437a8a231be4ff50bcb8cb5b9c783fa03403b8`  
		Last Modified: Mon, 10 Mar 2025 17:40:05 GMT  
		Size: 69.5 MB (69527804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5411ede4d5051c02d929f5b17b6f7167bd7d1f8d9a2f4a909bda25f3abd17466`  
		Last Modified: Mon, 10 Mar 2025 17:40:02 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:73df0a4147d389f7339524e2c22ae14eece495db4dc5d9739d7c369229996a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4947036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2523f556a393af4fda703e7cb4891068fa71db053e007b8790354913a10d3970`

```dockerfile
```

-	Layers:
	-	`sha256:285a3ac284e8f2379a3c632c6d5a36159380aca8756e7b4b6de107b1e2f36d44`  
		Last Modified: Mon, 10 Mar 2025 17:40:02 GMT  
		Size: 4.9 MB (4932726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9be79041d0590a24fb2549fc4470216ff343928550b31c870cdaf2d2205fbf2`  
		Last Modified: Mon, 10 Mar 2025 17:40:02 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:057209c25bd5626d8d10b38eaacdf5b114030386c8537c998bd6d3803e3477dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.8 MB (239813475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7290ace3800aadac4ab4eb5724a6edba9ce32ef09c226cb7cedffefcd32801d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be359407666b60496d85a7e4c0764526e9bdf9900987324b733ad8b60c22f88`  
		Last Modified: Mon, 10 Mar 2025 17:51:25 GMT  
		Size: 142.4 MB (142385397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a96cc9494abe36e44c6326c19b1c760220df99fe950d71cd6b3926a3507bef`  
		Last Modified: Mon, 10 Mar 2025 17:51:24 GMT  
		Size: 69.4 MB (69379005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c503f2c0017c6f1f402137cdbb99e2599bda8811fd896486b9f17016fa9de5`  
		Last Modified: Mon, 10 Mar 2025 17:51:21 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c81b347af62c0fece81a31d8df00a04a4722bd96ca879556f51d2054e5afc5fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4953533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b8230578dff112a515114410fcdcda139c8999981be687a1672a5c929f89c76`

```dockerfile
```

-	Layers:
	-	`sha256:c5191a685e007c639ea45a506b6fb3ee58b62654e5130f3ce7085a1b0c77bb44`  
		Last Modified: Mon, 10 Mar 2025 17:51:22 GMT  
		Size: 4.9 MB (4939105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac357f7b23dc984baf18cc553dc21be72f515737d2d373e3439b73b6eb17f1e8`  
		Last Modified: Mon, 10 Mar 2025 17:51:21 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
