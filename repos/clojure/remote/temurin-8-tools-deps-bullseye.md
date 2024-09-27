## `clojure:temurin-8-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:0f6bc507c82c305a07eb8c547c4d030ce9484409549f38558549680beca8b917
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
$ docker pull clojure@sha256:1cb6bfd2e9d08286291169a489b1b02780c6e9776b171bbefa112e503a59f86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.9 MB (225928118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edd23f6c0fd7f4e96860dd8ee3af1ac163c4834ba68b7ec92d9af3a09112b41`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:59 GMT
ADD file:aad8b86b3a958bc07504985acedcc819faa4f1ed12ca8b46d8d94c4d564cbdfa in / 
# Wed, 04 Sep 2024 21:40:00 GMT
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
	-	`sha256:d82c4492ee91810a42e0c53e955a661e9a092364bc474c9db559ea5b24b7047f`  
		Last Modified: Wed, 04 Sep 2024 21:42:52 GMT  
		Size: 53.7 MB (53731619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93db4c8afc8a0890bd9b0a199dd8e132178a1acc07b8c47cbbe930bb3d0c96a4`  
		Last Modified: Tue, 17 Sep 2024 04:09:53 GMT  
		Size: 102.7 MB (102729218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cc48033e70845f23056e0d4df9b6acd7cc7ef27efd95481e98a469627df56b`  
		Last Modified: Tue, 17 Sep 2024 04:15:00 GMT  
		Size: 69.5 MB (69466636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d946f956a425d52145666c8f682ad8848c66aae46635404ac4d26c7736afb1a`  
		Last Modified: Tue, 17 Sep 2024 04:14:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:dc047b145c3ac8c8b3710754128dac798615ddf0b612dbdc10ac9f230f310574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7085944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f26a9c6e4e25ade9366baaf1ed2398599f8b239ec4aad953c644a27da7825c21`

```dockerfile
```

-	Layers:
	-	`sha256:68a78133c140deab7790fa6072e69a7cc6890dc7be2a01fa654267569a4f606f`  
		Last Modified: Tue, 17 Sep 2024 04:14:58 GMT  
		Size: 7.1 MB (7071557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac680ffd48397976a165d1cbb68b138610b7bc1b87a153f9f08198e9feb7755f`  
		Last Modified: Tue, 17 Sep 2024 04:14:57 GMT  
		Size: 14.4 KB (14387 bytes)  
		MIME: application/vnd.in-toto+json
