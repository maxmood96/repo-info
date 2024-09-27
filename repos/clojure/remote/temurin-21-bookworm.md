## `clojure:temurin-21-bookworm`

```console
$ docker pull clojure@sha256:71d68ee29c9cfd0fe61320dc8e1b1d358eaeda4f37a3cd8f25d52a93753a3851
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:208e131a5317b7f5a02b88463cd4709a96c8955a8ddbd75818a8cc0607e42b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 MB (289063366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52cdfb1002da92599a1ab6b1c055aa11b6e8702e86ea99bec7d1ff40d6be0aa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
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
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5bf511d386afafc6fea17dddf462d830c9957bb2229c2beca4baf7ce0fca0f4`  
		Last Modified: Fri, 27 Sep 2024 06:01:34 GMT  
		Size: 158.6 MB (158579257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb58b06016f40ab4e9624f1c1c0eb49948285a3e25b0159484a443e153e66e8a`  
		Last Modified: Fri, 27 Sep 2024 06:01:32 GMT  
		Size: 80.9 MB (80928020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319a4b361ced04f6f180d615dc4dbcdbff74aa2f503aae82402888b675b4cead`  
		Last Modified: Fri, 27 Sep 2024 06:01:29 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48aca2c271eb7fdb00d553b0e091de5c77b7d2129915c0bd8e63e1c70fafe0a`  
		Last Modified: Fri, 27 Sep 2024 06:01:29 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:48d4f3826769b55e7d33497fcfb148d3769c3464ffd4b49ae1385adf8cd82935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7179187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41db52d5909e6be548d295d4054bb9141b237f7c550e2fccf9e5bd141f2f6e7`

```dockerfile
```

-	Layers:
	-	`sha256:825a417d87ae3b4c5536c6fdfd7304beed26bd5882e8374794b3f1e10a0bf79e`  
		Last Modified: Fri, 27 Sep 2024 06:01:30 GMT  
		Size: 7.2 MB (7161747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8c947abf7202dbda8cd6fbc8f1c261990a8326559a4de20baf6e2a741a253eb`  
		Last Modified: Fri, 27 Sep 2024 06:01:29 GMT  
		Size: 17.4 KB (17440 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:023204290e1d0856c93981baa31eb7bb2d6bcf451e5ff8c06af00cef2ceccc05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287122503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b52f6588fc34c2e4ef19f5fd19708ad89b6ee4520c3871db61eb2c1f507f8d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
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
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff31a2ecf1dcdf70e2baa2a3c51395950289d2241e9e4f8269fe8f2d2c3c34ec`  
		Last Modified: Fri, 27 Sep 2024 10:14:42 GMT  
		Size: 156.7 MB (156746167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc23f75cf076c6f97e360f5e1f97fde246d73262dd935445900c1036854c485e`  
		Last Modified: Fri, 27 Sep 2024 10:43:05 GMT  
		Size: 80.8 MB (80790410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afaf3e48100d372afd3d96ca99d2f8a2e28e0943432cee3ecc2a2e27d1d1e4e0`  
		Last Modified: Fri, 27 Sep 2024 10:43:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0485d2a07a34d3610374f70d827c7726934d2ed5130df5bc23ccf67eadda81c9`  
		Last Modified: Fri, 27 Sep 2024 10:43:02 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a42646cd0fe6876128976485bb222180acb29e45e856475cd794182e08725dc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7185635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f33f1a9f69b67f34274b58bd293c86026927d9d457b361fab206196bb0cf45d`

```dockerfile
```

-	Layers:
	-	`sha256:d36f643b617e64c4e1a39324add66b966e9921618e9f8f9264591b8a2b2c8f7f`  
		Last Modified: Fri, 27 Sep 2024 10:43:03 GMT  
		Size: 7.2 MB (7167587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c2ac9d597bf0e027caf74020afcb0f6c5dc8b7846f0cecda387632a22a573f8`  
		Last Modified: Fri, 27 Sep 2024 10:43:02 GMT  
		Size: 18.0 KB (18048 bytes)  
		MIME: application/vnd.in-toto+json
