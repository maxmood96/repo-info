## `clojure:temurin-22-tools-deps-1.11.3.1456-bullseye`

```console
$ docker pull clojure@sha256:b68602907202d121de07dca09a73091bfa75196ab40088f1cf4c4aaf484124a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-1.11.3.1456-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:8ccdd8e2fae06ea2e6aecf2a91f2c2de0c767c0762909286d2d485bee397fcaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280818594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d385768eab6576cbdd3b072a250b4f189f74b8cbda81af4e2ea7f519e6a4e36b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
# Tue, 28 May 2024 15:17:11 GMT
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
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9b49e3297756454d586fb96eec8f11b6d3012651c202b52e4a51f11b786528`  
		Last Modified: Tue, 02 Jul 2024 03:03:02 GMT  
		Size: 156.7 MB (156715523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:854a84095df2ae6d9fc88ff691fb95fea443c5b0f89b7dfde85c4266073efcea`  
		Last Modified: Tue, 02 Jul 2024 03:03:05 GMT  
		Size: 69.0 MB (69020674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca2023e334e06bb9482268eb060876212bab92859cc6efb9adf41a280b61506`  
		Last Modified: Tue, 02 Jul 2024 03:03:04 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421785d821716cf19f32ac3fbfda85a3db6c93efd9e190d88d1c2fdc9e044b22`  
		Last Modified: Tue, 02 Jul 2024 03:03:04 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.11.3.1456-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:743b024709579502ceffe4d3e578ececd6dd02eb87fc0620cceec1115dd4e529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7015222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a0ba4fb2b406504b0410c0d7011c9f44dd21c9d56cbeb91b527a844ab86200`

```dockerfile
```

-	Layers:
	-	`sha256:f522fcee4df09b9ef2cb6560fbe4ff228b024e9a9fee6b7d8b818cd964a11882`  
		Last Modified: Tue, 02 Jul 2024 03:03:04 GMT  
		Size: 7.0 MB (6999784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8dc3fc779589218fa3639c8bc7d6c5675ffb5c8aceb94d2202a219cbfa97c2a`  
		Last Modified: Tue, 02 Jul 2024 03:03:04 GMT  
		Size: 15.4 KB (15438 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps-1.11.3.1456-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:69ac6dd673c6cdac6784807c1ce6adeea8ff9e4998599b08b0836a16f03a94ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.4 MB (277407675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c51f03b70dda7dbc7a5cfff3efed017a7bbf5edf37dc924291248dc8f03d43a7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:cd3edc79f93d09aa5daffba99cc698c3fe0e02348e8dc284ef466b7e6596e68c in / 
# Tue, 28 May 2024 15:17:11 GMT
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
	-	`sha256:f975e52008de385eb513258b4912477b214cddf1c8e87877f85028d940bfcdae`  
		Last Modified: Thu, 13 Jun 2024 00:43:32 GMT  
		Size: 53.7 MB (53739581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d963a96394e2a9f4df474372727ed0b58c4b095d7c668d6d92d142be8c953f6a`  
		Last Modified: Thu, 13 Jun 2024 12:01:27 GMT  
		Size: 154.7 MB (154738000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2326b0c8327e1c12f1d945ce82bdfc15a6a63ec380d731fbd8bd97eac0ecc17a`  
		Last Modified: Thu, 13 Jun 2024 12:04:48 GMT  
		Size: 68.9 MB (68929046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cebc58e1f7350a38d4948317a9ead896de7164e1a067d7749231196af56ba52a`  
		Last Modified: Thu, 13 Jun 2024 12:04:46 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75600f3cbe00f39734bca9007d468e47515e0fd217ffce6a600535efc0284e8`  
		Last Modified: Thu, 13 Jun 2024 12:04:46 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.11.3.1456-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c3b1c49ea70e0d0b3ee3d4617c2ddf5ab41b30401fe63d49fa32ca7e5f0978f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7021442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b32164dd92e21ffd462033307c7417d1e222d47e8572b6c060f43fedcb3b6fa1`

```dockerfile
```

-	Layers:
	-	`sha256:8a522f64a78a9681f717e9702d51a9fa56e35c296cf45b7f3e4f54716e935f74`  
		Last Modified: Thu, 13 Jun 2024 12:04:46 GMT  
		Size: 7.0 MB (7005467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87f433b709a9900fbc8ebcfe5628182f81d489ccbaa3724212312d7f7d4fd7ee`  
		Last Modified: Thu, 13 Jun 2024 12:04:46 GMT  
		Size: 16.0 KB (15975 bytes)  
		MIME: application/vnd.in-toto+json
