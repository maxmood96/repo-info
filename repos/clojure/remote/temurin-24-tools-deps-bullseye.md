## `clojure:temurin-24-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:7148c3094061382a19397aa3f13e0b9fa5ed3ea5704cdba89b099135f3e85e1c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:6fca8dff854596397e995e5aeffa7c8d26b7dee25670aea9da7918df8d626800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.1 MB (213096821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4287c6673d715cc1afe8ec63e207f53a41f31f123fbcaca566d6fa4e310309b9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee42e78fd78442427d7b1fd5874548153b4147c3bb4c0620b7fffe6d9992563`  
		Last Modified: Wed, 23 Apr 2025 17:16:40 GMT  
		Size: 90.0 MB (89951972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b00e61a7ba01792e529194b9f0ebe0c0a81a2c6888643a971ceea6938bcb90`  
		Last Modified: Wed, 23 Apr 2025 17:16:41 GMT  
		Size: 69.4 MB (69395276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c7f96cf7a88c1d64186418d6fdf46d57207b47bb683c7a5160eb0d9431aba6`  
		Last Modified: Wed, 23 Apr 2025 17:16:39 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38490e4e176f32735fa4b4b88c03eaba3164af2caa5fa7a7aa10e2cd92648c4a`  
		Last Modified: Wed, 23 Apr 2025 17:16:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1b0504298a8d33b9d3ffcb7e5192f842f64a34f8ced702776addefec845471ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7172961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f06b1d8957fba2b23e2ac59f4faa37a7956bf38933051f0705e3faa7251a53`

```dockerfile
```

-	Layers:
	-	`sha256:0d3d00374870c1dfa411bd486a000a905f2a6881c435683a5f5166957ea07bdb`  
		Last Modified: Wed, 23 Apr 2025 17:16:40 GMT  
		Size: 7.2 MB (7157147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63e73cda32f7939a73b8e8108f989b45206d263378b46f9d913d960fcb89d643`  
		Last Modified: Wed, 23 Apr 2025 17:16:40 GMT  
		Size: 15.8 KB (15814 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c527292736c5824eac5376bce9ecf68b60cbc35e2dab2566b06e96c822ea8483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.9 MB (210877652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d331188b7521c4182f6f5c806cee6b92320079a32b8a5770862ede51c6466c43`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67679d6635369ee795534b11343dd855f46be72a101f3e77e223b4db82f4cada`  
		Last Modified: Wed, 09 Apr 2025 17:49:33 GMT  
		Size: 89.1 MB (89092739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8141786d9e710d77e2fab49c16425b3ccceb0fd12331f32fb32fc6332cb9b5bb`  
		Last Modified: Wed, 09 Apr 2025 17:53:29 GMT  
		Size: 69.5 MB (69529645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04cfbe3e0289982f5399d7a5a1e24d932d11ad9fd5ab29fa06a5ebf849190bf`  
		Last Modified: Wed, 09 Apr 2025 17:53:27 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c5213ba6ba2a1872acc0b66c701950206ea8b74db0c03458f9b0adb2348e98`  
		Last Modified: Wed, 09 Apr 2025 17:53:27 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:bd930ce4533e9d6ab9f0129dc46cefb39f5d3f53845e1208667b40d2e06b8309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7178161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0752f74a09752ae68e885489b1d49cca4dbf2d00f746adac8a6dfd65cf5c24`

```dockerfile
```

-	Layers:
	-	`sha256:ee1ed05a86b15d621ca5e3ae15fbff65be507b9840cc35057148f243d554673c`  
		Last Modified: Wed, 09 Apr 2025 17:53:30 GMT  
		Size: 7.2 MB (7162229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5ae1ccb22bd9bc5b9289edf64681c45f8e2c33e7b6213363dd27cfaf63a7277`  
		Last Modified: Wed, 09 Apr 2025 17:53:27 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json
