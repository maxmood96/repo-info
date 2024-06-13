## `clojure:tools-deps-1.11.3.1456`

```console
$ docker pull clojure@sha256:1f6728e45ecf295793df29082ca97d6028b729f7798ece9756e1c90e2d5a6d5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.11.3.1456` - linux; amd64

```console
$ docker pull clojure@sha256:3934a6e60ccef141230431c013cdd2d8e21d6575e713a228eaa20491ef436376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288369805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5488b57a3670102ce2067c472218c66c9d3d1d69cc3bb61afc288bb92ae7b58`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fea1432adf0957427b45b0ef8e37cbfe045b7cf8c15e3f43e48f2f613e214d16`  
		Last Modified: Thu, 13 Jun 2024 01:25:07 GMT  
		Size: 49.6 MB (49576643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd0408e39af59aca20ad624a245e88d6b58f9c5d4e12a5c29252920ccaba557`  
		Last Modified: Thu, 13 Jun 2024 18:14:22 GMT  
		Size: 158.5 MB (158497943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4d001f2083c6137367f9be6852bdbcf41d60bf8fc8850a3a386f2c17088216`  
		Last Modified: Thu, 13 Jun 2024 18:14:21 GMT  
		Size: 80.3 MB (80294172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c274a86532825749cd40ead63325d063a7be35bca67743969a932b7d5f68df`  
		Last Modified: Thu, 13 Jun 2024 18:14:18 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7981ebdce5b61879c6a7053918c95461e5fe697841325b8a0a588edbe9f3b0`  
		Last Modified: Thu, 13 Jun 2024 18:14:18 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.11.3.1456` - unknown; unknown

```console
$ docker pull clojure@sha256:60dcd21620e37bb92711abaf13d5dea8c8e0a577f3ee83aca2bb1a4d58b8ab93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6980115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db28c833c9200eea58916e73691d69743105934ede9efbb92d2338af3703591a`

```dockerfile
```

-	Layers:
	-	`sha256:64e69162c0dab4cac83b49345ef5c3f09943f55020ff2110ed97dfd822f7cdaf`  
		Last Modified: Thu, 13 Jun 2024 18:14:19 GMT  
		Size: 7.0 MB (6962676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c56bec2c431fc8edd7eaa026765f3fa4b707f7ea30c0056422e74faffceadff`  
		Last Modified: Thu, 13 Jun 2024 18:14:18 GMT  
		Size: 17.4 KB (17439 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.11.3.1456` - linux; arm64 variant v8

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

### `clojure:tools-deps-1.11.3.1456` - unknown; unknown

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
