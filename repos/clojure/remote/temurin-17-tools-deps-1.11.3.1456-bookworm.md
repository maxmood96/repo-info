## `clojure:temurin-17-tools-deps-1.11.3.1456-bookworm`

```console
$ docker pull clojure@sha256:d59fe72649b00a7eb15ae9bf71b55198eedc8eaa237641ece173f53a5ef5a1fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.11.3.1456-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:45e260d4b4fb7f9088be68e37432ddf2eda78d6d65e1efe12cab9406bc5c4a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.0 MB (274971894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9968f05900d7fa3203d03581b3c53779166e13d6395d94d6dc4427c57e3a45`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
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
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0456ca8fcacbb5f58fbe1d2e372e7b8ae6f2951197eeeca68d69222522f83201`  
		Last Modified: Wed, 05 Jun 2024 06:10:18 GMT  
		Size: 145.1 MB (145095091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9869d9d6f52562f236b27c4b0c74f7038b3ff1eec6dcee4cf1a90c24e751ea62`  
		Last Modified: Wed, 05 Jun 2024 06:10:17 GMT  
		Size: 80.3 MB (80299366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d3d53d4406c80d9df6a2ff64fabc290c57d0617b3d0664bcb7a307b9f29fdc`  
		Last Modified: Wed, 05 Jun 2024 06:10:15 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51baec31d4e3245dce59421d41f9e84ab35383cbb1cd9eda3d6900cc80dca045`  
		Last Modified: Wed, 05 Jun 2024 06:10:16 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.11.3.1456-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d3d7bba1972066ee93b4e8de72838ae66a1286c62f5b57ee8b2349e25f343a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6976056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be8448ae55071700a68e4717d39a64c1eaa040b825bd2d017b46b1e6ce5e37e`

```dockerfile
```

-	Layers:
	-	`sha256:ff18e49c536bb8ff69d8e1630062fabed5ec8a6e13638fa45ed6be37b9e6aee0`  
		Last Modified: Wed, 05 Jun 2024 06:10:16 GMT  
		Size: 7.0 MB (6960666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83fc9033db847a3a97f9cbe7724179e2df374b46ab433c79beb6f9e0bd547616`  
		Last Modified: Wed, 05 Jun 2024 06:10:15 GMT  
		Size: 15.4 KB (15390 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.11.3.1456-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3545848fb690ab845ead8e6810b14174fccae7a4cc72034a8c9763d94fa4d007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.6 MB (273552456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6379f3cc8c21b03418069dda1a40472a88258c8e3b8a9a0a66c5bfe6d19a5863`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:cfc8f76c8181d3ae6dda16ae894b184c69dbba114d446426e466126fe0ae62e5 in / 
# Tue, 28 May 2024 15:17:11 GMT
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
	-	`sha256:1e60a453843e00d6f3d4242dbd696365f0894e3ca2f02f4ce1ab098d7ff7907f`  
		Last Modified: Thu, 13 Jun 2024 00:42:50 GMT  
		Size: 49.6 MB (49613402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:798af59c3dfe0a2333f71d50df86f26dd31e844f8565450854e2afd957021b4b`  
		Last Modified: Thu, 13 Jun 2024 11:35:17 GMT  
		Size: 143.9 MB (143892766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3fc1393c776f72d38cd1a60d48c5ef3c3461661bd48fa34ee590ab480bc4ba`  
		Last Modified: Thu, 13 Jun 2024 11:38:42 GMT  
		Size: 80.0 MB (80045241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689a27c7b8f65b1f9338ab38ab5f7e909ca0d1749f984402b4cd11def3d0a11d`  
		Last Modified: Thu, 13 Jun 2024 11:38:40 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a512b7fe5f9c6f334eec69e60acceef61b1dbd1e902032c215d060eb9fee2d5`  
		Last Modified: Thu, 13 Jun 2024 11:38:40 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.11.3.1456-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b1b1c4fbf89d7e2d2f8725f4c2cfe66fefd1ac312a18cea64bf4edd46f420e9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6983028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc5f134c2931e35c7f92710b3afd8ba2e9499f001ea7d27a749961d2b6618147`

```dockerfile
```

-	Layers:
	-	`sha256:118c7d59c9cb4f7d198f6f1665fb59ebd526e350a86effd7f18d373487b0626d`  
		Last Modified: Thu, 13 Jun 2024 11:38:41 GMT  
		Size: 7.0 MB (6967053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3d4e5d172181b0850dcfca5121846ddacad6c03659a2d6ba922ffc72115e3c0`  
		Last Modified: Thu, 13 Jun 2024 11:38:40 GMT  
		Size: 16.0 KB (15975 bytes)  
		MIME: application/vnd.in-toto+json
