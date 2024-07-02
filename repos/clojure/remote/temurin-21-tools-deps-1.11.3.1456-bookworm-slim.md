## `clojure:temurin-21-tools-deps-1.11.3.1456-bookworm-slim`

```console
$ docker pull clojure@sha256:26dedc182ed60651ba770f4ded2e2426872e6f06d94ca31196af5f5247e38b63
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.11.3.1456-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f082da97473dfa6f4ffdcf03efed9dabe28d3f9c5f204c906136bac49868c106
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.7 MB (256691832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:894dceb7c9a2323e1b773ea706212f69a75d8bcc8adb9df5177eb50bcebff9af`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d659fa78b48b0b4633822aa4809a89c5d7bdda4a0668c32722589e418eda6ac`  
		Last Modified: Tue, 02 Jul 2024 03:03:08 GMT  
		Size: 158.5 MB (158497958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c85afca72c06ffb80685ea84da1831c33bbdb0b9708abd01832502729117a20`  
		Last Modified: Tue, 02 Jul 2024 03:03:08 GMT  
		Size: 69.1 MB (69066552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2782f00396092537d1d8a179529058ed8afabffe5dc8f94ecf89069e3fae35fb`  
		Last Modified: Tue, 02 Jul 2024 03:03:05 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614e12efd573d61ad0d6b7e89c0b310ad4c5a5cb5a0c7daa91e9200920258708`  
		Last Modified: Tue, 02 Jul 2024 03:03:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.11.3.1456-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:80b5966c00c06ae37980bb627e84818adca767f495cd69e1cc021d392b93f9df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4721953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bafbae17e9b5174e4a4ac6c0296ab2fa7404b132fffa857b7b2823213cbe74b8`

```dockerfile
```

-	Layers:
	-	`sha256:6a54e7f36529304f428213fa0c2260c4cc48d9db39c78498130bc5856aa56ef2`  
		Last Modified: Tue, 02 Jul 2024 03:03:06 GMT  
		Size: 4.7 MB (4705745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c25375c808c92693de422ee2358ce5a0373e0b6ba6a1d4aaf1c1b04ef5d89edd`  
		Last Modified: Tue, 02 Jul 2024 03:03:05 GMT  
		Size: 16.2 KB (16208 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.11.3.1456-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:691bbeb1fe08d22fe9a24ee9bc02eb1c6d9dcbacca4e84eabcf05c24a7e84b28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.5 MB (254467382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248aabf98bfe194631bb09490ad18d8477402821204cb91313edd15c703a9562`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c24c7a7b86f218dc61de558ffed50d5992f39df50505edf3204888486fe1b7`  
		Last Modified: Thu, 13 Jun 2024 11:53:39 GMT  
		Size: 156.7 MB (156665644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667d36716db6c32e5f608164829802c2dc048523eda4bc4f0af2899619d84594`  
		Last Modified: Thu, 13 Jun 2024 11:57:09 GMT  
		Size: 68.6 MB (68621026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60498181569edc615de2d1c4626403a3ec8ed0cab14a131cad534b5d7364fba6`  
		Last Modified: Thu, 13 Jun 2024 11:57:04 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8a7e46124952c8db9a98ef9e91226fa9e944fa42a779de0809a939ba096f65`  
		Last Modified: Thu, 13 Jun 2024 11:57:04 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.11.3.1456-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1445b83c40196ef621824131adecda830e1512e67c2e1c233dae9cd203640051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4728826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9fb172c404377bb3684ddd14d39ff6c9e3027a5b2522b1a13182a6059d94e24`

```dockerfile
```

-	Layers:
	-	`sha256:ca029339e69991fc53edf5a195153cb6612f0ac7a66ac1e2c0244319e59d547f`  
		Last Modified: Thu, 13 Jun 2024 11:57:05 GMT  
		Size: 4.7 MB (4712053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f730c868e53d4290bd69157576f10970c072dca956df3a1dfa30fae07266cbb`  
		Last Modified: Thu, 13 Jun 2024 11:57:04 GMT  
		Size: 16.8 KB (16773 bytes)  
		MIME: application/vnd.in-toto+json
