## `clojure:temurin-21-tools-deps-1.11.3.1456-bullseye`

```console
$ docker pull clojure@sha256:c17668fe0924c29a63db6a8badc198e1e75e81774e1263520f1ffa62d91d3e36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `clojure:temurin-21-tools-deps-1.11.3.1456-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:01112be7d78635baf4bc13168359f659dfd9048d8fcb4046da9b1b417cea2db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.4 MB (282414931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83020712fa014fc9c10c61e22d9eb09eb543d662f53d81ededefbb71fe294ffd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:28:14 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 14 May 2024 01:28:14 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f24651d987a2e75e63964720e07e73969c555c53a3bb0772657a5f25cd5e5a1`  
		Last Modified: Wed, 29 May 2024 19:58:24 GMT  
		Size: 158.5 MB (158497991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4bc0efe356c541549aee17ca2f588523340e5508e6c9e2484baa95d378505e3`  
		Last Modified: Wed, 29 May 2024 19:58:23 GMT  
		Size: 68.8 MB (68816493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c728f1cbff89c4a6eef955acc869275f2e1a966534e88d387b04407635bdfe`  
		Last Modified: Wed, 29 May 2024 19:58:22 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea24a54e3489f5b4be5b5b345772794b801d304ca4407e140c92f4584e044fc`  
		Last Modified: Wed, 29 May 2024 19:58:22 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.11.3.1456-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:81999d0a9acde30897659a9e20f51257427be9d8c6d9b49a1fe4ba26cb7ffc34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7016504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b66546704020225bb6ca5bda369e04b4209a50103b8bd6cfe6b92fb3064be3`

```dockerfile
```

-	Layers:
	-	`sha256:9e755d0beb902aa0269e03b7f4b74e1310a9864e8f50fb6961d8e701441c9f03`  
		Last Modified: Wed, 29 May 2024 19:58:22 GMT  
		Size: 7.0 MB (7000438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cab113e1477da700c7b2d1baf4b97e7e5b9b71913504b1d5cbcf1eb63203a5d`  
		Last Modified: Wed, 29 May 2024 19:58:22 GMT  
		Size: 16.1 KB (16066 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.11.3.1456-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cf81837ae4a6b997241211dac1007d73c02cc7f5a12194d594a53f5470116f7b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 MB (279543586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e76edb373ae0cc979def44d3218881f54b949623f70299bb7447776f13f62c19`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:47 GMT
ADD file:43721c605da3f74f0c3f71384780fc0e57e2478b88197672caaf4baa3eddab23 in / 
# Tue, 14 May 2024 00:39:48 GMT
CMD ["bash"]
# Tue, 28 May 2024 19:44:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 19:59:07 GMT
COPY dir:96a90c8e1c03defb238a6d560d8927dc81a1a58af3fce1471cbce5249ed27f38 in /opt/java/openjdk 
# Tue, 28 May 2024 19:59:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 20:00:53 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 20:00:53 GMT
WORKDIR /tmp
# Tue, 28 May 2024 20:01:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 28 May 2024 20:01:08 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 28 May 2024 20:01:08 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 28 May 2024 20:01:08 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 20:01:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:078d9526cc72763b2db16388f6b511c18a73e3e7f9d229364b3b85a6b5277bc8`  
		Last Modified: Tue, 14 May 2024 00:43:13 GMT  
		Size: 53.7 MB (53738990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab01a1138782d172d90f49938d22afd85b2634e691bf05dc5364d46e30bbb34e`  
		Last Modified: Tue, 28 May 2024 20:18:53 GMT  
		Size: 156.7 MB (156665547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a4d967f2a1f6f60db4599c4bb8d53365bed48668624b79f4868916de72165c4`  
		Last Modified: Tue, 28 May 2024 20:20:33 GMT  
		Size: 69.1 MB (69138030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6da733af34c3ec9b5b24705b69d7b7a51e8379d4aebaa1f76ce21e92968ce7ba`  
		Last Modified: Tue, 28 May 2024 20:20:25 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f80a725a9fc7c4e079884bae0d726767035c55212276c76a769949198cc2fe0`  
		Last Modified: Tue, 28 May 2024 20:20:25 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
