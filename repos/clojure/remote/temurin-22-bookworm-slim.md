## `clojure:temurin-22-bookworm-slim`

```console
$ docker pull clojure@sha256:69a20f0a57b6f56e2172cd4f068534687a03bed6bd2c0a0737a27b5a3887fa41
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:913f1891c238da9067ae332755f329691ba1b7bf6fbdffd3d7d6f742328abee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.7 MB (254676164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7503541d94ffa9cf0b9adb5aa8bdc58dec3a196796dba858d69fdf255a6ae0c3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac8c73f1cedc60c4faef387182b05c1c58630284d759a2639d6c464f80b9176`  
		Last Modified: Wed, 24 Jul 2024 03:04:43 GMT  
		Size: 156.5 MB (156481594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7ab26121abef29db50c5d43554a6cd3a944ec700a6834ac15d0a0717a36bb7`  
		Last Modified: Wed, 24 Jul 2024 03:04:41 GMT  
		Size: 69.1 MB (69067240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8376b042ccda21da82a70e78330e73056f044dd40946d9288cb90d04d30d87`  
		Last Modified: Wed, 24 Jul 2024 03:04:39 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae818bb3055a0b4a2f0ab5f70cb7ba2f0a52b8e8882816fdb415ee76ad251ab`  
		Last Modified: Wed, 24 Jul 2024 03:04:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:85735d7087edc349740d48e43b72ad8ae5ddde89c7fcb225e72d4abe5018ed30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4760671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d06ffdb6868c1cd1613ada8cd8473cc4093cb8f4e05f3cbabf685192697456b4`

```dockerfile
```

-	Layers:
	-	`sha256:d2420deb0872567ace3b20e915ea601e583797c608737d611bd2a5b287e6002b`  
		Last Modified: Wed, 24 Jul 2024 03:04:39 GMT  
		Size: 4.7 MB (4745158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8ec283ab6f43e078cc44944e138d63ac1dedf0eec518f224b9fbd40ba900af4`  
		Last Modified: Wed, 24 Jul 2024 03:04:39 GMT  
		Size: 15.5 KB (15513 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:724b5def494328402597b1ef0fa9c370c52985ce3bfc1caafec6a2f1a88fa88c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.7 MB (252713601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c8d22d5e6e23af246595de6022f36027addebfd82811362bf515502b9be9530`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a45b65ee7760733c6d0e2844a91cc6dd770e36853341760b7c7cab214abe251`  
		Last Modified: Tue, 23 Jul 2024 12:54:46 GMT  
		Size: 154.7 MB (154738009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d10fa49df72bd5088015c44d54b6b9e09f39af6300557d8d17422d1e5084c9`  
		Last Modified: Tue, 23 Jul 2024 13:01:33 GMT  
		Size: 68.8 MB (68817980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12879d6a0f1bc44c0d4de2b811350936d874f458a56f2d8e5f7c945b8823da04`  
		Last Modified: Tue, 23 Jul 2024 13:01:31 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b05825304be42dad88d2f8815a11304f332e403510ed7d3af4baee183ef38c5`  
		Last Modified: Tue, 23 Jul 2024 13:01:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cbb1d11233dd34c11508382563758e8725b8cc21c830c6cf1e07ed8ab544253d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4767596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f06860566b95c40655dd1a4a16c723ed21974037a2a4db729f5e4014d02ea04`

```dockerfile
```

-	Layers:
	-	`sha256:0c5196e668a79c7fac2741c6a30e984cce7deab1e0b722b79f5cb0f98d72a9c0`  
		Last Modified: Tue, 23 Jul 2024 13:01:32 GMT  
		Size: 4.8 MB (4751543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e48df2ba33e3a0e16f33ee96a23c375dff424901fc6932eed3e5ad3f5998fa5`  
		Last Modified: Tue, 23 Jul 2024 13:01:31 GMT  
		Size: 16.1 KB (16053 bytes)  
		MIME: application/vnd.in-toto+json
