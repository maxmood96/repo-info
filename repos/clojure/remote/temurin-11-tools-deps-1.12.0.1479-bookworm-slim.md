## `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm-slim`

```console
$ docker pull clojure@sha256:cdaae1d39f3a6f2319d60bb63110931bd1310c0e33c0c6a76aba94f66b10bff6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm-slim` - linux; amd64

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

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e80be01a5e3652440d4aa15c20774668bb8683dd7436fcafa92f1d86d3f7bfc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240881938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcc1c9dc034d48832552ddbca312b22c8ab8f88f39d99992154b0d905405107`
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
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b55715c2acf7d2e0d4e3993e57138bab284227d99b9c0daa802adff868664f`  
		Last Modified: Sat, 16 Nov 2024 05:21:06 GMT  
		Size: 142.4 MB (142389062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc174a48e12620c9d7a8a8d92c1d5bd82dc3faeae827b880bfd384655bd7dbca`  
		Last Modified: Sat, 16 Nov 2024 05:25:30 GMT  
		Size: 69.3 MB (69334874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0e627c65c04ecd2686d151843b7217ad0de5de99007fb3aae829bb632cbeca`  
		Last Modified: Sat, 16 Nov 2024 05:25:28 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1b4bab5f887b2e5610ab0c91c519b3126f7c4db50b4f59cba77f452b16da713f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4961612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cacf7c23a186e1445ec606e057f29760ef9df791897c4334dd09b8d351ac74a`

```dockerfile
```

-	Layers:
	-	`sha256:6e5c3439a99b59f3b14d597256b38aa2c4061aaee48756b9afa96d5378188834`  
		Last Modified: Sat, 16 Nov 2024 05:25:29 GMT  
		Size: 4.9 MB (4947184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b52174c56215722b29ac841116b9d0d9201f08968713fb69ca2f8d02342d659`  
		Last Modified: Sat, 16 Nov 2024 05:25:28 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
