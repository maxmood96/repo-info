## `clojure:temurin-21-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:4d8a9174b87e692f272f970f267a70901a2db8b18186bcbe5a283e09245c4faf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:51b54878bcb466f0c4d149cd24888ed58b22dbc7a272a28a5f198056c930288b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247237721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83f3ae50c080c47e20d482ebed5ca9ba0a1d0fd41a13e959f8818fe725b46d94`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Fri, 14 Nov 2025 00:54:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:54:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:54:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:54:37 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:54:37 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:54:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:54:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:54:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:54:50 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:54:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66dfe5240b377be5a4986f529c3b1a22b70a6cc5c5dcc0d3f1413233e8323ce9`  
		Last Modified: Fri, 14 Nov 2025 00:55:18 GMT  
		Size: 157.8 MB (157825975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e4d8c0b8b7e2251066de20a855a98663635cf1e2ab24d7fccefee47d817866`  
		Last Modified: Fri, 14 Nov 2025 00:55:30 GMT  
		Size: 59.2 MB (59152108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6dedabb7b350c2ee2fbaeb6ef7a89ccbedfef2b6c7e5ffc586526d6d7869ffe`  
		Last Modified: Fri, 14 Nov 2025 00:55:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a924a99cdbc127db990d0e2ff42362e20de5197867c109f289cb65167e07dbf1`  
		Last Modified: Fri, 14 Nov 2025 00:55:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b2504a4a617cf9bae7b0ab466d62019f393812a61e93ded7c229abcdd6233e47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5327007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:867f593cc5d79228588b2700ab3ada388eb3f0662d2f475077e34564f105c887`

```dockerfile
```

-	Layers:
	-	`sha256:4fabd8b553e7c36a2524caa49decbe1c57648b3b08272c6edbb7240b5555808c`  
		Last Modified: Fri, 14 Nov 2025 00:55:09 GMT  
		Size: 5.3 MB (5311171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b2a01673e0819c08f7e8ebbcfe1606fdc1e59474fbf93992323c1670eda38b7`  
		Last Modified: Fri, 14 Nov 2025 00:55:09 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6f2bb00336acf7a1b779afa18618a48a2861c2825c6615b866553c8782821629
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244144967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3f3a00f164b0762d45474120c21f4d44b4514f771fe49d7cc375d9d3d9f364`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Sat, 08 Nov 2025 18:44:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:44:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:44:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:44:31 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:44:31 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:44:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:44:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:44:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:44:44 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:44:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657802403e9773f03ba974cab7fc54ac3c402257bd472582ecc4391b6f5d8b00`  
		Last Modified: Mon, 10 Nov 2025 03:56:18 GMT  
		Size: 156.1 MB (156107661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487a70f56fdb479be56468e64fe82cc3efa54298156970c9814a49b56b19063d`  
		Last Modified: Sat, 08 Nov 2025 18:45:29 GMT  
		Size: 59.3 MB (59287710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2740a280ce1c495f7d5f77661c7438cc7d05ea649bec05b4c40ff1aecd81999a`  
		Last Modified: Sat, 08 Nov 2025 18:45:22 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3382341ee368d91ba1c225a3c2c65ef56ed5e5f550e8f18c2baa8ce42226376`  
		Last Modified: Sat, 08 Nov 2025 18:45:22 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d1f2a6c37e3169af5010078c496efe925c6122e35365f176dc96fef378d8ab0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5332857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ab00a78fe7091d457e1b20d2bfd64eb7e8d61e86b7b5a50cbfc13ddaec9f2de`

```dockerfile
```

-	Layers:
	-	`sha256:3fa3e01200526a19711922e52f9d1011cef6396b4ae492246427486873a02ac5`  
		Last Modified: Sat, 08 Nov 2025 22:46:32 GMT  
		Size: 5.3 MB (5316903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:562a7691cb00dfdccdc9d65d61477d7801dd1b81ef634539dc306e985ef5cc14`  
		Last Modified: Sat, 08 Nov 2025 22:46:32 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json
