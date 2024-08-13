## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:c1f5327bd7b5526bddc7b3d0737fbd45111e46c52af01b27b1d314c77637438e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:3d45aecdcdd022680b89ff000371c92eecf728dfb05dfc8832e1fd2a290115fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.6 MB (269598006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5405273f9a32d7d7f6de88263f70bced3c06efe0c9d74f75385b30d1d48902`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:6648a8158bbf4a36244eb9e936fbed4ea29f2f090fb0a97a6a737be2d85a5333 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:203e9cf21bd27322e5baf32653bf3314ccf688be497585240d18b9f0ca24f2ee`  
		Last Modified: Tue, 13 Aug 2024 00:24:05 GMT  
		Size: 55.1 MB (55084675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284a9b1ebed17fbcfe16503a1a89154ff13dcdd053b20fbd5f02d9f3de401dd3`  
		Last Modified: Tue, 13 Aug 2024 01:11:19 GMT  
		Size: 145.6 MB (145550323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddfe243d8bc8e9b35547c5511c04d2c5ed39f4032219267a653417733318f828`  
		Last Modified: Tue, 13 Aug 2024 01:11:18 GMT  
		Size: 69.0 MB (68962364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f57f59a36bc1ebc6d6cf0338464a82b44517eff5040ead61a6b1690c7a5393`  
		Last Modified: Tue, 13 Aug 2024 01:11:17 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7a53f0713c9b5a79b5cd90bca6a61e7be8c067863686e7d95af7ca4ce64da571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7054209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dcb857e78d07d0ad19e89d351600a5b01c1853226771c175ede57c2e076cd76`

```dockerfile
```

-	Layers:
	-	`sha256:8d363bf5e80730b2a152ea8d0d95ba75ec7b5aed567eed66a73e2d1640b6f67b`  
		Last Modified: Tue, 13 Aug 2024 01:11:17 GMT  
		Size: 7.0 MB (7040344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cebb40f3165de95c0888df9258965cda3be5e2a9275851fd2e67fd299aa4f9c`  
		Last Modified: Tue, 13 Aug 2024 01:11:17 GMT  
		Size: 13.9 KB (13865 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:032ca02718a679e53d4064ec6da6f6751ce4fb0771a238142d8389af28456a65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.2 MB (265180270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0407dd690ecf930e054f06b6d45b13c9dc45a43bb676f52dbf5945a12c92ae77`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:58 GMT
ADD file:bbd5c67ed8e7916601bc20e4ce4973720e715d9dcd892ccbd64c1d5de711a38d in / 
# Tue, 23 Jul 2024 04:17:59 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2c9750102c61ce3f4a11c8776dfc892d41a6d4a662d2882e471664dbad58487e`  
		Last Modified: Tue, 23 Jul 2024 04:20:44 GMT  
		Size: 53.7 MB (53729987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307167e2f9dddf5502bcdb4ac15623d90fce4e4de6bbc372aa9e0100e67e9221`  
		Last Modified: Wed, 24 Jul 2024 11:26:54 GMT  
		Size: 142.4 MB (142356360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f0f9472d4c5afc739041e3153f28551b1d26a806eb5414d951aa9f19c409ea`  
		Last Modified: Wed, 07 Aug 2024 20:03:56 GMT  
		Size: 69.1 MB (69093277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8277300a9d4d9b2545d1e782a6e46eafbce145d8949310d7033196da9fb28225`  
		Last Modified: Wed, 07 Aug 2024 20:03:54 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:76fc96a215d97b06be42e78e43d7e5181ca8ab4263c58068e458a42326324f48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7060467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65a9c2bd67fdfd5e6f66cb4703427a00d4eb774915dd9c9322a091ce27e8b410`

```dockerfile
```

-	Layers:
	-	`sha256:f2f1c836f6fdf68bbdb86550675936877635f6ebcf69a1a4392fe7db31b093eb`  
		Last Modified: Wed, 07 Aug 2024 20:03:54 GMT  
		Size: 7.0 MB (7046066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0addef264c618ded9f24fcbdfb0d7edf67970426d1045288dba26f273ca432f`  
		Last Modified: Wed, 07 Aug 2024 20:03:54 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json
