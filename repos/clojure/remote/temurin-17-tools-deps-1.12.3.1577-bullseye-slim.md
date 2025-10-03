## `clojure:temurin-17-tools-deps-1.12.3.1577-bullseye-slim`

```console
$ docker pull clojure@sha256:d718fb432f96bc54799d152d63a91b68531c32467a9b71130857792cbad23f4a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.3.1577-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f4efdd1177152a0b3bbbf0971be3cc24e7eae97099c132076f1f8888d5726d44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234103518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f29040b3e5fd0c28d14c1523993662df669ebad185975df9efdc35a7c4eddf`
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
	-	`sha256:4eb1dd59a73886acc6a3cc9d4c8f8e66d1fd6ba6d6195b05ce21c22b0658aab8`  
		Last Modified: Mon, 29 Sep 2025 23:35:18 GMT  
		Size: 30.3 MB (30258363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ffe0c8f028ea13cda03a5b80dc9f4accef014168d29b126a5062273571e972`  
		Last Modified: Fri, 03 Oct 2025 08:21:29 GMT  
		Size: 144.7 MB (144693589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3903cbeaeceaed88684e6cc97dfda251436e6e3f69917a950bf2222a049a7dd1`  
		Last Modified: Thu, 02 Oct 2025 08:59:06 GMT  
		Size: 59.2 MB (59150525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895f04a1ad9f8e1364cdcf5c7a726c0b522147eaa06d0a4de31f336bd79d019c`  
		Last Modified: Thu, 02 Oct 2025 08:59:02 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a87e4b940fa505dc3461a19a59e32158c7339fd99df79a7d627d3f8ae3f4552`  
		Last Modified: Thu, 02 Oct 2025 08:59:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0ca59450c81c7a32d04c5fd82a8ba81c48b2dfe67e8e35618735d91e87c6d9cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5323943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c95b994b576398cc027130fbd250beb2b18544b2695f2cb6528be4de8f95bbc5`

```dockerfile
```

-	Layers:
	-	`sha256:ecbc5a18b7d46a2d3d718497054b3d4560ac10d49e528b06bce9c2b9564754f9`  
		Last Modified: Thu, 02 Oct 2025 12:38:15 GMT  
		Size: 5.3 MB (5308067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2986f0c7082ab237d5c332ffc4ddff008380c2ad7da28e52369c9ce0cec8f557`  
		Last Modified: Thu, 02 Oct 2025 12:38:15 GMT  
		Size: 15.9 KB (15876 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:aade7b598bd82fa1935937830a44263e0ffc5b81d9b3c04ff4389df905500b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231576509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43882a08e6a87617d6ea5cbec4a4c33b1703388d283a2e8785fb9a8d92e34c65`
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
	-	`sha256:93b0b88e50eb7468103e583a7be2e8ee3fe5f86e6c74df4baca40a3685b5eee1`  
		Last Modified: Mon, 29 Sep 2025 23:34:34 GMT  
		Size: 28.7 MB (28748427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902d5b8238c9c2eaaccf7f5fd1f022112689dea9268b37d68e55bf18b0e118c7`  
		Last Modified: Thu, 02 Oct 2025 07:55:32 GMT  
		Size: 143.5 MB (143542162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14b979948c661fe3c10124ea53e1c1f55d7c927852f1d75f1c5c62d0867dba1`  
		Last Modified: Thu, 02 Oct 2025 02:44:16 GMT  
		Size: 59.3 MB (59284884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6c6667431eecad0c5a411e614b10bd30cc4272e3d8f205410f991ec12f5282`  
		Last Modified: Thu, 02 Oct 2025 02:44:13 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197892170d12edeb89bf6284f01986cfbdc1ce49d2405324620c6aa036b71329`  
		Last Modified: Thu, 02 Oct 2025 02:44:13 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:29e7ec348166e8c68acaa23be739439a336b6098242cd913f88a4bd94f30e62f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5329796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6938e53ff23dacefde6d8c3a7751c798c481f11f1bca2b6ef6a683e0378e798`

```dockerfile
```

-	Layers:
	-	`sha256:b8d4352ba69437ce5d3ed547cd784f0a0a18bf73aaff0ad10d7cc303c546f845`  
		Last Modified: Thu, 02 Oct 2025 06:39:15 GMT  
		Size: 5.3 MB (5313799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e42e6c0c9692d2b2aac3f46fb64293098078769fa39ce0e6ad5345d5aea6312`  
		Last Modified: Thu, 02 Oct 2025 06:39:15 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
