## `clojure:temurin-8-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:3da64d56de1a6f38116ab262d9aadf21a7fc9f1c0f948f70c521462decddd4ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:c62e51db95015c831c123a7670140931a2707a2bdaf285bcb7919ffa9e1c05d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184205854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a366ea6ab00a958dd04013b01b6c1a923a03845b4ae12348c12a84bb42a1eb19`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c287d3f7330c1ddf05d2acfe79d2a3dfd3ad36ad04df90754bc4c10ed7c350`  
		Last Modified: Tue, 08 Apr 2025 01:49:01 GMT  
		Size: 54.7 MB (54721234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331513ce85fabcb5aa02b1637908eb2d30dd8a2e5da2c6306d1f5d34e40ebdd1`  
		Last Modified: Tue, 08 Apr 2025 01:49:01 GMT  
		Size: 81.0 MB (80993433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19799096d863bcff71297c2649acce02dcdaed75f2bb3a613f4653603e12636`  
		Last Modified: Tue, 08 Apr 2025 01:48:59 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:dc887f58ca81fd824ba3ca6d22ff73941636dde628ffcc0c273e4feb0aadd352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7308323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc2901503d6703cccf7c6895941b1d5c60ff314a5fb050d7f943505adf50bbd2`

```dockerfile
```

-	Layers:
	-	`sha256:0fcdb22c7bf29ed33ff26302241867175d8eef858be357ec80b2120d14509df2`  
		Last Modified: Tue, 08 Apr 2025 01:48:59 GMT  
		Size: 7.3 MB (7294086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09dc24838fdaeaccbdfd6795860e88fba3751239099995116953bff511c4f3cd`  
		Last Modified: Tue, 08 Apr 2025 01:48:59 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:519bcc87fa7462870bd5d8e449ebbb573b8b07d475a11e098e64414afd2a230a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (182993466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1457b00b73239aa2fdb8a838288dfab1228371fea4a2c378d3c01ee29144be4a`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b240c2fa4760e5dc778efa96856045fef5b294ed0750d15ab22a3c4c8696edb`  
		Last Modified: Tue, 08 Apr 2025 11:12:10 GMT  
		Size: 53.8 MB (53822770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a241b13489ae911abd7b38ad0c18a21cb65433a1e1e1a88a57d9beb12857605e`  
		Last Modified: Tue, 08 Apr 2025 11:15:27 GMT  
		Size: 80.8 MB (80842581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c622ffc89631111ce99300379e5f4457ad9bdb4df25e733f455361d3b330bf7a`  
		Last Modified: Tue, 08 Apr 2025 11:15:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:01896e6e9b09dacdbe556dc9673cc20ccfa07aafdd6bb835f545e98ba7c97413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7314902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fcaf80c170c15473954aa5ec0a71525d711ff0ee5ff8f22fdef1dd7295d8f84`

```dockerfile
```

-	Layers:
	-	`sha256:7c8c0d38e400d30912d0f995b25407c14062baddc57f2a42c536d8a8edc8acb4`  
		Last Modified: Tue, 08 Apr 2025 11:15:25 GMT  
		Size: 7.3 MB (7300547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:549690cdcc8a50d406f31f1eccedaf766bd475e3eb3aa170c128d3c8879d04e6`  
		Last Modified: Tue, 08 Apr 2025 11:15:24 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json
