## `clojure:temurin-17-tools-deps-1.12.3.1577-bullseye`

```console
$ docker pull clojure@sha256:d50e690ecc9f9ad987a148d0feea8df20aed5914520e7948a8f60af9bcf48a5a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.3.1577-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:41a73a56793c158c60bc656b35f1234def80c8e1f1aea6767e48da3fa2f1c64e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 MB (268166571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93da236b1c620e7ab30f4793377cc24bdb7a5a4a6f23f17d28c3425020d6eebc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Fri, 14 Nov 2025 00:53:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:53:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:53:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:53:01 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:53:01 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:53:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:53:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:53:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:53:14 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:53:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f1bde766c0f53226a997ec3e31033ec25f005cefe6fdc26cbef5bbf5614dc3`  
		Last Modified: Fri, 14 Nov 2025 03:12:27 GMT  
		Size: 144.8 MB (144847974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21aaf26335fc846e6c5cb8d5d0362fec84cca410117c8ca0e294c865599654b`  
		Last Modified: Fri, 14 Nov 2025 00:53:48 GMT  
		Size: 69.6 MB (69560863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeafa3e4ceebe4eb4271d6586df68ab9e3f37ca13e7b947b78aeb31146489df6`  
		Last Modified: Fri, 14 Nov 2025 00:53:41 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c734f90a30c3e531e4832881b63d643bfdb9116e30aa9b537821ac21dd3604c`  
		Last Modified: Fri, 14 Nov 2025 00:53:41 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:0a0d654672cb1dfa5a95a14c96c9882dc5702b24bff77c7064a4aaec128ae903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7411447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:045a281b7e36916507f8756b4ccbbf227ea7831ae9b73d60283139e2142ea1e5`

```dockerfile
```

-	Layers:
	-	`sha256:d48a7387be529765c36a65166f8ba40172be701f60d363b01b74a6568ff93d02`  
		Last Modified: Fri, 14 Nov 2025 01:38:57 GMT  
		Size: 7.4 MB (7395669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:388b39f0aa9c6cc1a3dc0c929fd7e09642f7feca51f6aabe83e61764a70f33ad`  
		Last Modified: Fri, 14 Nov 2025 01:38:58 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cea244d1e3707bbdc46ecf750934a1ee30c91ee0997e61541250909777f1c0a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.6 MB (265627310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b282cc56bebe3326b658eccd43826e876a874247bd7afcab951be51e095cffc0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Fri, 14 Nov 2025 00:54:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:54:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:54:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:54:52 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:54:52 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:55:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:55:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:55:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:55:06 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:55:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b1c9a2dd4f585c9f9c803c9bdd9ffdbe1ee8c35a881c237217d67af6d43701`  
		Last Modified: Fri, 14 Nov 2025 00:55:31 GMT  
		Size: 143.7 MB (143679915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961cd2423b50c199f2a2a1b5c7edcb96018cc555b14ac983f7d660bada87d66f`  
		Last Modified: Fri, 14 Nov 2025 00:55:44 GMT  
		Size: 69.7 MB (69688387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c59af72c8c7e525fceab3abbb04c97cbe6df00f2f5c8158f5f37aaffd4b4f9`  
		Last Modified: Fri, 14 Nov 2025 00:55:37 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c29a9aa5d71284bf54ff4bd240c399385444393d5e6b09012109aa63e79f040`  
		Last Modified: Fri, 14 Nov 2025 00:55:37 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:998c9e10a110878f257c0f2b06f130e91eae1128097e8f787a9ee2c907af9cd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7416663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae1b23a1f560112eea3d6ecb4d69de6582587e6dd9702ccd0269c119b8db38f`

```dockerfile
```

-	Layers:
	-	`sha256:dc8dfd86f89bf6f1c480dcdfb2604b8b4cb254f076c9683f65c7b1c3a1b72b30`  
		Last Modified: Fri, 14 Nov 2025 01:39:05 GMT  
		Size: 7.4 MB (7400768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:697f4aa21e078ef6a2d30ebb53e56a72ef197341b8a9df028d83b2d7b5ff0d06`  
		Last Modified: Fri, 14 Nov 2025 01:39:06 GMT  
		Size: 15.9 KB (15895 bytes)  
		MIME: application/vnd.in-toto+json
