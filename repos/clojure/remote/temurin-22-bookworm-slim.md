## `clojure:temurin-22-bookworm-slim`

```console
$ docker pull clojure@sha256:50480e6c143d1e998ab2ede9f6891ef3f1370408da2f02830099c3c64d7d0819
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f4ad3ec4bfafeee6bce0e9bad644bd3eda69f9d5bad23c0c7bccf17293a05dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.6 MB (254632970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861a1ba20e408d901c6ab8441e50651d64dc55f6819e2ec605b4a39a394955e4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855dfeb5f912c85fec6c98d073fd1e2669b3058036bb1b93f263e369fe55f563`  
		Last Modified: Sat, 17 Aug 2024 02:04:29 GMT  
		Size: 156.5 MB (156481638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa9fa3c8e06a681280dc19853466156ea1dbe8ca4630aa2bdf05b9db652aafc`  
		Last Modified: Sat, 17 Aug 2024 02:04:28 GMT  
		Size: 69.0 MB (69024060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ff53633d96b0d85fc4d588c9d48a9762e95332e3f7fac9e443ee2569fdac5a`  
		Last Modified: Sat, 17 Aug 2024 02:04:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd94a039ef26c7bfad13abc75f7e2c52d750ec794c4a9e4929380836fde0a661`  
		Last Modified: Sat, 17 Aug 2024 02:04:27 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d07d53476804bcb553b084fb29da845d6ebb940065062c00b8d42d48f06857f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4760671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e22d09e42b22486267fbd3ed04d9710ce6b31f9b7bf624ceab22b6813f0a8238`

```dockerfile
```

-	Layers:
	-	`sha256:aa8a96da3be2d5286631ea43714523b08593c8d3c56559319e2882b560cc6312`  
		Last Modified: Sat, 17 Aug 2024 02:04:27 GMT  
		Size: 4.7 MB (4745158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b868f1d1ffb5d8d56111a65f0c8624f8db37c18f0317b22d97b2f4601c1a73a`  
		Last Modified: Sat, 17 Aug 2024 02:04:27 GMT  
		Size: 15.5 KB (15513 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:aebdbd81e0ebab18462895e8f05f64d7e2baba418d98d7673ff3598b775aed8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.4 MB (252434232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e87ea4022778ce8a6616bffd6f545af1083e488ef836f26007b5044e7e40c1a6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c142b38ffcbff18bde51f24b46783a56c2e920d03361ae340f0228c6870b66`  
		Last Modified: Tue, 13 Aug 2024 06:45:30 GMT  
		Size: 154.5 MB (154503733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99fe304648c3b55453bd96ac8c2417dd9c4a8c2be7abf0f8ffbf22fe540d44a7`  
		Last Modified: Tue, 13 Aug 2024 06:48:56 GMT  
		Size: 68.8 MB (68772933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2946c53673f0b1deb6fa7a18ce4dfd128a457f325b80b4a49235ef37284516aa`  
		Last Modified: Tue, 13 Aug 2024 06:48:54 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51f9ed17817513771682ce865c422be5520f5c3b69b23d1ca63012fd4b7db76`  
		Last Modified: Tue, 13 Aug 2024 06:48:53 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7e23975f9c68479fc10f5f416a3ed7c29627aaeee973f6b2e18420efdbcc80e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4767597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:922f7b6be4af23a91989a36f8765f7d3be22a476d2b8e23086ed40d76e4669cb`

```dockerfile
```

-	Layers:
	-	`sha256:ecfb9f248a8b9cf1e9688cb0b7a23e886b2cd0be6d7af331cfc7f0bb1c989ec1`  
		Last Modified: Tue, 13 Aug 2024 06:48:54 GMT  
		Size: 4.8 MB (4751543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dff254810768d3c9522b05d382cfad0858987329e0994863dbc8eb23eb472ebf`  
		Last Modified: Tue, 13 Aug 2024 06:48:53 GMT  
		Size: 16.1 KB (16054 bytes)  
		MIME: application/vnd.in-toto+json
