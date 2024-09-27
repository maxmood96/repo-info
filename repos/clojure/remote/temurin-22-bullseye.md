## `clojure:temurin-22-bullseye`

```console
$ docker pull clojure@sha256:9946e1cec25552c52e57fbb683b8377122bc9bc64eb705a9e0ace8234aa6e541
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e83324ace01634f5c7b523bf0b2756b7110d38f236d10999d937838cad4f85b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.9 MB (280897958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e54fe789effd6398c67ef1657a8c80f916ad1a74b33e285d5f4d0e16817d3f4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
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
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9510cad887429d76a34bf65ff9a8e53e5ffd81a44f912f6440ae196f0da7c210`  
		Last Modified: Fri, 27 Sep 2024 06:01:36 GMT  
		Size: 156.5 MB (156481620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f89e8973394ecdee6ef38bdd309bb4a83d6d5b8ccf7b4a7fd4f059f4fbbee7`  
		Last Modified: Fri, 27 Sep 2024 06:01:35 GMT  
		Size: 69.3 MB (69333908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5ed301575553d0dc27a939f6ba546b637d12c74d1b5db734cb5139114e185b`  
		Last Modified: Fri, 27 Sep 2024 06:01:32 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6c685e0a370017bcff2beedb29b2d5a3d78566355397544485899ffca6a4fd`  
		Last Modified: Fri, 27 Sep 2024 06:01:32 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:9b20931ac12ad6aac9ea52c8799f2c605e8f79b586dfe4c09533f58ab53943fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7209110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc5473c19abeb2b370908784d79bc9ee5cd38a89927808e1c9cbabb881ad07c`

```dockerfile
```

-	Layers:
	-	`sha256:2b74a1d5e85f56828cef2cb25d73aadd4f51564c78b8737b3c1edcb0b7095015`  
		Last Modified: Fri, 27 Sep 2024 06:01:32 GMT  
		Size: 7.2 MB (7193670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ff0abe0f391bab4ac114b0ec67042e6efffbe0a746da4c87e0a13c868fe6c9c`  
		Last Modified: Fri, 27 Sep 2024 06:01:32 GMT  
		Size: 15.4 KB (15440 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a34b4f874474be28bafea39628c9ae9cbce7e36d3e5efff05c1d99a192a47ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277705296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a1ce92960a3e59ff45ff72dd317f1a1ddbb78998e474b1a94b0b6e67ef10ae`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
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
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e143c6b4563fd2b7fba928d1140ee94b51e99d5272619bb9e2d5e4740f8185e`  
		Last Modified: Fri, 27 Sep 2024 10:48:37 GMT  
		Size: 154.5 MB (154503760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d6ee338c46762e1f15a943bdd1379cd9a00ce267413225596f74c21220157d`  
		Last Modified: Fri, 27 Sep 2024 10:52:07 GMT  
		Size: 69.5 MB (69466632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b97cae8e57da6edddef1fd1e07d8954589938a9b566d1f0688931d9fc8e7dc`  
		Last Modified: Fri, 27 Sep 2024 10:52:05 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ece5eac2dc9d01b591baaa4f5bc9b8f037e92ad120dd03bc28f15bfc1043ce9`  
		Last Modified: Fri, 27 Sep 2024 10:52:05 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e6c9f22ea1da94bb319df415455b3665974e2da88b463005b43e494c37082dcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7214127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5de9ff5cb4fe131ceb9197658febff06ae2ab9c157beda798cd7d3ccc849144`

```dockerfile
```

-	Layers:
	-	`sha256:8e7b6d84ce48aec6be9cab6cba0342b93d5a49d1ff1aab05df5569c2738f5140`  
		Last Modified: Fri, 27 Sep 2024 10:52:05 GMT  
		Size: 7.2 MB (7198151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a104b1f2698f32b0d390c73ca2bab9026159e53799fef7a7b37ebfa728247f8`  
		Last Modified: Fri, 27 Sep 2024 10:52:04 GMT  
		Size: 16.0 KB (15976 bytes)  
		MIME: application/vnd.in-toto+json
