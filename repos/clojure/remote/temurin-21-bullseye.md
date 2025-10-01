## `clojure:temurin-21-bullseye`

```console
$ docker pull clojure@sha256:7b913693fed153736c6024cd598bb066b17e4394daf83e89217662cae5b22b8f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye` - linux; amd64

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

### `clojure:temurin-21-bullseye` - unknown; unknown

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

### `clojure:temurin-21-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f6e40b466511423cfa911cf7856a6ff72db105ecbbe3bfe5a8dbc75f468e6dd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.0 MB (278018969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429eb0ce2e0822e36d7bd15828f13104c0082e64c49ba529620e6f402f861c7b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
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
	-	`sha256:7df02cb4a974a4e8a9eb65ffcff7274f9dca341d29aaa763294c42e49805ca19`  
		Last Modified: Mon, 08 Sep 2025 21:15:41 GMT  
		Size: 52.2 MB (52248370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbb5d817a7ab755bf13f36abfc3da40d21d97b5786f87c575375d86418be679`  
		Last Modified: Fri, 26 Sep 2025 20:01:58 GMT  
		Size: 156.1 MB (156081217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82c30629e2cfddc0d27c8b4c7c6a22d77f61f57f1694b5659c901d2eeb4eb82`  
		Last Modified: Fri, 26 Sep 2025 20:02:17 GMT  
		Size: 69.7 MB (69688342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fbc7d0f4f8d362dac25a3f712149ff200eac6e8a3fef5877525dde94810bd7`  
		Last Modified: Fri, 26 Sep 2025 18:48:43 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043e90b0bf2662358cf0f094c25f4398c805df5799893e638095333950527ef4`  
		Last Modified: Fri, 26 Sep 2025 18:48:43 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:88d487f2e1afb33091453fc21e16e77ecee6f0487dc14e4f8546f12c8fe60bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7419807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c758bb33f16ebca0ef848206fd3e05c29a685dde01dd4b9922e89d3f1514b80e`

```dockerfile
```

-	Layers:
	-	`sha256:ad9acf8326a210a46fd7753aeaae0ab4ed804fc635b16a1b9dfa4418c0f48c80`  
		Last Modified: Fri, 26 Sep 2025 18:41:36 GMT  
		Size: 7.4 MB (7403868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cf3278cd798f870e12ed286c47f9e099d0e4a6162ac213f2ce5889e23281584`  
		Last Modified: Fri, 26 Sep 2025 18:41:37 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
