## `clojure:temurin-21-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:3a38dd2a764c7fa4f5168e442feeff5da9589c2575d2eaee2e19611494bacc7b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4d4299d75e275e36618b49b424c2ee01e8762e721f25770e2244620a3d178b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246578474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edc0700c103f7fd9156ab864eb301acff60c62a43740ece8d142597101a806d4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
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
	-	`sha256:6c87eefc1f428634061bcdc9ec95ccceecd7c7475d35a777479af83f64ee6915`  
		Last Modified: Tue, 24 Dec 2024 21:32:32 GMT  
		Size: 30.3 MB (30252643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e486320fe9275f800ba765088eb9bf1bdac5f9b6ff93020c2b5ecd0042d271c9`  
		Last Modified: Tue, 24 Dec 2024 22:38:35 GMT  
		Size: 157.6 MB (157568719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7865f6b816e93033eddb74e92643706cf9431769d3f1660f95bbcc94c17235`  
		Size: 58.8 MB (58756073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd22f553f7adb7eafdd5d75a4a7f203d706b2ed2fce2a53db89be0966fc1c9a`  
		Last Modified: Tue, 24 Dec 2024 22:38:33 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f4eca7777e5c1d115423ed44ebe32c64d02b8a4a9148109d6543508e608442`  
		Last Modified: Tue, 24 Dec 2024 22:38:33 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b81d67bb2f6a0af426f3263c7bb2c4d61f725ff95893150ff6ff2f7896bdb435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1840f9b9ff430722d41aa66bf0cda0db745c4a5dc3c7a6d2616baf8741609c4f`

```dockerfile
```

-	Layers:
	-	`sha256:2106408862ced503f5fbcda661c9cc2411b92a0c4b844a300f3bd16232e3e798`  
		Last Modified: Tue, 24 Dec 2024 22:38:33 GMT  
		Size: 5.1 MB (5120805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72f491a218a4ff4563c8e1fb35737e0d34f5b8e24dc7dcd01934a6f04e63e639`  
		Last Modified: Tue, 24 Dec 2024 22:38:33 GMT  
		Size: 16.6 KB (16574 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9c301c7e91210cc4f320847b3988d0dc2eba23d085350b767ce48529d7ceb0f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243419123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b643359d4e50cbc087fd2fc1ef3427633ab0c5e0f29e3055573da67b52afab`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
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
	-	`sha256:879a6187682fc52c69294a2f450abdb54e257a50e8133ec6e89cb140345be6ce`  
		Last Modified: Tue, 24 Dec 2024 21:34:50 GMT  
		Size: 28.7 MB (28744853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416a3a2fd8cd9807260966b02586a95c093ce6d1bd3085e2276d72f97ddf05cb`  
		Last Modified: Wed, 25 Dec 2024 07:33:18 GMT  
		Size: 155.8 MB (155793154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def59cec6258dc4af97b9e305c06ca12dd638e778578e4c343715e97d0d0dfa1`  
		Last Modified: Wed, 25 Dec 2024 07:36:05 GMT  
		Size: 58.9 MB (58880080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a645e0dcd915b1761ffcb05ead2a011a5043aa85a8cd72d56b1d360d6117ca`  
		Last Modified: Wed, 25 Dec 2024 07:36:03 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56bde6987f1e224d832a6e114b31be385aabcb933dc58d1cafc42791caf34b14`  
		Last Modified: Wed, 25 Dec 2024 07:36:03 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e055217d70f8a042132e3ee064cdb7ad61ed72da0a0ae0f086bf62ec72edd226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5143277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e003246165d05e3d8f0c2f4131ee0656230943638d6c482576c4a63c5405bd3`

```dockerfile
```

-	Layers:
	-	`sha256:296c7be618cbfda1245e99567e1ef439955a154f7e6077d94f028c89811a7f24`  
		Last Modified: Wed, 25 Dec 2024 07:36:04 GMT  
		Size: 5.1 MB (5126561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f71d7919f9d2752a4e6b738be4c3cd3da763eaed37052035f86887670efd9f26`  
		Last Modified: Wed, 25 Dec 2024 07:36:03 GMT  
		Size: 16.7 KB (16716 bytes)  
		MIME: application/vnd.in-toto+json
