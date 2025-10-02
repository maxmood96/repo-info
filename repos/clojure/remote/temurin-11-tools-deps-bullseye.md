## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:e5bff48752c6feb100bff347f085564093e0dd7253bc36bc1bf9ba76ecb83a0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:467b21062e1e495c6f58c961b68250e90147e87b5f14b2424b7c2cc426f69b6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268974690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f915e5761d0e97c365bdfdc3120c438745ede6b7f35ac5b703b616827421fd`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:10ffc47270cd106d2d04bc7ef4749d579620e45a84804ba3b18f0898fe5ecc64`  
		Last Modified: Mon, 29 Sep 2025 23:35:07 GMT  
		Size: 53.8 MB (53756064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c95dccd09a097f11bc9c7cd183a6e0f3e04340d2c9132646610471084e2a1b7`  
		Last Modified: Thu, 02 Oct 2025 01:58:28 GMT  
		Size: 145.7 MB (145658240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ea1c3e827e88c65f798b9ebdcf53571382ecb2f62455d4bce858ac017f80b6`  
		Last Modified: Tue, 30 Sep 2025 00:53:14 GMT  
		Size: 69.6 MB (69559742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552f7c20a6af0c84570a402f1448e7ab0b5db24d02ead480281a4a835686a23a`  
		Last Modified: Tue, 30 Sep 2025 00:53:05 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:851d49d021c3e244d2703d972bb325e3d2cb19ed4167559df9c37fda48eed3be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7429259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:517ea4df42111331d39ce6f67b089f0e52f3e8da9cccca7a301d96e09e54e22f`

```dockerfile
```

-	Layers:
	-	`sha256:10607c3cad232527f8ad4d322a507bd10e7d63a7375afb5899663a7322509975`  
		Last Modified: Wed, 01 Oct 2025 15:35:26 GMT  
		Size: 7.4 MB (7415808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fc099a8a17135d1abb47e19a831eecfa3dc1192365cb4fc20c80fb1d0693d1f`  
		Last Modified: Wed, 01 Oct 2025 15:35:27 GMT  
		Size: 13.5 KB (13451 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ae81df26061ca5e4ae29a8d2acc2546911002451e355e1648970009d8bcc7d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.4 MB (264403400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d731363aed5d9f48d3b8d69d40fa3e6f6cee8fb5b047567784a30f86e3da31a0`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:9b16ae1bbd1ada84c12528379a10e280bd89e0d0332670c8487145eb77fe2fe1`  
		Last Modified: Mon, 29 Sep 2025 23:34:42 GMT  
		Size: 52.3 MB (52257414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041aa23cd45898d78616e7dd61fc8d86d6d516f40034a113caa0c0961fe7f8c0`  
		Last Modified: Thu, 02 Oct 2025 02:42:13 GMT  
		Size: 142.5 MB (142458701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e72c8838e8dfabfa74bc1f6310ca01983a4475f2f022b6a6712e9dfac1b8a0d`  
		Last Modified: Thu, 02 Oct 2025 02:42:26 GMT  
		Size: 69.7 MB (69686641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8493a659356194abd17565729cf37548e26b1b6fe40cd42fa4f50b86a106b4d3`  
		Last Modified: Thu, 02 Oct 2025 02:42:17 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d212b70450ba36c5c74aafe51953e376cb99aa646f688b078739f6d2a3483770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd8ed02e25ee49ac9c1a296c4bfd873d30867a7a144b9be3155a54e1b59e5dec`

```dockerfile
```

-	Layers:
	-	`sha256:12f0a7cbce6615b971cb38904c270a8f0d375573c9800836f969fc37d6a25a35`  
		Last Modified: Thu, 02 Oct 2025 06:35:58 GMT  
		Size: 7.4 MB (7421525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc275f37325d3e4b2420e299adab4869d4b39d8255170fe513808a1d0e27555a`  
		Last Modified: Thu, 02 Oct 2025 06:35:59 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
