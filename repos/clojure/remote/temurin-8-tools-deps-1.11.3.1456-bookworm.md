## `clojure:temurin-8-tools-deps-1.11.3.1456-bookworm`

```console
$ docker pull clojure@sha256:49b00a66b6f6a1c4ea70665b648bcdf4feccb0c2cbbcb55bc24b216924ef6728
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.11.3.1456-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:3eda944e29dc638ee8c25a16a326c3393e9f7cd2c4ee6292b3c5cab5670754e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 MB (233470937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b5b8d264cde24fc5dfe453609f54d81fce8736ebc94e6cd484efd8e5efaf1e`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:b532f8e401e9a1fcc2ea1fc034adf820a5269c6ace45769f60a81fcb673f01b8 in / 
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:fea1432adf0957427b45b0ef8e37cbfe045b7cf8c15e3f43e48f2f613e214d16`  
		Last Modified: Thu, 13 Jun 2024 01:25:07 GMT  
		Size: 49.6 MB (49576643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d7413f6ca368d5a22dd2a0931de0eaef3b1a19137ee0f9ef567a83f1101d5b`  
		Last Modified: Thu, 13 Jun 2024 18:13:54 GMT  
		Size: 103.6 MB (103600198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8fc2e575919c621bdf32d0db9931994c16cfd78d75ca574047162bf8d6802f3`  
		Last Modified: Thu, 13 Jun 2024 18:13:54 GMT  
		Size: 80.3 MB (80293448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f3cb51bd90b68771877379a7033149590d3727beb88bb50c8fb78e9a9d5bf0`  
		Last Modified: Thu, 13 Jun 2024 18:13:53 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.11.3.1456-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9b11d42ed2efd4739586952c2d24b31062764380a97c1478795ed9bcdd89186a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6997005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:130670e87b544be6aedbf5842efe776107032b518b3d0acd704cd6d8874f49c2`

```dockerfile
```

-	Layers:
	-	`sha256:3f32a7ce29f09bcd4fcd2097496098b6a3c9cd2da28739552291b2d2acc2ad2a`  
		Last Modified: Thu, 13 Jun 2024 18:13:54 GMT  
		Size: 7.0 MB (6983154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cf4aba686b38e1728a804f715012f54921164382b5679c81aa343ffb3f2103c`  
		Last Modified: Thu, 13 Jun 2024 18:13:53 GMT  
		Size: 13.9 KB (13851 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.11.3.1456-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:80673afb6f294dae96c2bbb8591d48f57697c7e6a6d84859cab10a619469e5ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232359282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ca9a0d975f0f7d00833403cf38d2817c2cdca0ce66baaaa287bf8c228eb1069`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:cfc8f76c8181d3ae6dda16ae894b184c69dbba114d446426e466126fe0ae62e5 in / 
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:1e60a453843e00d6f3d4242dbd696365f0894e3ca2f02f4ce1ab098d7ff7907f`  
		Last Modified: Thu, 13 Jun 2024 00:42:50 GMT  
		Size: 49.6 MB (49613402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6e9ecbdc3ddf118977ce6146d477e95e017b027a376970e58b440ff008a5b9`  
		Last Modified: Thu, 13 Jun 2024 11:09:40 GMT  
		Size: 102.7 MB (102700388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d57c15b94be762ea9595f29ef21f8e920090b15b7c45195d49e434bd400f06c`  
		Last Modified: Thu, 13 Jun 2024 11:23:59 GMT  
		Size: 80.0 MB (80044843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c136e552c3c401165b050089010f937b995a05368d5ef1a03cb827f2b358ec0a`  
		Last Modified: Thu, 13 Jun 2024 11:23:57 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.11.3.1456-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:37c8b9c93257debfb3f0816bd1956671b50f2a9c4ccff1224a0884963cd19802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7003926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729c576e6018b3de1894c6df8280c38bc99df32b36e3b9432fd6b6e23c6c392f`

```dockerfile
```

-	Layers:
	-	`sha256:620e5b8f911c7df9b9bde6dca6eba5f9d4e486f2bd50b64ce02d012a2717dbcb`  
		Last Modified: Thu, 13 Jun 2024 11:23:58 GMT  
		Size: 7.0 MB (6989541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a47a9042c1cf709e6b9acceeebd31c42ca51a769f339d57412f7eb66c9719c4`  
		Last Modified: Thu, 13 Jun 2024 11:23:57 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json
