## `clojure:temurin-11-tools-deps-1.11.3.1456-bookworm`

```console
$ docker pull clojure@sha256:81952d04ef83db2d225df24dce5a4e62f3bb458c91877b526d25a34fea18a211
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.11.3.1456-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:d8ffe171823d05ac7e2ad002db542c7d7cd1b62586eefad6969d5a547ed8ceac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275381691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf61ef1646a4b5a244ab7c14ddd25ea22c9745c0e3283d1426d9da6dd8f58e31`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1806f741e5fa838a221acff1b5807a0c4cddbb935a8b812e19ad87a0e553ea7a`  
		Last Modified: Wed, 05 Jun 2024 06:10:21 GMT  
		Size: 145.5 MB (145505214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f45be0a4723943683a32b1f74c9956ae77a6d6ad50c9375a1f0cbc8474e501`  
		Last Modified: Wed, 05 Jun 2024 06:10:20 GMT  
		Size: 80.3 MB (80299440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc27fbaf49f75245bd805ce5b402387ad594f86edbccced91b4164f3bfcd377f`  
		Last Modified: Wed, 05 Jun 2024 06:10:18 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.11.3.1456-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:264585a204c8907daf3ce290eeb7da2942b493d42592897c5124a8f27f981265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6974481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12fb594d524c6a835030ace6613d6c6329dab3b0d96b5798db0e58fe8a518d63`

```dockerfile
```

-	Layers:
	-	`sha256:4afc5383fd7cf50eadbbe0de625cc217abf0d0455d61453e12b4347bb1eb3628`  
		Last Modified: Wed, 05 Jun 2024 06:10:19 GMT  
		Size: 7.0 MB (6960666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a816f3a2cbf6d19e863307e8b9af45ba841e38d96390b5fe9b5f2114aae0ce0b`  
		Last Modified: Wed, 05 Jun 2024 06:10:18 GMT  
		Size: 13.8 KB (13815 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.11.3.1456-bookworm` - linux; arm64 variant v8

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

### `clojure:temurin-11-tools-deps-1.11.3.1456-bookworm` - unknown; unknown

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
