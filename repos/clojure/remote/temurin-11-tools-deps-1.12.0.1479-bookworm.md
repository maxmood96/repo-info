## `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm`

```console
$ docker pull clojure@sha256:229e39da07056abb1f0408d2dfc858c51230d956e7f64a4164d6644524db821c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:eaec784c204c2306bb8300bba25ba0b4936c0c8958087ca8a075aad256649d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.1 MB (276116132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45284fc419c885a7684eb256d22a572e6cf621c81011872cfe6bcdb3d9b194ef`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9662d5e58210c8240c05ce9b13f361b29fb2dbf0cb07d5cc7b0ebac42e943f0`  
		Last Modified: Sat, 16 Nov 2024 03:51:42 GMT  
		Size: 145.6 MB (145601404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f274cd9c99440fc75f3773cbe96d2f3abb7cef30ecb7964f50ee8f4f2789a8d`  
		Last Modified: Sat, 16 Nov 2024 03:51:40 GMT  
		Size: 80.9 MB (80938388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72863d85005da2630c0396ca4367a1b82f068765ec46a7cb8b353de97db236e6`  
		Last Modified: Sat, 16 Nov 2024 03:51:40 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:73d6b8af1d1b2dcdf34197d614d80f8e8071789ad1a24b089a6b5dc43334ec30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7216845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8434b9edc8d29352f69e7aad77dfd849134f644c9864534fe4d49b546f5305e`

```dockerfile
```

-	Layers:
	-	`sha256:e2ae286fcc3203925f32b9bbcda64ba623e7e84d36f48e5ff43627d4c2e08322`  
		Last Modified: Sat, 16 Nov 2024 03:51:40 GMT  
		Size: 7.2 MB (7202594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61567af0e76b86f2f97798c15bd746e5c5ce8b42be845388c6e674d59e50267c`  
		Last Modified: Sat, 16 Nov 2024 03:51:40 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:faa460d96f47085aeebdf6cc32ded5d4476050154ca543adb6ec7f415632eee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.8 MB (272775286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88d0984527c8c20172ab19ff2bd9bebcdb96d0f5db3031eb779231f8a67a1a9`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28dd2b0b60c02b8a9fd58b477f6fe962396c2a452c8c346722aaffe3c5a9a13`  
		Last Modified: Sat, 16 Nov 2024 05:20:05 GMT  
		Size: 142.4 MB (142389148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58140ed844d5458f3c9e4165acdceae6e0ddf2f6d8b04ec27b89c0e2eb676fc0`  
		Last Modified: Sat, 16 Nov 2024 05:24:38 GMT  
		Size: 80.8 MB (80798293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d36008c906698cb3b90ad59094e7346e1222679b7b2260c793fecf9f3221f2`  
		Last Modified: Sat, 16 Nov 2024 05:24:31 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8dfdedbf28756d738d14e01e12bed818bbae1dca4d678047fefc69816b296021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7223350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e807dc3367b772ee11eaba4113acd36855b209ac8c14ce29c3a0fac091e05ab3`

```dockerfile
```

-	Layers:
	-	`sha256:9de3c7b6e608df482b64087ce23282ea287c781a7ed8c49e8baad6276c740758`  
		Last Modified: Sat, 16 Nov 2024 05:24:31 GMT  
		Size: 7.2 MB (7208981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4a72b874b9a5c8549cdfb885b3bc0008e6d398bd937a58b2e5435f3bfbb0421`  
		Last Modified: Sat, 16 Nov 2024 05:24:31 GMT  
		Size: 14.4 KB (14369 bytes)  
		MIME: application/vnd.in-toto+json
