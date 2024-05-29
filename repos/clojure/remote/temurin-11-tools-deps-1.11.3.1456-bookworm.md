## `clojure:temurin-11-tools-deps-1.11.3.1456-bookworm`

```console
$ docker pull clojure@sha256:4031a7c2e84e70c289e823daf830b91717c0ab9376ba2dd71d594e6c26e3071f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.11.3.1456-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:9975b46c3e7f367f6fb4c5697444ebc2c8de0e1ea6d3f4e98c89ed47b0e01741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275375575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c6d85a0a80ffc8ba8f807cc8c52a2ddfc47054ffe70b76473965f46544ab85`
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
	-	`sha256:0051e37ea87f46ec9a23ca18770dc1145a5bc3b7c4162bca01ec3cd4bd4a31ce`  
		Last Modified: Wed, 29 May 2024 19:57:07 GMT  
		Size: 145.5 MB (145504827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5a407f01cb4bf0e3ffd8582e6a500765ed955590fdcdedcff4f91c6b809a40`  
		Last Modified: Wed, 29 May 2024 19:57:09 GMT  
		Size: 80.3 MB (80293709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46705aa55305f5a195e51b3558200105aa38c685a79443d5644c8ed18bac5f66`  
		Last Modified: Wed, 29 May 2024 19:57:05 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.11.3.1456-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7e7148322b3850828d19ace9d649344a7a7074e0cfe509b0e85a03a391514044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6974482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66c3eb68f5b7ef64f43468cbb6cac024edb9eed0e35e18d655dbd1d69d790aaf`

```dockerfile
```

-	Layers:
	-	`sha256:af35da0d07b6d14bb750b32f5ae39b31cf1e8c379de86177c0fe07e148498161`  
		Last Modified: Wed, 29 May 2024 19:57:07 GMT  
		Size: 7.0 MB (6960667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddd64ee646e629a75804a7787e40b6dd8bb48a14e78b85c06f999e51e1af4c67`  
		Last Modified: Wed, 29 May 2024 19:57:07 GMT  
		Size: 13.8 KB (13815 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.11.3.1456-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fb884f782991a6bc9d0d32cce29edeb3348a6a1f85f36a9fb3415014c4a05c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.0 MB (271962913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f8431121ed4466a768de013e086c2ec843b2fc405072aae6fe0f0401555f30`
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
	-	`sha256:66442d4577a2a857519fc8836919bb6ff53950899016113d8484e65ae5cde093`  
		Last Modified: Wed, 29 May 2024 20:35:50 GMT  
		Size: 142.3 MB (142304146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e01ae05d282230a72a407ade1ea87e81894e411434c7994cf3720f6e764cbcd`  
		Last Modified: Wed, 29 May 2024 20:40:31 GMT  
		Size: 80.0 MB (80044730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233ef3817d5cb41b2b9e446f82f0a7873f2408643355c07d97f2562ce7744137`  
		Last Modified: Wed, 29 May 2024 20:40:29 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.11.3.1456-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b463f750aa617de7f7454ac6a7b13900c56ee6ff3d54306aebfcfed63be6325e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6981405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05fca5c02f13806643fbc984722bdd2def0e87cab99505f73030fff925317c8`

```dockerfile
```

-	Layers:
	-	`sha256:4c061f0e8cb671c85765729261674914faa93bda81122d7781fbf75e8ff5a1dc`  
		Last Modified: Wed, 29 May 2024 20:40:29 GMT  
		Size: 7.0 MB (6967054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29e0fa98842327750935a206782b52fdcf70967a47a8dbdea50fbedcef86445e`  
		Last Modified: Wed, 29 May 2024 20:40:29 GMT  
		Size: 14.4 KB (14351 bytes)  
		MIME: application/vnd.in-toto+json
