## `clojure:temurin-8-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:f0f7390b5569e9cd3896b8cee3d30bc78e9d2750c7b9d10f63e2b59f1d0b5e62
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a02c4f2b6fb04511a7ad945ff46a8c60dd8fc20b8747c6a81ede27e283ca13f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.6 MB (201619357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c36a7cbe9f234402f886013b5fb9eca55a85880431979912dfff11f0910578`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
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
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a372bcca8abc222c5c50573b3ec60da5e48bbc2eb6d869af94416ad47e4b0780`  
		Last Modified: Wed, 29 May 2024 19:57:02 GMT  
		Size: 103.6 MB (103600228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be46677484b85238b25c1bf52a2db36f4195c11b4dfb751d309c4fdac9094e22`  
		Last Modified: Wed, 29 May 2024 19:57:02 GMT  
		Size: 68.9 MB (68868071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0032248c395a75d6311e7cf5291be0948af52292b6199bfae678ded5c472c9cd`  
		Last Modified: Wed, 29 May 2024 19:56:59 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e085510a23abaecb1e7fb9d1dbdf0cd066a6c2d8ed2ae9197f252ea286fb5c96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4741298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:496999d614bedef9aa65c0910ec682cb638ae7e01d9f64698924cca0fcb2d551`

```dockerfile
```

-	Layers:
	-	`sha256:b082c7cd74512069d05226529e6ca5f7343ee7d9b063ab0b83e189a1254461bc`  
		Last Modified: Wed, 29 May 2024 19:57:00 GMT  
		Size: 4.7 MB (4727427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d49673d461ec1f64ac882325455b5f675a87a885a9a0d03caa857f868646dd4f`  
		Last Modified: Wed, 29 May 2024 19:56:59 GMT  
		Size: 13.9 KB (13871 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:44f499666621f3a2da6396ed2ade01dea26b11ffbf56bf13cc4eb498f65b923b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.5 MB (200501299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a501f716b33f1ab60a24016b4364c5d451f7cdbf44102f4b82915a6a76a27a6c`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
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
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9a88c9bed081edb4c90f4a71c52d7a62dcd0620d34a7f26ae50be4431385e2`  
		Last Modified: Wed, 29 May 2024 20:24:42 GMT  
		Size: 102.7 MB (102700399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f114415891dfcd918d36f82dc22314da6f60b66a9d5735a451be7eddbfd153d1`  
		Last Modified: Wed, 29 May 2024 20:31:10 GMT  
		Size: 68.6 MB (68620750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b86419afc0cd7195d0ce901b3cc42e4d6ddc47eb05d41ff2faaf7f91427cc57`  
		Last Modified: Wed, 29 May 2024 20:31:07 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e9d64629598a0d7b5a967cc98c418b7b896fcaf2b28057f4d2a790bf4fe66fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4748222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad73766d01f0d34a58ecf4d62839708095de3a4a8ba0937ad554bc53615026c8`

```dockerfile
```

-	Layers:
	-	`sha256:c52884690326eb710ee38767b5212053aa4688fab50258e986916293de0839b9`  
		Last Modified: Wed, 29 May 2024 20:31:08 GMT  
		Size: 4.7 MB (4733812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f950430765045b1d292aedb219cadb76724c4249e4b9cd952d2586c6ff3caca3`  
		Last Modified: Wed, 29 May 2024 20:31:07 GMT  
		Size: 14.4 KB (14410 bytes)  
		MIME: application/vnd.in-toto+json
