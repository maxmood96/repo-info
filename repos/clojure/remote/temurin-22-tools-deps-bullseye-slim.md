## `clojure:temurin-22-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:b495ce5a4e60febeb91779c17bd777bed4f7560b5ed851b23589c231442aa08e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a24462e0988b30aa9dd22d7cd0a75272f68fef117d495a5416094bf3a2af3f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246851267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b6dd56b2ba239db5c405603fe02e5c3af3ef03a22c65d41c5bb083bae8c407e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8055ee09ed0a60659ef48cfee9c056a15b9ef01b0e0d80c1716d1fc740e7d2d`  
		Last Modified: Fri, 27 Sep 2024 06:01:40 GMT  
		Size: 156.5 MB (156481594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b53b2833b9b77f9b6fa667ed78a6eb78f26ab44b7d5a3d7f1c54bd6669e8f5`  
		Last Modified: Fri, 27 Sep 2024 06:01:38 GMT  
		Size: 58.9 MB (58940036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e5eb7a01eaa7a029dcf6997ba0627f8d3bb8d262c97fdba4d7860e1750d8c0`  
		Last Modified: Fri, 27 Sep 2024 06:01:36 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a40211d0c5d017a89e157714c782b0f848716031e0466f33013f15849bd2e0`  
		Last Modified: Fri, 27 Sep 2024 06:01:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:38d43415d3cc1f393ead03fa7462f1c45ea6abfa35326b44b91ef466c28feb4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5118665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4dfe2486295f738e9326a2ff42e732320045e44f0f6c7e99eedbcc202c3627d`

```dockerfile
```

-	Layers:
	-	`sha256:1fe05d58c21207d69e0531204ded67a6800b727114aea18f6722c58d6c16ce62`  
		Last Modified: Fri, 27 Sep 2024 06:01:36 GMT  
		Size: 5.1 MB (5103152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd0fd9d1b7cab4c995d210128b3a9c7ac486f82f1066fde28be20b3b36296d9e`  
		Last Modified: Fri, 27 Sep 2024 06:01:36 GMT  
		Size: 15.5 KB (15513 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:16bff10c9fa67c2ebbeda24d4fe377034403a50259c65dbfadb4331955b318eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243652367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:902bff369a4339aecc214920244541573b2b0ecec79b2eff99f38f15c7ae3310`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f625c4783c842cd66e3191d86a916b00ac78f74108e9968634e3c785f5db36`  
		Last Modified: Fri, 27 Sep 2024 10:49:37 GMT  
		Size: 154.5 MB (154503748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d35a2fbc0900365dc1f46d681ad9346623aa5cc06e829e88eccc3d3d9d983c`  
		Last Modified: Fri, 27 Sep 2024 10:52:57 GMT  
		Size: 59.1 MB (59072423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2391e9349fdca3eaa7ce63876f7b206165da107a1851dbdc14f1216c2cfd2012`  
		Last Modified: Fri, 27 Sep 2024 10:52:54 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c12149bc5628d2585d08f7a3d3ca6976080e80005073739beae7dea1ceafac`  
		Last Modified: Fri, 27 Sep 2024 10:52:54 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:925c289d7ea529f74cfb8a303cd9ed4e4f9f976995b1a51bf3bba32a9701da79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5124320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a78eb69a5acd92172838f6af4348d66d453324858b24cde324eecf5901e442`

```dockerfile
```

-	Layers:
	-	`sha256:4c9f79646b57acd55775b0f0628cf8b212694cb9e0ce222d2a88d2f7b416d86e`  
		Last Modified: Fri, 27 Sep 2024 10:52:55 GMT  
		Size: 5.1 MB (5108267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16216ecc6d0e24aece9658f8ca397f8d19563c9d115d459fd38158712f812e6a`  
		Last Modified: Fri, 27 Sep 2024 10:52:54 GMT  
		Size: 16.1 KB (16053 bytes)  
		MIME: application/vnd.in-toto+json
