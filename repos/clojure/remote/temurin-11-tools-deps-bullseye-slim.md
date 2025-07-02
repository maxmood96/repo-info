## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:cd4378114d35e7c3c8575a9f9dc31087410be42c0f976ddfec953234c30a78e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:69e10f0906c22d01a9e85f8efd210241911c190fc2176837d4720ff0bb1f9de0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234898020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d515c4b478881f1219c29452ae6da30c8a92957c416f57b3e30f297769f12c`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c75ba428ad6db3248a0423d8d1cde7b29b14fb5ae82fc6db855d0144700c8e5`  
		Last Modified: Wed, 02 Jul 2025 14:49:42 GMT  
		Size: 145.6 MB (145635731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586205ca21fd5c042a3345b93c6d869c16259b2e14b6f838fbf72e902c35c77b`  
		Last Modified: Wed, 02 Jul 2025 14:49:37 GMT  
		Size: 59.0 MB (59005597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a57d08f7d45c64642d8ef7c6b6b8286289f4fd56dbc431bc0c5b9dcf0991b1`  
		Last Modified: Wed, 02 Jul 2025 14:49:30 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:325509b138dd42a4d881e03757c11093adfc71d2403b74319b40738cfb2fc777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5342488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce76020b4d38479ec250d0ad755a92755bc6b229ce149ec6568daf2655ae8b4`

```dockerfile
```

-	Layers:
	-	`sha256:3eef4708d8a1366717f58d3c2ee132088f697177bb62548e097810c13e39dd82`  
		Last Modified: Wed, 02 Jul 2025 06:35:20 GMT  
		Size: 5.3 MB (5328179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfa529aad60f5fd24a6a6e5a04431a6f666e808899134ee040e228e7e0098a51`  
		Last Modified: Wed, 02 Jul 2025 06:35:21 GMT  
		Size: 14.3 KB (14309 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7a97cfe86fd788efdeddfa377cb7da9f70e2833bf26a9e4db505659219b33d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230303254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fb419369d4b29fb5244079aa72289f321002d9849054728481c4a5b8c2550a`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:00ce3d02ade4a2c8e5e37b1a218bb5c24c995bd8757095b89316c42854286fe8`  
		Last Modified: Tue, 01 Jul 2025 01:15:35 GMT  
		Size: 28.7 MB (28744140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd3a9e6918453f2c489bf587b46ba0d4ae0d4119e108c41f5aaf2474444f623`  
		Last Modified: Wed, 02 Jul 2025 11:44:55 GMT  
		Size: 142.4 MB (142420682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28d095c45113e5b145c8d09d305b3cf5c45c921f593d6cbe388fa8a11408e59`  
		Last Modified: Wed, 02 Jul 2025 12:25:48 GMT  
		Size: 59.1 MB (59137787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebffa2b8f3ec6c37ff1fa5cc68195356d14e071c8911fed3ba719a4eab05b61c`  
		Last Modified: Wed, 02 Jul 2025 12:25:44 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3e850fac164e09f9d85c34800ce9cb680f992f862fd95039827ca291bd7d23ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5348957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d4c4b2048ca8d71ca8b3a89c29dbe3edcc150cdab4b274f8400f677f9fc7b2c`

```dockerfile
```

-	Layers:
	-	`sha256:fe3cccc1d430112e2c629bdcabcaeadd8557194012ce985698bafc508ae8b8df`  
		Last Modified: Wed, 02 Jul 2025 15:35:20 GMT  
		Size: 5.3 MB (5334529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdc5d60e5a2034504fe28defc0fd431faf4022ae52c53cc5e5ffb0545c94124f`  
		Last Modified: Wed, 02 Jul 2025 15:35:21 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
