## `clojure:temurin-17-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:773b4881e3ef6f49ff1418965bbd1dd89b75acb0b16e43a9da9691db33202c88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c23825a18653551a3c5beed89ff9fc3e967fb50a8aec38b2aa1f75040e5945ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242311336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98885aa2757a4ea1b333515365d636154847993e78abffb3a45d37df5259ce3b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 04:27:59 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda7d9691b1137d7fa30d3ca6568a945440f210d6495114d54a9ab0ce71bb421`  
		Last Modified: Wed, 05 Feb 2025 18:10:33 GMT  
		Size: 144.6 MB (144566522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc2586c6218d31cbdcd19afe6d3239321aa0008fbc81ff077dac5d55f9a26c3`  
		Last Modified: Tue, 04 Feb 2025 22:35:19 GMT  
		Size: 69.5 MB (69531477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8678be00ef9c48f5fdf069a0e189758aa7200c45a4de6e16c7115b5a88b6e5a3`  
		Last Modified: Wed, 05 Feb 2025 18:10:21 GMT  
		Size: 608.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b820a59c6f220306c6e1c8197b9731e809d0055e62c531de78cc0d76b81cb60`  
		Last Modified: Wed, 05 Feb 2025 18:10:21 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1710468420132d43a4c797dc6e32c764922b2892d80590e8ebb27d526e636b71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4928446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590bb4c3c2f2db0f0a1c74f604563ea2a395d19d5a8c706e7640d683b78d63ce`

```dockerfile
```

-	Layers:
	-	`sha256:518e7a482b064be1479f65154337dd96f0273735d4357b7df31d993b3bb80717`  
		Last Modified: Tue, 04 Feb 2025 05:28:11 GMT  
		Size: 4.9 MB (4912567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6922d6d7f6ae8908d251ceeffc3f22682f03d72292613419578341f0bbea8cdb`  
		Last Modified: Tue, 04 Feb 2025 05:28:11 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5a8251ead214af94237bbfc25bae0f5b150bbf91dc2153d5094a29e39713f26c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240878384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee71b40cb775ce6989f83104f3cf17e4018262fea7c1d5d0babd60a81d5f6662`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 04:29:51 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ae012ff89092306c93163c5501638b4e1ea553e25181d4997dd7d40d4e9812`  
		Last Modified: Fri, 07 Feb 2025 08:23:10 GMT  
		Size: 143.5 MB (143454713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875ff187b6961c292267600747481877bdeaa7e8cc3766cdfec405c25a5d710c`  
		Last Modified: Fri, 07 Feb 2025 08:51:52 GMT  
		Size: 69.4 MB (69381754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e12c693f4d5010e798240c29b0ca5577ad533cd31d8d39cb7232e638a9c8a9d`  
		Last Modified: Thu, 06 Feb 2025 07:12:58 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd6e23bfca1792f225de5addaf714b8367e36d801634b05572b44cef84c8afe`  
		Last Modified: Thu, 06 Feb 2025 07:12:58 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0a6653f4695240181d15091d158783afd571712437b15f8a4bddb23decf138dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4934325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd471aaf86c37281262e3d8491a732b61c72f07dbbc69cd1446e785d79e94338`

```dockerfile
```

-	Layers:
	-	`sha256:87d574338771e837d44f38bdaf2db09c3144b4c3707d25c0432c6338619a42c1`  
		Last Modified: Tue, 04 Feb 2025 23:48:08 GMT  
		Size: 4.9 MB (4918328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6946c435c1fea7bf4999075942f3d5ef1422cacd3954584bd9122c109071e988`  
		Last Modified: Tue, 04 Feb 2025 23:48:07 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
