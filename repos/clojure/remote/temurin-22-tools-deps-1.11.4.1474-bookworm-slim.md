## `clojure:temurin-22-tools-deps-1.11.4.1474-bookworm-slim`

```console
$ docker pull clojure@sha256:730c3879df25f24a7e60d30b73777485f953a00ea3fd8bb33b4d3b78f33443ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-1.11.4.1474-bookworm-slim` - linux; amd64

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

### `clojure:temurin-22-tools-deps-1.11.4.1474-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-22-tools-deps-1.11.4.1474-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:19f285f7c95ef3e03d8d75f034ac759e7a5a59f4de3896b9e935337ec8bc2f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.4 MB (252434651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb426b54ed9160d456e322b33355c896395bdb7a5178005e549364ff6000c6fe`
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
	-	`sha256:6d1fb39c7baa693f1d90f06cdeb26f0916fed34db00c7e3c5e300abff9ca8690`  
		Last Modified: Sat, 17 Aug 2024 06:34:13 GMT  
		Size: 154.5 MB (154503738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e0c5bad4f6a5197bd76067ae47de16ff6d88cfd4f9b49e287c3898be4159df`  
		Last Modified: Sat, 17 Aug 2024 06:39:48 GMT  
		Size: 68.8 MB (68773341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf1f66a817cda42f89e73084e50a30883f217a0974781a5e7a510aecaf523fe`  
		Last Modified: Sat, 17 Aug 2024 06:39:46 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025c5ed36db311b4e99890b31d747147558d0d3a4bb5f3c87c5c802fd6c159b6`  
		Last Modified: Sat, 17 Aug 2024 06:39:46 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.11.4.1474-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7cf9967c36ca0b96d6ad75b1ada4ad9ac05379ba9937af3373f64e0241f6c24e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4767596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f36c8031af70104de240fa71154c2526555abef671b6c56e4deefc326d47f65`

```dockerfile
```

-	Layers:
	-	`sha256:15711dfdb46f42fa8eb06870f3ba4d4853652adf8eefaab6b8bbaa3a63037666`  
		Last Modified: Sat, 17 Aug 2024 06:39:46 GMT  
		Size: 4.8 MB (4751543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0a97272e8538abb9a94202f079dc4181a771a8be0edce1ecad36b513bbc1406`  
		Last Modified: Sat, 17 Aug 2024 06:39:46 GMT  
		Size: 16.1 KB (16053 bytes)  
		MIME: application/vnd.in-toto+json
