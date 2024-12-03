## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:1be42cb3eec8bf7092c54ac3a01b99c5813a66aee206afce99f5c55e0b2d5858
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4b352af91a9760160b35bc6f5202a536d148188e97fe83cc40d0ebdd019d10f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243126394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff0b26e67e37f26d26eec17220f87722cdca930047746e2e276ae1f7100a5b7`
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
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae233d08cc1cb68b2a713d7001382c7e169c5e0959c3f55e5e794e8197d3b6d`  
		Last Modified: Tue, 03 Dec 2024 03:19:29 GMT  
		Size: 145.6 MB (145601451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d41c4a97fd12adee01f5e9aa01cbbc1263512a0ed8974483e7dfc652ec7a717`  
		Last Modified: Tue, 03 Dec 2024 03:19:28 GMT  
		Size: 69.3 MB (69292717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c95fb76c8bec182fac56e0658448998ead602f0b93ae92fef3205637634cbb`  
		Last Modified: Tue, 03 Dec 2024 03:19:27 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4890dba74a598ddb3b01ca51d342dd47e654865d248729728e41d97019ec4394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4953861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b7deb8e4b5fa155c132dfb589fa6a65bd94343259028cd7547f1d61544656ca`

```dockerfile
```

-	Layers:
	-	`sha256:e446a6d55bf1163e8e53bf80833acb60cdf803ac81e281308072652d61b99c39`  
		Last Modified: Tue, 03 Dec 2024 03:19:27 GMT  
		Size: 4.9 MB (4939551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c50e0e17ca98fe455b753acab4046ba6e7ea14973f7a191379a1e19d092f9824`  
		Last Modified: Tue, 03 Dec 2024 03:19:27 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9e60cbcabf282e5f3bb2bc308c66e29a7f2cdbdadac908fb3e39f92af771d777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.6 MB (239589349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf2122188fb511668480afab037af29249bb2db7c97a8490e8185d0ce807974`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee73b740bf0c91d6533d7223a2201ab13c32a02ba20c93d7ea7ea16f74d4af4`  
		Last Modified: Tue, 03 Dec 2024 15:10:14 GMT  
		Size: 142.4 MB (142389034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42019f3dbe82ed62652b9dfd4ebacea7dd161f679b5c3f71bf492ec7201def0`  
		Last Modified: Tue, 03 Dec 2024 15:14:24 GMT  
		Size: 69.1 MB (69140861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2721b8553131d2687fa412a2c1299514a6be6f18fa54b2485a45848c3959e6f2`  
		Last Modified: Tue, 03 Dec 2024 15:14:22 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d5fd67c5c79e594d8ba59ee1807c6a3f79df2f4ee0b2a30ad8ea4e901c6a5347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4960364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:999abf1abdafc5168237db6f2894986ac53575f435d86777c42640990b2a2e94`

```dockerfile
```

-	Layers:
	-	`sha256:7f28bfb239a2a7116fdcc0f4f4c96f4a1f310c394f6515b3f7c9206f4444e8f1`  
		Last Modified: Tue, 03 Dec 2024 15:14:22 GMT  
		Size: 4.9 MB (4945936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:272016f4de68c85e44628cc9ae25a4bf1a50ae700f1c15f2125f8a6d912e010c`  
		Last Modified: Tue, 03 Dec 2024 15:14:21 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
