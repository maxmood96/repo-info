## `clojure:temurin-8-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:9d2f94ba61edb22edc444e968dbd1245f0cfe52310b25ced92ea70edc6bd2672
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:bb8f965b687e93224335dc673c61911e2da6371e202e1671edf8286a8e8e8df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.0 MB (228027854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2bf6d1fd0f3ad63cbf5f0f50decbb69452ceb2a65853c048d1dff4176abccb`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d2c17bce2b882027a9ca09a5b74dbffe3aaee695802fd4e6ae78b2d2868d98`  
		Last Modified: Fri, 27 Sep 2024 06:01:08 GMT  
		Size: 103.6 MB (103611875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a872890132e0f6ad0936b0c2cad82fd62f0f5df1908a605e973b418d720b2d5`  
		Last Modified: Fri, 27 Sep 2024 06:01:07 GMT  
		Size: 69.3 MB (69333945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b3fc5991232a194dfd60fd426f8005b4edc91bc39309e2d53ebc0a94bfc636`  
		Last Modified: Fri, 27 Sep 2024 06:01:03 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f625c0d7b51c039bbe2263a2f0d83f0d40355c49fa12ec9dfb33877798f5116a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7325985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a25c927421a931a509e7645918271b57ac389572b063343dfda91aa4e902857`

```dockerfile
```

-	Layers:
	-	`sha256:f79759eb69da2a16c4aed46507132ed4f1c20cb5a8ba23dd8f426e74ba3b7ccc`  
		Last Modified: Fri, 27 Sep 2024 06:01:06 GMT  
		Size: 7.3 MB (7312133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff273bf59405388dd6dce89a28cfac0b956553a22d4e91fcf00a4526d6cdf118`  
		Last Modified: Fri, 27 Sep 2024 06:01:05 GMT  
		Size: 13.9 KB (13852 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:509b33cc6a5d3a9693c4f68d3bdc87e9d1766b7f356da34ebdb27e94183dcdaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.9 MB (225930414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96069757e6f28533a35b3fdc39f94d074fcfe9539c293f2f1e1f8538e3cfdabd`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c16fb95702f0963c8e0700ba267f7d617ed0636b626ac3e4e6e1ebcac88e71b`  
		Last Modified: Fri, 27 Sep 2024 10:17:50 GMT  
		Size: 102.7 MB (102729254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4221f779a21bd53a7644034050445bb3648194b1934bbcd750bfb189bf190ca9`  
		Last Modified: Fri, 27 Sep 2024 10:21:23 GMT  
		Size: 69.5 MB (69466652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635397fb09d744cec142289f88a24df2cd30541045ead13f649cd22a67a50356`  
		Last Modified: Fri, 27 Sep 2024 10:21:21 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:bc0d6a2327742747e745b8425e2c9bf1f4942baeee117fc6ff694f82cf2a7317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7332322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30fb63bb83137989ac16047981f397542f8620abb372f9dafeedee92f1673e12`

```dockerfile
```

-	Layers:
	-	`sha256:880c3a62b5285abb9d8e0aa94af84b1c04819a9c52416e94e40c430465260a8c`  
		Last Modified: Fri, 27 Sep 2024 10:21:22 GMT  
		Size: 7.3 MB (7317935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7647a014abdc075fbe9e1d161a31da8ad8f5cd865aff30da9c89f059d5d60a3`  
		Last Modified: Fri, 27 Sep 2024 10:21:21 GMT  
		Size: 14.4 KB (14387 bytes)  
		MIME: application/vnd.in-toto+json
