## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:f8d40d9152ad1f024eb695d95fee660af22bf61bf40ab47b850c344410b045b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:15de8d3c425756121c59c90f1c249960a8d46e31b529ebaa452ad49a849a120b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.8 MB (234849910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a9afcaf2f39006aab064183d5d75cb9f7a17583a0c9bb29dd36ee3bc1166d6`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3f6ce8b073e7eef71039f57ae204d4e8c775628be068575fb8d98c6f685bc4`  
		Last Modified: Tue, 08 Apr 2025 01:35:50 GMT  
		Size: 145.6 MB (145598939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9acada818cc701bf9217724c77512e3728c93247b655ce98f6a58985587857`  
		Last Modified: Tue, 08 Apr 2025 01:35:49 GMT  
		Size: 59.0 MB (58992907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:709725af712c6d312a9fd4c543a4919e0e3669a787ea927176595604359d965d`  
		Last Modified: Tue, 08 Apr 2025 01:35:48 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:73df2e3561fa3f97409ccda2a3321846113ce8b55bdef58ef900f5b2f4dbbc6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5153464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33871ab3fce16e2e861e3cde32adfadfc0f00cdc51b09e68288e2f8226dcde2e`

```dockerfile
```

-	Layers:
	-	`sha256:ad0b079b8120d1454c3cd15571557d5e80e95143e136efa7f812b6b0fda6019e`  
		Last Modified: Tue, 08 Apr 2025 01:35:48 GMT  
		Size: 5.1 MB (5139154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcb8a7e6cb9c4472f7952e073450d7dea0f384c6a58ff22ea46c1178570fee82`  
		Last Modified: Tue, 08 Apr 2025 01:35:48 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e9865943d89c447cc385209e1bb77beec574c8dc9233596209167d016d8ffee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 MB (230040368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b31f41a81823b3a590a3fc82108cbd16f2f39770d1a01472585ef466eaaa4b8a`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
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
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31bd0e4f078c2c4cb2dcad1abd23a72f823a227be81994064233a92f643e2346`  
		Last Modified: Tue, 18 Mar 2025 00:07:31 GMT  
		Size: 142.4 MB (142385397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7be6b68328b455427b4389c08663a08eab07a36f994e44e58e4bfc6721f7fb8`  
		Last Modified: Tue, 18 Mar 2025 00:07:27 GMT  
		Size: 58.9 MB (58908403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ef996b5318165ae8ab33e14f9c68f1e36a642e54a18bc6572d84566c7d51b5`  
		Last Modified: Tue, 18 Mar 2025 00:07:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ce43869369f38d89132b1771dc13d6e55dc48688e731b69d2ec355bc1d542b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5157986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b75a70836536c57b03551d37acf28dd62b4091fd0b91f4d20015b636a68d18f`

```dockerfile
```

-	Layers:
	-	`sha256:4d7f02d179d5ca0288acb0af537c2af2f665269cabdcd00306d37ec3fd85fbe6`  
		Last Modified: Tue, 18 Mar 2025 00:07:26 GMT  
		Size: 5.1 MB (5143558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5514cf0d054f9f31fb7d98b3f0984726ea86781605ae586468a5be6984c3b7b0`  
		Last Modified: Tue, 18 Mar 2025 00:07:26 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
