## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:2dc35e61f1214025a77ca62105166055778f9669a4925676737a49828aa6fcf3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:23a734b66ea5e2c4770afb04ac05edc6792fc1c24a23e138ab0716d98114a106
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.4 MB (234377575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:362e34b975a3377e15296597bfed0cf5832657033fe6ab5c57abafd797e854b6`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:51:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:51:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:51:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:51:28 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:51:28 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:51:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:51:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:51:42 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a88499d92e58a9f7d74dc939bd949d9c2d87abbbaaec03b5f87553e69d901a53`  
		Last Modified: Mon, 08 Dec 2025 22:17:50 GMT  
		Size: 30.3 MB (30258465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225a45c008a4366acd98661da5586d3315469d52d8cba59c271bad4ce59d0425`  
		Last Modified: Mon, 08 Dec 2025 23:52:21 GMT  
		Size: 145.0 MB (144966626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bba2f8eb0b6a68b03af8848ab51709d6344110d911baf51bcf3165696613c83`  
		Last Modified: Mon, 08 Dec 2025 23:52:12 GMT  
		Size: 59.2 MB (59151840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b85174d92206e6a465d85bdd2c1b0006d5b949e2d7df8f812dbb29ad968bf69`  
		Last Modified: Mon, 08 Dec 2025 23:52:06 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6044d27d01bf5d23b251f17936a5de05d0237baa0508a5593b302953663d2c5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5342475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8374bdda73dc3e4a8fa5652f6220b82435c0d042906c80565f05b54dcf8a2f05`

```dockerfile
```

-	Layers:
	-	`sha256:20588a6dc9d61dd869f697e0065c82880ed2e9c7578a111dd10b93870400282c`  
		Last Modified: Tue, 09 Dec 2025 04:36:32 GMT  
		Size: 5.3 MB (5328208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:562d71b924ec0e223dbdd5d594333ed3a32f2ffa0ae847c1c790f84105787066`  
		Last Modified: Tue, 09 Dec 2025 04:36:33 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6c52ec0799b6cbc057236f850230c9624d8e36b057368b63b2fe85b57ae94293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229768243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eddb1644177e436cfa0369ea88e86927da2a56442bedb1a3f9d7426c13f1faeb`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Tue, 09 Dec 2025 00:00:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 00:00:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 00:00:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:00:05 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 00:00:05 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 00:00:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 00:00:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 00:00:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7d43510e20279c4831f5ca1d424a1d56c6c24251d7c93288a50a066dc7e72bda`  
		Last Modified: Mon, 08 Dec 2025 22:16:06 GMT  
		Size: 28.7 MB (28748482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f733bd8ff8b7484e55d9150818c7e5b622c213b0b77729fef738322537e05bb6`  
		Last Modified: Tue, 09 Dec 2025 00:01:07 GMT  
		Size: 141.7 MB (141731500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365f489f6be55cca6855fecaacf9f0eca4bfa54e77555b60b65b6fcaf027426b`  
		Last Modified: Tue, 09 Dec 2025 00:00:49 GMT  
		Size: 59.3 MB (59287615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2bcb6429c6d20bd61090136babe73543a246a04dc45013d4968b19babd3564`  
		Last Modified: Tue, 09 Dec 2025 00:00:46 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b5023c339b317a728eae1be7cfefdb6eaea6d2821d21cf816ec62b1d28dbad6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5348943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b31db829a344806053282e31eda17b0c6d7bff29336466c048e1053b7d4a7be`

```dockerfile
```

-	Layers:
	-	`sha256:e3fce239ec563d39c428af72c52fc494bb583199f028702871fcfb456a2e4335`  
		Last Modified: Tue, 09 Dec 2025 04:36:40 GMT  
		Size: 5.3 MB (5334558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c2783b9cd4c867f4d2ccc3a82267bb752823d1ccea05a6844d9f0f94d465a55`  
		Last Modified: Tue, 09 Dec 2025 04:36:41 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json
