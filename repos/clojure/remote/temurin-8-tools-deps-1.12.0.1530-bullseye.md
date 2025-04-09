## `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye`

```console
$ docker pull clojure@sha256:da477af03727402fc294e11ef63f8cc8859bd02f7aa50f2c84a390347fa1be38
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:f22daf7e0cb388fb75e10ef29a48ecaa7dde8312f14575185a135204f0737a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177865110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60e2caab2f2d13bbe248e631e27c8e0cae9a1906f5b05f938f0eead4374ca26`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9caa446d6bb2207a2f85b620687c9451ad4299d7ace6427e233ba4cd566998`  
		Last Modified: Wed, 09 Apr 2025 02:18:17 GMT  
		Size: 54.7 MB (54721225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7fced4cb913ce4885d1672ed9bfd732e44ec9309068afbc07d1b0836785005`  
		Last Modified: Wed, 09 Apr 2025 02:18:18 GMT  
		Size: 69.4 MB (69394708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35a70f018095522da05a9962332bbd96669ea6537cfe75325222ae87405a96f`  
		Last Modified: Wed, 09 Apr 2025 02:18:15 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:be3a34938968e4cc4a6aba050fb87555c29db46ccd7ff78b33a0bf777461fdf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7342348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07723a134bb56a4b223298ba280d0806a97f6899b0f4a1c765f671c92a97ff4`

```dockerfile
```

-	Layers:
	-	`sha256:bbccfc63b008a3952f273fab42568a25c0d95ca2a9e292c37efb37031121e01b`  
		Last Modified: Wed, 09 Apr 2025 02:18:15 GMT  
		Size: 7.3 MB (7328111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7b1b1e326132570f991d1daa6a9722380560b7420851163563ec24612d5be24`  
		Last Modified: Wed, 09 Apr 2025 02:18:14 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a0a0b3f0d920c04eb40c2211def3192acc0fc0bdd688f41b628e4daac693a7b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.6 MB (175607362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba696ac061cb0c91b23a69043ec0c35d65a535ad2969342ccc201f8fa4baa82`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ed3c3095e037dcd3f9d0412720b3f9d97adc708c3eb9bcf47590225cb6ba6f`  
		Last Modified: Wed, 09 Apr 2025 17:13:13 GMT  
		Size: 53.8 MB (53822769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34092dc2461bcb3831495c1ba70141f831b66ce92bf1d133f861ba63d4785356`  
		Last Modified: Wed, 09 Apr 2025 17:17:46 GMT  
		Size: 69.5 MB (69529724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11454e28439357d483139c45b2fc48c70bac65250d2a33ef8900f2b30b5d3ed8`  
		Last Modified: Wed, 09 Apr 2025 17:17:44 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:bf760e6e7186454907e9f5e00a860acce6fcbb04af91658122b96650127bcae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7348263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:402e7c52358bbf566064de5bb027e1235f49749d3e5978693d512a4ecf446989`

```dockerfile
```

-	Layers:
	-	`sha256:7fd6a18d8a41bed3032aac74256024e4a36ea2d44129795cf734e9d3d4f5d61d`  
		Last Modified: Wed, 09 Apr 2025 17:17:44 GMT  
		Size: 7.3 MB (7333908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cabb721a4cab1ba300182e4dfa0afd89f00e12e03753e0b7a7b9d6980820018`  
		Last Modified: Wed, 09 Apr 2025 17:17:44 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json
