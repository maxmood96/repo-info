## `clojure:temurin-21-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:ad440baf4ab3b83a9990db03c2c4a7c48474d170235c225dfa7f4be40a92db78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e953959a89e205a992cb848d87e0695778fb4892906852d78db4dad6239fa5a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 MB (281121513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2aa87fd95f443aaf122b186890e1c2afc25f59547010f3b543ad0d9992bd9b5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:10ffc47270cd106d2d04bc7ef4749d579620e45a84804ba3b18f0898fe5ecc64`  
		Last Modified: Mon, 29 Sep 2025 23:35:07 GMT  
		Size: 53.8 MB (53756064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7740dba7a63f21e173a488421b5a4f55ec6e1718ab5562fea1bdea35ed5557`  
		Last Modified: Wed, 01 Oct 2025 00:59:15 GMT  
		Size: 157.8 MB (157804727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1348571b3f17ae3439a5d4a47b1317cda0a0cef6cc00b628cd96b6b43a8dba`  
		Last Modified: Wed, 01 Oct 2025 00:59:12 GMT  
		Size: 69.6 MB (69559683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086c778d8e6aac3760ddce54e759b9764f2b7828a0176ecbbf906abcb52c6f0e`  
		Last Modified: Tue, 30 Sep 2025 00:55:30 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a2a72d18eb27839efb1e1b5c721b8052bbe84a6734c1b054dff75c9d4836ac`  
		Last Modified: Tue, 30 Sep 2025 00:55:30 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b7f76ccd1f8893429f73199ffa23867d5012981cea11e0d28e4da659a95d14e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7414590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5a5d4db557d07cfaead4205daa22d7af2654dd7bfe9dd8296576f7d94310c7`

```dockerfile
```

-	Layers:
	-	`sha256:6214c182aad362dc0e85da90c993285087351a119028443a2621ce7576c81e67`  
		Last Modified: Tue, 30 Sep 2025 21:35:44 GMT  
		Size: 7.4 MB (7398769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a74262865fa7805c851573503742072a719d037fe3a5c274d2792a19105303b7`  
		Last Modified: Tue, 30 Sep 2025 21:35:45 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d80fbc20b1e73007fd095a2aeeca987147d6344d38c2ae05e5d4c85c22b78f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.0 MB (278027043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72684cf7e06504a0c5f5b7c729497f20fa10fb7a256fe1e5343e88b20302e782`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9b16ae1bbd1ada84c12528379a10e280bd89e0d0332670c8487145eb77fe2fe1`  
		Last Modified: Mon, 29 Sep 2025 23:34:42 GMT  
		Size: 52.3 MB (52257414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9840c31b168bb172aeb5507c61f6c096f5577fc7590feb82e8e60a5cf8a2a72`  
		Last Modified: Tue, 30 Sep 2025 00:54:08 GMT  
		Size: 156.1 MB (156081234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9b104ed485c4bca39782636350ae7cfe38fdc906bc95acfcac1008c5996423`  
		Last Modified: Tue, 30 Sep 2025 00:54:35 GMT  
		Size: 69.7 MB (69687357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ff5a42e6f212f25df08acce3a05f5f8ad073bed133c6c509cb927301687bd9`  
		Last Modified: Tue, 30 Sep 2025 00:54:21 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3f338b6a7906f1ac288a1124ebd43d887bd75af919e8282bdbae02939fb5de`  
		Last Modified: Tue, 30 Sep 2025 00:54:21 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3064d37e280876bb34c1c727ce749af866ffb6e7f13739729a984b0bf60af85e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7419807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:614d8c591a51074e54d9860e4933ad9673c64094f8af6520cee2a09a688c6d18`

```dockerfile
```

-	Layers:
	-	`sha256:46373fbca2995df71b924905808ba951ed431fcb2702a9b3e21ad3604d1f6130`  
		Last Modified: Wed, 01 Oct 2025 21:41:57 GMT  
		Size: 7.4 MB (7403868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a41189bbc9f83a099a2f8bfdfa414b1fe86bd60ad24d31ed876f6981134cd85`  
		Last Modified: Wed, 01 Oct 2025 21:41:58 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
