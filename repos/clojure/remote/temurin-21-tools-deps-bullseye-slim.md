## `clojure:temurin-21-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:c19519899f8319192f1672cb71dd3477449b293bf64c3570feabaf520c73a929
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4c32ad7de864b24cc6498d13150fa12f6e94c674879149cd265f8a3868f06bfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.4 MB (248353224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b57b163c0775f9b539700a9c5891090a1422cb37d5aefb714483480e43602223`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8b7e31ca9aa76f3eabffdbb81ff8deb9443fbd4529199f5a4f7cd6230523f7`  
		Last Modified: Wed, 29 May 2024 19:58:30 GMT  
		Size: 158.5 MB (158497942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b65f7b62bf28bce6935e8686cfa411e476d1f52216958ce28436cd1dda27c79`  
		Last Modified: Wed, 29 May 2024 19:58:28 GMT  
		Size: 58.4 MB (58420302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22b6c7b28ccaa7ebbb5f0b1f4a5c4c7c03fe384219d344a366ea4a7f15c2efb`  
		Last Modified: Wed, 29 May 2024 19:58:26 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89ff40e18fba73dd4140359a312b82ed6b56898e426752536eb85f667e3249d`  
		Last Modified: Wed, 29 May 2024 19:58:26 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c925e18e33e914aa67f03316baf9e2ac4c899eab78ab3212b51e9f31eee60ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4926099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d8c330726b3dbbba0ccbcf665a08e64f6035efc5d30eeb5a0e58548e33b021`

```dockerfile
```

-	Layers:
	-	`sha256:6f356cdc307047df5a662339a5e5ddc9d9443f9b2d86d2d498a543b590263128`  
		Last Modified: Wed, 29 May 2024 19:58:26 GMT  
		Size: 4.9 MB (4909940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f137a2f947c25de069ed6e6237dc33d12e564461f4c7955b6bcc44be23155f9`  
		Last Modified: Wed, 29 May 2024 19:58:26 GMT  
		Size: 16.2 KB (16159 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9459d8ff081628cb8b1ee9e284edeef7742db2e5340887d1adec85951de32add
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 MB (245293653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:998816fee1d4efc05a407909f56214a64ac161a9ca64ec0e5aafa6daae68f1ea`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36739f47c257a5ce7926e172a2385e063cebd51a193f6f9a8289c7af2ebb3679`  
		Last Modified: Wed, 29 May 2024 21:50:36 GMT  
		Size: 156.7 MB (156665602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a60935648a3d13345349c0aa9ef19c562545d62243f63d9126700d427820e1`  
		Last Modified: Thu, 30 May 2024 00:21:40 GMT  
		Size: 58.5 MB (58540095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0976c04d468c2e0702c752f12b50c5767a2973e1a25f8722d59370a65f68696b`  
		Last Modified: Thu, 30 May 2024 00:21:38 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4567ac9aa3b629c48f89ffd309e43a868fa0ff2416c984d6a1f85759556d7285`  
		Last Modified: Thu, 30 May 2024 00:21:39 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3fbdf0aec8ece15f1fb59ac88fd86f294459cec04a162352f86040b80066031c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4933044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0192ccc8fe930747ac5326265ff44095701ea0869cdb9b304fb4769ac56c5b5a`

```dockerfile
```

-	Layers:
	-	`sha256:8a3c9ad670a9b48c6e59a983037c24fb20b14951381a724fdee3029e17c5401f`  
		Last Modified: Thu, 30 May 2024 00:21:39 GMT  
		Size: 4.9 MB (4916320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a52efc06d750e4e8720ff3cba5aa98501b08b1c350b8ad57302f1842642a680e`  
		Last Modified: Thu, 30 May 2024 00:21:38 GMT  
		Size: 16.7 KB (16724 bytes)  
		MIME: application/vnd.in-toto+json
