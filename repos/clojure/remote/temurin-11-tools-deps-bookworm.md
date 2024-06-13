## `clojure:temurin-11-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:cefc89361eb9ab775780f3ce5c2d4bcc533ef0a78e490976ff3da1dd780f552f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:8e56e160051368bacf5895399e6716d3d983047906930726fd7b82a74b05c4f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275376084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc92517726935095d47d144e6e51b52812e33cf03b26529654317a84585120b2`
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
	-	`sha256:2f78a7bf5cee0a23b9573f09671987910ab6a56f813a521cba87e006f35949d7`  
		Last Modified: Thu, 13 Jun 2024 18:13:59 GMT  
		Size: 145.5 MB (145505215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cf202c86d08fbd446dfb36db08c2c86993a5b99df60c3c370bc961952654ee`  
		Last Modified: Thu, 13 Jun 2024 18:13:59 GMT  
		Size: 80.3 MB (80293577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d83a86a6388795667d76ff66600bed332c4ad8803ea4314346c351b56106f82`  
		Last Modified: Thu, 13 Jun 2024 18:13:57 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5a11ea09d9885335fe60535d375be09be19d3a0f0de530ffec8d5b858c8965e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6974530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b75333f6b6df961bc7ca6b214ac6f117b72b79e848f96c7c7b8f23a584dbde2`

```dockerfile
```

-	Layers:
	-	`sha256:817392d0d3ef86f5a69a7505aebbfb2e9cae3faf28bf788de1883f9dfafe246f`  
		Last Modified: Thu, 13 Jun 2024 18:13:57 GMT  
		Size: 7.0 MB (6960666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:221a9d3695e8452ed3d0cd0225d42a5422128e7046fe76323acc8a6d69bd810e`  
		Last Modified: Thu, 13 Jun 2024 18:13:57 GMT  
		Size: 13.9 KB (13864 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1e453a0f11c540c82601cb4cd8af564dfe1ae6c907c72495bddfb192b9eb2ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.0 MB (271961867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea3c3d8831f0004ced58783ea22b2e4e073d324c63c02f609f6d1281ee79721`
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
	-	`sha256:c994443e04e21bb1306b98beb1d8092f88115cd46256bc1fab8093e67ac36682`  
		Last Modified: Thu, 13 Jun 2024 11:28:18 GMT  
		Size: 142.3 MB (142304076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58a010ce25cca5e1831f9847741d4c4c914229a4ada2c8494ca1f24b23c44a2`  
		Last Modified: Thu, 13 Jun 2024 11:31:39 GMT  
		Size: 80.0 MB (80043741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b593bf413a7e65204bc9d7679e1e54e5469968219a5044c9fda12ea20764a31`  
		Last Modified: Thu, 13 Jun 2024 11:31:36 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e428de6bd507596ea3af40119a43b881cd66b3bf10bca097aabbec9d7fd9593b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6981453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c4ebbf19797ea9411e881bf947b3e1f173a3a9a40315382d1471663d7ce9b5`

```dockerfile
```

-	Layers:
	-	`sha256:44c2fe527cbab997cf463a30fd544499b1372994bf712dc2d5e4bf2649aabdae`  
		Last Modified: Thu, 13 Jun 2024 11:31:37 GMT  
		Size: 7.0 MB (6967053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68783ecca6a31734472c4dafcee920de464e2401bf77a327aed2ebe249baa2bc`  
		Last Modified: Thu, 13 Jun 2024 11:31:36 GMT  
		Size: 14.4 KB (14400 bytes)  
		MIME: application/vnd.in-toto+json
