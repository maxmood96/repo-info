## `clojure:temurin-22-tools-deps-1.12.0.1479-bullseye-slim`

```console
$ docker pull clojure@sha256:477a5e67264a89cd4020f9e5cecaeec4002636c13c1c2f3c66a1c29535d58242
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-1.12.0.1479-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a24462e0988b30aa9dd22d7cd0a75272f68fef117d495a5416094bf3a2af3f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246851267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b6dd56b2ba239db5c405603fe02e5c3af3ef03a22c65d41c5bb083bae8c407e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8055ee09ed0a60659ef48cfee9c056a15b9ef01b0e0d80c1716d1fc740e7d2d`  
		Last Modified: Fri, 27 Sep 2024 06:01:40 GMT  
		Size: 156.5 MB (156481594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b53b2833b9b77f9b6fa667ed78a6eb78f26ab44b7d5a3d7f1c54bd6669e8f5`  
		Last Modified: Fri, 27 Sep 2024 06:01:38 GMT  
		Size: 58.9 MB (58940036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e5eb7a01eaa7a029dcf6997ba0627f8d3bb8d262c97fdba4d7860e1750d8c0`  
		Last Modified: Fri, 27 Sep 2024 06:01:36 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a40211d0c5d017a89e157714c782b0f848716031e0466f33013f15849bd2e0`  
		Last Modified: Fri, 27 Sep 2024 06:01:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:38d43415d3cc1f393ead03fa7462f1c45ea6abfa35326b44b91ef466c28feb4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5118665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4dfe2486295f738e9326a2ff42e732320045e44f0f6c7e99eedbcc202c3627d`

```dockerfile
```

-	Layers:
	-	`sha256:1fe05d58c21207d69e0531204ded67a6800b727114aea18f6722c58d6c16ce62`  
		Last Modified: Fri, 27 Sep 2024 06:01:36 GMT  
		Size: 5.1 MB (5103152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd0fd9d1b7cab4c995d210128b3a9c7ac486f82f1066fde28be20b3b36296d9e`  
		Last Modified: Fri, 27 Sep 2024 06:01:36 GMT  
		Size: 15.5 KB (15513 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps-1.12.0.1479-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7107a103a45c4825afbd45418ed01dc5ee2762b1922f7cc05e2cb8844722483b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243650705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d830fcbd7d375a81075b0aaf44485ec7f3fb82a94709d8ba6dbe4e20f285d2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 04 Sep 2024 21:40:08 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Wed, 04 Sep 2024 21:40:08 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50350f2974c0417f312abfa4209238a88e094d8f3d7ce45496c26f6a51b902d2`  
		Last Modified: Tue, 17 Sep 2024 04:54:51 GMT  
		Size: 154.5 MB (154503758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3046c278c6af29b50470f4f0fd30fa4c61341d1fea06c228fd3d256023753faa`  
		Last Modified: Tue, 17 Sep 2024 05:00:00 GMT  
		Size: 59.1 MB (59071538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23693893a4f5f34d714886d31c9d32eebbe9e86d45fc1085b45c1d2f7ff5add4`  
		Last Modified: Tue, 17 Sep 2024 04:59:58 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f5fa3d745ac9a8d1e3dfe4f65a47abf87f6299eb1befe8df5279a9ac1f2d85`  
		Last Modified: Tue, 17 Sep 2024 04:59:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f401b603b7d99c96b566d3c384ed0b0b4d9b2e2b8e9882f74f3713db6541b138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4972229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd5e7cd084cb1740f35d096916af691773d776b566ddebbb7037f27345585eb`

```dockerfile
```

-	Layers:
	-	`sha256:288c8849c625464960c75db80a80c309f1c23a92481505ddd0875478d7ce0470`  
		Last Modified: Tue, 17 Sep 2024 04:59:58 GMT  
		Size: 5.0 MB (4956176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0a3dc2b581b090675d6d38c04a8c5a45f55c9649cbd424920dbac7ff1c05cb3`  
		Last Modified: Tue, 17 Sep 2024 04:59:58 GMT  
		Size: 16.1 KB (16053 bytes)  
		MIME: application/vnd.in-toto+json
