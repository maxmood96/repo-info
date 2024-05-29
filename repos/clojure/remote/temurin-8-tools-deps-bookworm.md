## `clojure:temurin-8-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:dc5509d993f341c505d1915813c4ec654bf37183a217417389348780bf29bb20
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:7b345daffb1a88fc0feddbf9cdbe393ca7fb4a257670982659504581ac99af1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 MB (233471529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4df56b60e3bb9f183ee5fc9c132881591f5445582293dde5585e2bdff4c11f4`
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
	-	`sha256:ec721d431be9d0253b739c890cea67b17befbb9aec1de491fbd05e7057fe2ef4`  
		Last Modified: Wed, 29 May 2024 19:56:56 GMT  
		Size: 103.6 MB (103600228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb19ffaf0dd1136cd18b6dee327aeb99c7ca1f26121fce2fbde87c6f564dbed`  
		Last Modified: Wed, 29 May 2024 19:56:55 GMT  
		Size: 80.3 MB (80294263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a75229b09ab18204502cf70d6f62432526c362b0e40c44bd73ec12a3ac3da5`  
		Last Modified: Wed, 29 May 2024 19:56:54 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0b7de5083132b8a5f5936aa63f2d2c419090370023c255594c16f9d8628fff8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6996957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb3a817d67f0aeec3f4b7b5bcd90e64a34ccd481c57f95ebe38f837ee67b080`

```dockerfile
```

-	Layers:
	-	`sha256:71b970b0ca55f8a777bd4dd1c51dc99a6a1a8ba69b44ab1ec854b0c6f7c61735`  
		Last Modified: Wed, 29 May 2024 19:56:54 GMT  
		Size: 7.0 MB (6983155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65d57cdda924990e299f4a63080d36efefab4c4ee8a826e04d9de66c6c3bf2ad`  
		Last Modified: Wed, 29 May 2024 19:56:54 GMT  
		Size: 13.8 KB (13802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b79163c04903f55239b95bc5ccfb71124b63954ded8a2e2b75452bc15dd20a35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232359324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6279665e2f448d5d2bd8868bf52ca7e08b8650b91353060df699c5cfcdf9f571`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 00:39:32 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Tue, 14 May 2024 00:39:33 GMT
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
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429513d912c66c681705c8aa16d730a4b71c1cd1e40db844d161cca11cced3a2`  
		Last Modified: Wed, 29 May 2024 20:23:52 GMT  
		Size: 102.7 MB (102700444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67eb69a4e3c98e7b586f4515ae0755952b06cc932ac71d89244c8fa0972cff6`  
		Last Modified: Wed, 29 May 2024 20:30:21 GMT  
		Size: 80.0 MB (80044843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acb077a3957361c57c3034c62d84f0f2ad39b014511f424caa93eb867900255`  
		Last Modified: Wed, 29 May 2024 20:30:16 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e990660b82a1fbee7fe250bf002bfe48248a6884c789d230f5d6ea9f3d90ff0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7003879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46301d1c5ae2c2f15a0aa41a9ee8fa2e17b328f87ac227fa81066d18550e417d`

```dockerfile
```

-	Layers:
	-	`sha256:8758c8e7b09d0f4ff148a0dfcf334c10534c1397544a5e58a504e1008910049b`  
		Last Modified: Wed, 29 May 2024 20:30:17 GMT  
		Size: 7.0 MB (6989542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d492eb3e7c52bf0857f9e0f8ccf34cd64c087c5525cbdf5c695221b00b72ab93`  
		Last Modified: Wed, 29 May 2024 20:30:16 GMT  
		Size: 14.3 KB (14337 bytes)  
		MIME: application/vnd.in-toto+json
