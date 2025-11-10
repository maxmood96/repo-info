## `clojure:temurin-21-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:cc9b8b33ae0f1250b49b9cd24ed383c3759d4601f0267d9090202544061605ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f6088708796ce5f0fd3f843a31d08a39638be459e4fea7cd2b82d23d1ac1c02e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247236695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c9443ab28352c8b65350d9e2c2036770f4c438e890fc257cf39e49f423a458`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Sat, 08 Nov 2025 18:43:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:43:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:43:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:43:57 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:43:57 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:45:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:45:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:45:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:45:02 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:45:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977a11021b1e8739ef70a03594a27b853f8524cc230a3c649f984aad414aef53`  
		Last Modified: Sat, 08 Nov 2025 23:04:28 GMT  
		Size: 157.8 MB (157825965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907a009bb86cdae52d0b4d59dee3150bce44063be6b364f17472eab35fa72052`  
		Last Modified: Sat, 08 Nov 2025 18:45:30 GMT  
		Size: 59.2 MB (59151090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0edc797e1dbc0926b95c4c815c42653d79bd532fc2f35a9153b846f53ce4a13`  
		Last Modified: Sat, 08 Nov 2025 18:45:26 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeab37e3a2825bff62967bfcc39d3f6956b1417e4a26f8bed5aae2db8792b33b`  
		Last Modified: Sat, 08 Nov 2025 18:45:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:923411388298a7c67008ddfc93bff321dd0197cb5ad0892e58f8a2e90cd808d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5327007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e19cde11d5501784f924d641837c8bf5863b6b43fc008b2b8595141883b14f6`

```dockerfile
```

-	Layers:
	-	`sha256:6f737e26aa44be654988dc84338a9daa476019b379da052e2609add929e23653`  
		Last Modified: Sat, 08 Nov 2025 22:46:25 GMT  
		Size: 5.3 MB (5311171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:535d633d1d3d7e4798c1e59db97c01ab1885daaa590a55e17418f2020d2a0f50`  
		Last Modified: Sat, 08 Nov 2025 22:46:26 GMT  
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
