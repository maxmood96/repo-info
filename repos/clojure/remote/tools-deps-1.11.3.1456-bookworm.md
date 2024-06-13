## `clojure:tools-deps-1.11.3.1456-bookworm`

```console
$ docker pull clojure@sha256:f8e7d9fa93f1fc4247d23c9169dc7f9cbc7c037d1b7ef0b50acaeb2fbb6bcc83
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.11.3.1456-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:24d567f0588063dc7bf8ff1472936a40803b71ffdd1a714797579a6781d01cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288374120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cef637ec94e2a5dc060d8dfdf66daa85872429c8a36f9b2c4faab3c532f4e02`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad246211a32d46848be9601189d9208d315885aedbe572a849a9c4f66e28a555`  
		Last Modified: Wed, 05 Jun 2024 06:10:32 GMT  
		Size: 158.5 MB (158497970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55d1f2a4fe702ec4da105ca3d2ecc8506cbe8d17e232f407c66b58deb693bc7`  
		Last Modified: Wed, 05 Jun 2024 06:10:31 GMT  
		Size: 80.3 MB (80298717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc8f69844e4d9c9006da1bc4faa60b9ced5b5fbcd4ed048deb78e956816c2a4`  
		Last Modified: Wed, 05 Jun 2024 06:10:29 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb947bda822c6494016a0bbc48473c4010154cdc047178df10a8660b512ba31a`  
		Last Modified: Wed, 05 Jun 2024 06:10:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.11.3.1456-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7fb8fbd04339319c463192332d497d344c62ef038172b6745c0a2cecaf8ae60e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6980066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817a75155f6adbf140844a16cd345edd6f389fb91890e28f5eb4ffb1dc097e55`

```dockerfile
```

-	Layers:
	-	`sha256:2633d806ea5df3fa497eab6d4fd99bbda5f3c509a766364b1b225034f21ba5ff`  
		Last Modified: Wed, 05 Jun 2024 06:10:29 GMT  
		Size: 7.0 MB (6962676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f84ac94ccd3f8aff6c572d02fdaf305b90ba7b2b9d11716bc32e950cb40d3b8`  
		Last Modified: Wed, 05 Jun 2024 06:10:29 GMT  
		Size: 17.4 KB (17390 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.11.3.1456-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b9f4673529a26e000904117f652fd12de42dca7b910a037d64b8056fc2f9566b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286325232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0235ca1780b5528b49720eca11d6e41c69431e5faf3f3ae93253e512190a3fd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1e60a453843e00d6f3d4242dbd696365f0894e3ca2f02f4ce1ab098d7ff7907f`  
		Last Modified: Thu, 13 Jun 2024 00:42:50 GMT  
		Size: 49.6 MB (49613402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3821e8399c5ada85512a0d6bc71593288d495a78acfbcd5dc576817d7341de25`  
		Last Modified: Thu, 13 Jun 2024 11:08:48 GMT  
		Size: 156.7 MB (156665624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b047c08fa3f03e8ce2c26245b7fb0e2d5108a699a5a929803f3ca02c7e9a5f9`  
		Last Modified: Thu, 13 Jun 2024 11:56:18 GMT  
		Size: 80.0 MB (80045158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1035889add5e248ee09f591905ca5a45b78d070d2d1f761200f13de22e6edf9`  
		Last Modified: Thu, 13 Jun 2024 11:56:16 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e735e7932c43acf272bb77a8545e691215d8fd4b485bf9414b92044fd4a58fe`  
		Last Modified: Thu, 13 Jun 2024 11:56:16 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.11.3.1456-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f0ca0f0fbd9939f4a72411d8c67526a5a4381b3c3a655b581daa6a49d4231649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6987182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646277bbc870b52dcddab9e52832119e1d3bd736404f91a97b0946df0c1b264d`

```dockerfile
```

-	Layers:
	-	`sha256:d8f89d1868f4bec7e00636d7a4a31b4f19979e87b8ecec58ae4fe284d2f1ced4`  
		Last Modified: Thu, 13 Jun 2024 11:56:17 GMT  
		Size: 7.0 MB (6969135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10f27ead3dae6a819d58cfde49cf89fe060d381e5c3f49606b1b9ca8de0cbeea`  
		Last Modified: Thu, 13 Jun 2024 11:56:16 GMT  
		Size: 18.0 KB (18047 bytes)  
		MIME: application/vnd.in-toto+json
