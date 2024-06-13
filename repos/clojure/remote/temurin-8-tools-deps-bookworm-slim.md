## `clojure:temurin-8-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:ff51aa56855d2cbac8ca1885f40fa7a7d24ec1a000086aa95b9f0ef17f21e8e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:aefd4dea1470d711da87abdf6197977d8132940dff566b797c76445fc11922df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.6 MB (201618977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71dfad30ae507dd0d9f0239cad56956215e3bd7fb555fb58e2b30225c309a98`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
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
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fbc16548e0cc43c34039da7dfaef217d32b3d460d7be0d7ead5f668039dc91c`  
		Last Modified: Thu, 13 Jun 2024 18:13:50 GMT  
		Size: 103.6 MB (103600204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4c72fbda44c0beae1b5aa5c2338250aee5901b3d1726aea2b82cbe34a9b75d`  
		Last Modified: Thu, 13 Jun 2024 18:13:51 GMT  
		Size: 68.9 MB (68867693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c032c284f66cad8a63b6a3a13304f505ce062fbec5a0ab961ec132f252dd9501`  
		Last Modified: Thu, 13 Jun 2024 18:13:48 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:142fcec544e415f01e1a64bdf68bc52d1fed653c72aa8471361bdffd22c60f4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4741346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef32d03399f7824c02528eb139422a0bfeab0d7fbc96f5f94d0654863009a52b`

```dockerfile
```

-	Layers:
	-	`sha256:5a336663bcd6d9e7fac2c73190b8518721490cde51967c609c4c85ebf4b684b5`  
		Last Modified: Thu, 13 Jun 2024 18:13:49 GMT  
		Size: 4.7 MB (4727426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fae9e2798adf664abdba29f49e4c4fb539f99718b28cd5287ee978ef5f7638e6`  
		Last Modified: Thu, 13 Jun 2024 18:13:48 GMT  
		Size: 13.9 KB (13920 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1d3f3b0e42f044fa2d05df85fcd8cb494d6beef6b5d3da72d2401eee9704f08c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.5 MB (200501208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507a3233f6477684d7df13264a9313b45461f623b54712cbe53e26110a65365a`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
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
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab2e61ffd9a81e8a8962bd8afec8741dfdf92978bd880ae8228d1fb558eca13`  
		Last Modified: Thu, 13 Jun 2024 11:21:17 GMT  
		Size: 102.7 MB (102700399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2605297d0c66832f95c152dacedef5f44e01743fe01f126c6f95e516384fd2d6`  
		Last Modified: Thu, 13 Jun 2024 11:25:47 GMT  
		Size: 68.6 MB (68620493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7492410e516c81137a2ef783385c26bf87d8dcbc327dcfd40539839eb8aa31f3`  
		Last Modified: Thu, 13 Jun 2024 11:25:44 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fb7fe2302bb08654b7730d53cde283be376ee75b32b0613bd87c47fb0491b6b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4748271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f843da8a682b3d0498a3b436871982f67b47528cc130d9c8479c649003156470`

```dockerfile
```

-	Layers:
	-	`sha256:c809a5a1d29cfb967a92b0b54af3d76ac8bcd0291d445f6cdc8a5cd16f3baf4e`  
		Last Modified: Thu, 13 Jun 2024 11:25:45 GMT  
		Size: 4.7 MB (4733811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b861b9e5181cf0bec969117193b45401b12398823a3b0a65bcd58dc296e94af8`  
		Last Modified: Thu, 13 Jun 2024 11:25:44 GMT  
		Size: 14.5 KB (14460 bytes)  
		MIME: application/vnd.in-toto+json
