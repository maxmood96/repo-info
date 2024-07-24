## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:f26930273535539aefedb7a45cb6db5d519679ebab355c7281bfbd9b6b862149
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5184d77b4abd19951aa7730e111ffefd8123eda26742848b1aaaf2dbfa6cca96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.6 MB (235603436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31003f19087c30a3fb84e7071e00d55b99d2acdbad310aaaae4517798adeb8e5`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931fadb73c06ce2d1faf10311bb134d55e9ad7d0b7c5350f0955532da9dc4dc2`  
		Last Modified: Wed, 24 Jul 2024 03:04:24 GMT  
		Size: 145.6 MB (145550342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5d132048b461ea59b55e5ee673cc376fee4926e3a3f2d0e7fb64e018cbe288`  
		Last Modified: Wed, 24 Jul 2024 03:04:22 GMT  
		Size: 58.6 MB (58624118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9dca0912bfe709bd2a871b4c373b6a5240ccfda0f2481c0bf73a8b165150bc`  
		Last Modified: Wed, 24 Jul 2024 03:04:21 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c6a46b0ef12549e04504860ffa3a953bcef112321e312f44e8f794748ba7cf6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4963764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e39ecdc130d4997fe1878baa6f1be23aff3b616e9d20219b7d4ac89de27495`

```dockerfile
```

-	Layers:
	-	`sha256:eb3e9d4e086b3a1e3eb275f5209e16271767c9a177db5f5b5392a308c44369e6`  
		Last Modified: Wed, 24 Jul 2024 03:04:21 GMT  
		Size: 4.9 MB (4949826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec58af327de2eda292802f6437c048583f391855dce520a554019c5544590f1b`  
		Last Modified: Wed, 24 Jul 2024 03:04:21 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ea6dc38b4980ba55ffaa18a525808ff33025800aaa63aefc8e41fdb7890bddab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231124881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f9305857004a2e65276285f60dff258500a76b9fdca3191d720270d13740c10`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244e69a54f15f458626b6756d260ecbd32672feb26382680eb1a61f78d77cbb7`  
		Last Modified: Tue, 23 Jul 2024 12:18:47 GMT  
		Size: 142.3 MB (142304049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bc0d850f5720c415196196d0eca6cf6e659c0f5e7df6593b36df02e51ba434`  
		Last Modified: Tue, 23 Jul 2024 12:24:11 GMT  
		Size: 58.7 MB (58744105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f656226486953291c8c19a04138654de90506e8851abd86ab1cff160a3fddff6`  
		Last Modified: Tue, 23 Jul 2024 12:24:09 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6eeded183e79a3a513ed0b2fa4535bbcb8ff765ea94cee059d3d28c27639ad29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4970660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b6faf35041abd48672f37aef6bee8ed698dd2fc7423c07c020038472313804`

```dockerfile
```

-	Layers:
	-	`sha256:654c21f546ca41b04f279c60e262c5536b3fc785de8f429649a09bc76fa3130b`  
		Last Modified: Tue, 23 Jul 2024 12:24:10 GMT  
		Size: 5.0 MB (4956182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1c1d4d1d0e40177e66dae796f92b9c5194eb1aec1fb77bfe9c252395462198b`  
		Last Modified: Tue, 23 Jul 2024 12:24:10 GMT  
		Size: 14.5 KB (14478 bytes)  
		MIME: application/vnd.in-toto+json
