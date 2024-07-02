## `clojure:tools-deps-bookworm`

```console
$ docker pull clojure@sha256:854ca1c02f1d1a92b95b9afdf4342cb1b7eb1b310e1a5c1071dd00594c4776c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:a7e0eb6430504f96bab9cfcaabdfa459f65a74fd7aa43a59decc6d2de356678b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.6 MB (288564909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1926993d61160a9bb67102cf9c5621403207639d470a1fe3233c8720f2c3b425`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
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
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245af1f389224b8f3aff22fa6e64cf8b327733d4e777badfba601d09f7bdf675`  
		Last Modified: Tue, 02 Jul 2024 03:03:05 GMT  
		Size: 158.5 MB (158497941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cdb360a21699aa3a6c81fc2be63bf36c3edd27e146741b877580458d2ae4f0e`  
		Last Modified: Tue, 02 Jul 2024 03:03:04 GMT  
		Size: 80.5 MB (80511863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ca7f563b7565436eea24c04d42afa4fadb262ad2c6f5beb21be3e8abe53304`  
		Last Modified: Tue, 02 Jul 2024 03:03:02 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5342b926e66b4b56ab02f6cd73f5446c075c13466a81bb788c50896146db3af`  
		Last Modified: Tue, 02 Jul 2024 03:03:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:70a24399d53a14ee884db007c18a785c0715ee053a0c825f2e78fe402c1964e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6979410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:795fd178f448fe4ed542485475c0fc7b655c0e855855ab8a7bdbfce7f83d7e2b`

```dockerfile
```

-	Layers:
	-	`sha256:7acc4de91196aec621ec8c348539b767c98f20c06ab80da7e2dd3470f4c99712`  
		Last Modified: Tue, 02 Jul 2024 03:03:03 GMT  
		Size: 7.0 MB (6961971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19a947024fcc4e03b0a60ca4d4fbf5012f4025e849cef8953402bc08757bd24c`  
		Last Modified: Tue, 02 Jul 2024 03:03:02 GMT  
		Size: 17.4 KB (17439 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm` - linux; arm64 variant v8

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

### `clojure:tools-deps-bookworm` - unknown; unknown

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
