## `clojure:temurin-11-bookworm`

```console
$ docker pull clojure@sha256:ea089cc0855691df1011f20d898a56e8df8b256b739dcf35d9ffcd10b1171192
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:22c05c34fd9ea48ef139ae1e356b58cb20aef1c0933448cc23b5dde7cdb28149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.8 MB (274843538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe36971828390bd8d76eb9dd95b80d5d40f92374929daf1492421320022dd2d`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae233d08cc1cb68b2a713d7001382c7e169c5e0959c3f55e5e794e8197d3b6d`  
		Last Modified: Tue, 03 Dec 2024 03:19:29 GMT  
		Size: 145.6 MB (145601451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d62e79e4c75eb7f06f4a913710b9fcf88ba18e843dc992672d39df54870063f`  
		Last Modified: Tue, 03 Dec 2024 03:19:31 GMT  
		Size: 80.7 MB (80744233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131a8edbcc39e162118f41ca836c6a57e5b11447dd73480cea4fb1c33576b36b`  
		Last Modified: Tue, 03 Dec 2024 03:19:30 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ee489e2bc6921f34e8f8be744c5e5d99f04ef4582ef01848b21ac2abacb32555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7215598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36ea85e3e772469d0517517e0809f74800d11cbd0f97631cd47ad491afbdb66a`

```dockerfile
```

-	Layers:
	-	`sha256:47ed8f5d12551a548235aa0758a07d572d9df97a4d8824094da4ef786ef2b36a`  
		Last Modified: Tue, 03 Dec 2024 03:19:29 GMT  
		Size: 7.2 MB (7201346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b142f665376f485826838368f0a3274a6a7d0af93a8a71d145412f7008e72c18`  
		Last Modified: Tue, 03 Dec 2024 03:19:29 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; arm64 variant v8

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

### `clojure:temurin-11-bookworm` - unknown; unknown

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
