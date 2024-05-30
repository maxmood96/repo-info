## `clojure:temurin-17-tools-deps-1.11.3.1456-bullseye`

```console
$ docker pull clojure@sha256:0911bf3ad632ee8a6a4a9264d79337fe8239018afcd154b2e8ae598886bd1314
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.11.3.1456-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:62af53b3a5a8c3db5d844a0562764fd3d8ee6063bbc52566872ba3e9ea7bf9f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (269011832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be96c550eb2b8faac411d7eec14b5a8de37d4845c8a35db644d1e58a642b7e3e`
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
	-	`sha256:88cda92c42c4b49ec5a611d32e97eea2875a4dfa4de24087c96f28ecb51d950a`  
		Last Modified: Wed, 29 May 2024 19:57:19 GMT  
		Size: 145.1 MB (145095043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e26fd023c77202c92add637a33026457cc789129e4f58e4a3e267241bec3e10`  
		Last Modified: Wed, 29 May 2024 19:57:18 GMT  
		Size: 68.8 MB (68816343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc809b4e747d64d0d30ba4ab033484c7e9b87fb6ada4c5a043be3b0682a34a0`  
		Last Modified: Wed, 29 May 2024 19:57:17 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f72f0a72577f9ea01003d57b67915ffe665d84eae0cb41b0f715ad2a113e4c`  
		Last Modified: Wed, 29 May 2024 19:57:17 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.11.3.1456-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:087a8901c1c65b896ac73ef92b0cd1a4ba7feb12abe99b848017104dba7910b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7015142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72e34fe2532c1b2790e732c3146d6828a3263e1810fad48b8ce2ef2d17f2c5f0`

```dockerfile
```

-	Layers:
	-	`sha256:1c5ead8d2b8acac753c3d68b7f90f43f92851919789812e89dba00e849c5a529`  
		Last Modified: Wed, 29 May 2024 19:57:17 GMT  
		Size: 7.0 MB (6999752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcb9bbd47f1573448254e84fd20594a0950d6dc6b3ed445f1fc15f57b9fa394e`  
		Last Modified: Wed, 29 May 2024 19:57:16 GMT  
		Size: 15.4 KB (15390 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.11.3.1456-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3a54e20be0110dc176ab501fedf4deb68edb0e60270a1d126c7dd7d98b036eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266562032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f452779fec99f607d50277eb81a2fd0aa2c4cec777d787a0415c8ec895d8e7d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:47 GMT
ADD file:43721c605da3f74f0c3f71384780fc0e57e2478b88197672caaf4baa3eddab23 in / 
# Tue, 14 May 2024 00:39:48 GMT
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
	-	`sha256:078d9526cc72763b2db16388f6b511c18a73e3e7f9d229364b3b85a6b5277bc8`  
		Last Modified: Tue, 14 May 2024 00:43:13 GMT  
		Size: 53.7 MB (53738990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0cca2e5711a3b07a756296cd3b6b27b79904360441fb0143165760f385fa7c`  
		Last Modified: Wed, 29 May 2024 21:40:29 GMT  
		Size: 143.9 MB (143892699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4de19facd8cc2718a521573a12502425b1e8934d850b6057f5b9d628b8898f2`  
		Last Modified: Wed, 29 May 2024 21:45:23 GMT  
		Size: 68.9 MB (68929297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7214ef492acfa194fcb1d21199bcaba625f806666c84462dd44e3650866f2dc`  
		Last Modified: Wed, 29 May 2024 21:45:19 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a548d2f2bea9d477aac1e882d9d7d3232f2413fe18b669f2e8717e050e10d7a`  
		Last Modified: Wed, 29 May 2024 21:45:19 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.11.3.1456-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:390b5635c3e17600122dec61ea44380c41b4152a14c86bb17518690a3fd8197a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7021400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2325045e7e478594d62f28bac03fa245a2b509b30eef09a21eb13f8d373ffda8`

```dockerfile
```

-	Layers:
	-	`sha256:16e2ce8cebdae5dd6f37f90825d89c2248e0b6c184c0f9201a33233f833e096f`  
		Last Modified: Wed, 29 May 2024 21:45:20 GMT  
		Size: 7.0 MB (7005474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ce0ea9637bbf127128d50789e554a7481f58f72b2387bd40a80c53e78602d0c`  
		Last Modified: Wed, 29 May 2024 21:45:19 GMT  
		Size: 15.9 KB (15926 bytes)  
		MIME: application/vnd.in-toto+json
