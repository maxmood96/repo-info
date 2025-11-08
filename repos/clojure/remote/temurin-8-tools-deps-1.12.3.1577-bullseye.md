## `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye`

```console
$ docker pull clojure@sha256:a6435095f2b9622da4b75dd016b8e36e423189fc61cfd6b0a7741eff402e5d41
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:a6c408a54b792aa1971d48ccfb0aa3e724de689af193d89640db3048fcf66085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.1 MB (178051660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ab5711d021282f35eb552b19491b9e60282f608df842e1f9d4864242eed5df`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Sat, 08 Nov 2025 18:04:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:04:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:04:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:04:19 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:04:19 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:04:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:04:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:04:32 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8437d2fd04be8425cb1312badee987df12033091edcfb0ecdba5fc92765b205`  
		Last Modified: Sat, 08 Nov 2025 18:04:58 GMT  
		Size: 54.7 MB (54733342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10fe1c4d1b4f10cc0060f31684f45dde54d7a46234b73ddaa78c896953a727d`  
		Last Modified: Sat, 08 Nov 2025 18:05:17 GMT  
		Size: 69.6 MB (69560980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e02e5b4a6ddd5215560d73ed8faeb519554f0faf695e96c1188e5a368e9a6367`  
		Last Modified: Sat, 08 Nov 2025 18:04:58 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7167742902fc8c4343ea8ee1a2d44b0124b786d29c3baaa52cf6d7c3ebfe9ff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7531471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ebd5e8a8404bd2092f0e87338cfbe099299cade35099932e234d648976424c`

```dockerfile
```

-	Layers:
	-	`sha256:7957193a78e8c446ba4b4d6d8ebd364f9ed5efa0ab474067115e9791e38746ee`  
		Last Modified: Sat, 08 Nov 2025 19:37:52 GMT  
		Size: 7.5 MB (7517277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:918211fa9510d23435b132d4c95e2f74034854f8a93097d0f773041e12f9db8d`  
		Last Modified: Sat, 08 Nov 2025 19:37:53 GMT  
		Size: 14.2 KB (14194 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5032306832fb3b1fe815c2e8c078a1c364ba052d630d46d65bfc15b97345d501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.8 MB (175761996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3967a1db8a3c5754a7cc8db1c3f6004b156400229301e1c32d6b089fced0522`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Sat, 08 Nov 2025 18:03:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:03:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:03:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:03:26 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:03:27 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:03:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:03:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:03:40 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d65e2c645922bca495cc09b41e5fb6607a461cc075f841130727e1fe1abad97`  
		Last Modified: Sat, 08 Nov 2025 18:04:25 GMT  
		Size: 53.8 MB (53815043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9ba25c91c8555947a56d5b6ac9e7594df6d8008369b4a8baa833ae3bc7e18f`  
		Last Modified: Sat, 08 Nov 2025 18:04:11 GMT  
		Size: 69.7 MB (69688338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3daed8b92b5dd57f9939c2901a4983077c2f762983166137a63c57ad016c8503`  
		Last Modified: Sat, 08 Nov 2025 18:04:03 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b2b9de790e3845df4580cccc767a1a734ba56206f544b2ff2784a9274603c7e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7537386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5079b759349508ae21514adf74142f042de4dcd71abd267fd726b667875f1f5c`

```dockerfile
```

-	Layers:
	-	`sha256:0d581d648142dd9116261e365ecbea64fe15f5c4b14cd4af0768375eb194c8f4`  
		Last Modified: Sat, 08 Nov 2025 19:37:59 GMT  
		Size: 7.5 MB (7523074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d6cbe9684656e3fe27d39a1030334f1a57e2ad006316c982394bcb112069e30`  
		Last Modified: Sat, 08 Nov 2025 19:38:00 GMT  
		Size: 14.3 KB (14312 bytes)  
		MIME: application/vnd.in-toto+json
