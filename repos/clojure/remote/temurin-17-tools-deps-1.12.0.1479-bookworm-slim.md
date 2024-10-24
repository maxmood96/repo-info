## `clojure:temurin-17-tools-deps-1.12.0.1479-bookworm-slim`

```console
$ docker pull clojure@sha256:d5a9c6e5b43cf8d18ed4c1ce83c22aa408ecbbfb29bd84d7310834a05e358ce3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1479-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:19ce4d521b63c6ab9d17b3268b89a4b0e2f1b1d6c4e0a831e7dbec623ee504d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243144774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c365c5dca73eb75fcab21c43057065f3a9c333eebaa29f328c6eaf5c45a8f6de`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d1829db38209e0dcaea7cede81a02a792e370d5738c2ee01ce49e4072203a7`  
		Last Modified: Thu, 24 Oct 2024 02:00:21 GMT  
		Size: 144.5 MB (144534837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f05a5d44f3ca4b285f65049440aa0657b7b3c293fbe17aac2187775c7d7cd5d`  
		Last Modified: Thu, 24 Oct 2024 02:00:21 GMT  
		Size: 69.5 MB (69482609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70677d4a5febc61bfc6aa4d8968425f083b67b5625b3b9c6655d107b10cad94`  
		Last Modified: Thu, 24 Oct 2024 02:00:20 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da61c82ee9205a9b5497541abdc5148061b3f4b2a66112508ee8979c49738b03`  
		Last Modified: Thu, 24 Oct 2024 02:00:19 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:af936620913f8b170c0a677321af5b166b6eb6f4eb8d4e27c39d85b1ab46cd2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4936275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99f46f92abc3b678d9d8a27311340b27b54067be0009fa3b69359b5b1404a2d8`

```dockerfile
```

-	Layers:
	-	`sha256:9c4f5aafdb1c12fa557ff15a4e699d61bf66b5e764a06ace2108a09ba13d29bd`  
		Last Modified: Thu, 24 Oct 2024 02:00:20 GMT  
		Size: 4.9 MB (4920592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e85d15bbd78fa97f3f13e62631822fb323fa7ccd94d46fb5dbca047152d5a64`  
		Last Modified: Thu, 24 Oct 2024 02:00:20 GMT  
		Size: 15.7 KB (15683 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1479-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fb9d8c23e2a1ce869e88bb1b441892ca3aa35e4df253752ab6058d2dc3094985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242462082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44fb865b2aaa315b7483bb94da81bc8619d7edb79b7f3666548ce85d28ce4f8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3d0b3b90758f2da033069b4131178bf4a6c1fd6b5c07637d01ad797ebbc059`  
		Last Modified: Sat, 19 Oct 2024 12:01:24 GMT  
		Size: 144.0 MB (143959478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19a53bede711a73d711f78a5875568f585e33a1680fc0502989caa1755aabc6`  
		Last Modified: Sat, 19 Oct 2024 12:07:06 GMT  
		Size: 69.3 MB (69345220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9384ae5514225f769fbaec02e8f68ab620696eda9a307d106d721964af5c7e46`  
		Last Modified: Sat, 19 Oct 2024 12:07:04 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addec6defb3687a06501984a9f0acfe51c068356ccaba0a5104cc5cdc78db699`  
		Last Modified: Sat, 19 Oct 2024 12:07:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:935fae79d57879929b2e392544ce5da71b0fe9df544326a237e39fecf317ca2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4941553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c81393935f2afbee6bc7d3fb21903e174ce869eddb65fba68bb4547db4fe0ed`

```dockerfile
```

-	Layers:
	-	`sha256:752de58dd36660cbf8e0aade1a9aae2aed8d493cc78b45f441592bba0961cd93`  
		Last Modified: Sat, 19 Oct 2024 12:07:04 GMT  
		Size: 4.9 MB (4925722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e217df0c8d8f5e1faf9673f095f8f9aba92f099c9acbac503d373aef98acc8b`  
		Last Modified: Sat, 19 Oct 2024 12:07:03 GMT  
		Size: 15.8 KB (15831 bytes)  
		MIME: application/vnd.in-toto+json
