## `clojure:temurin-8-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:e674f8c189491c1a69b42e5199154242b320146a28b5cda4d4a25cb83f7e881b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:177df6cb0be54217c34e2e01b91dc3bdca3b6a58d382e1eefa930497b055ecf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.0 MB (178047158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d8a1d4cf20bc340c9c2e90a23f1590a75dc284a5cae55aab34f60ed2d429e89`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 03:19:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:19:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:19:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:19:45 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:19:45 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:21:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:21:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:21:09 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fccfc62cb15165379a658b98df1680b95e3908f69adc8e7176a095a7b4cf2106`  
		Last Modified: Tue, 13 Jan 2026 00:41:36 GMT  
		Size: 53.8 MB (53756446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1729c6df4936598ac07b8ee907198f1ee33502d4f6e850e5be5bcf6ed0306b`  
		Last Modified: Tue, 13 Jan 2026 03:20:25 GMT  
		Size: 54.7 MB (54733371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bf0c2db632a6f75a1cd329277d79aa5c99f9b9520d33962ce7dd1075dab083`  
		Last Modified: Tue, 13 Jan 2026 03:21:39 GMT  
		Size: 69.6 MB (69556697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3929eea70d79f2b2539255fd2ea5ccc3441652dc3fc390cd4dc9e70d638e996`  
		Last Modified: Tue, 13 Jan 2026 03:21:32 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d607eefc16391ec56c3fcfdd6625c3006ae311e451304540f57a378e558e98ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7531471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef6425293dc7f6a781c2e582fcd8546ed456d18c6c108650769fd24d0939fa9d`

```dockerfile
```

-	Layers:
	-	`sha256:8a4d8cfeac693696cbfb02e8d5c987439a30009907b8126a3902ffaf581a2391`  
		Last Modified: Tue, 13 Jan 2026 07:47:50 GMT  
		Size: 7.5 MB (7517277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b085e11e00b6c7732385f99ddb64a44277e9e6b7372738de8afd0923ec556d5`  
		Last Modified: Tue, 13 Jan 2026 07:47:51 GMT  
		Size: 14.2 KB (14194 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:46102272ea13c94d03877f611aa963241852471bbb015d7fc2523247a89ad0de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.8 MB (175760347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd17ff848761ef283ae17f573e4ae94a3139359dcbe4678201a3b7a7960bcab5`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 03:28:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:28:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:28:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:28:29 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:28:29 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:28:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:28:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:28:44 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:52 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ffdd8ad494b6e18d663f0d2488237c3af168797d1d0ced40f1b4126fdcc424b`  
		Last Modified: Tue, 13 Jan 2026 03:29:14 GMT  
		Size: 53.8 MB (53814993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd2f67ae0f4e2d257bf2447d9b0569f7969470991c8622635ca2e2b794d7330`  
		Last Modified: Tue, 13 Jan 2026 03:29:15 GMT  
		Size: 69.7 MB (69686940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8b53c0bed86b62cfe37a02f1fe81d79c98e07e518d963bd3bf6cc15a2324fe`  
		Last Modified: Tue, 13 Jan 2026 03:29:08 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3644a9b1a68eb930c2369a395feee9309dfbe6f5558506c9ddc936c8a1342c7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7537386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921e467e57572b81e240fcf1d7dacbe9e0d83d79b3ca02850e7d6931d299b3c3`

```dockerfile
```

-	Layers:
	-	`sha256:e6170a681478755547ed027420b653428dbcdf29a72e66dea8da64f98d100e0f`  
		Last Modified: Tue, 13 Jan 2026 07:47:58 GMT  
		Size: 7.5 MB (7523074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3794a37322efdd18ccdc595f06291d5abb083c6b3e1a47286e31d5461f21f30d`  
		Last Modified: Tue, 13 Jan 2026 07:47:59 GMT  
		Size: 14.3 KB (14312 bytes)  
		MIME: application/vnd.in-toto+json
