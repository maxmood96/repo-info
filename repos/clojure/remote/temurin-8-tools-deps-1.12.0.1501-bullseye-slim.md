## `clojure:temurin-8-tools-deps-1.12.0.1501-bullseye-slim`

```console
$ docker pull clojure@sha256:a9fd20afcc52fa8f64c8333d3934c1d478409d060c46abd2ddd4ad75bbdeeb44
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1501-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:40802b8e7517b00ff2ee01d91786163339b4c871f9cf971ecd3f42d901969853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143762461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8e4b611e7046633186de91b403c278fdd978c9ba923f37c283d20db56c089fe`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f84b2930787618cdc759501b991fd54ac3c2b83b0aeaec33a78293c1df2010`  
		Last Modified: Tue, 04 Feb 2025 05:27:50 GMT  
		Size: 54.7 MB (54721258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b943942cdb26f98b1f280fbc446719e6899c8e53b61ebd961790abdd03750fed`  
		Last Modified: Tue, 04 Feb 2025 05:27:50 GMT  
		Size: 58.8 MB (58787969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c94f511bb0b3e182aba2b7c20b01466275ff449565b8e3685df86b119c3ca7`  
		Last Modified: Tue, 04 Feb 2025 05:27:49 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1501-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e142dd4925d410e243f4eb770146f4fc3cdb4ada3fb0b207bc91da6bee389a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5252967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5b775665cf3a4991a9873e2602e304ab61cac35c9c7866b791e7250b9e3bc59`

```dockerfile
```

-	Layers:
	-	`sha256:873ee2f621887f8a833101fcd6e685603966c2120353b0f7c43a89cdc487ea4a`  
		Last Modified: Tue, 04 Feb 2025 05:27:49 GMT  
		Size: 5.2 MB (5238677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc6b96eee67227e76f4fb51040d4b5089e89154d574572094a372e3654434dd0`  
		Last Modified: Tue, 04 Feb 2025 05:27:49 GMT  
		Size: 14.3 KB (14290 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1501-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6f9f6cf3e2cee0bb3fb4c9d614fbf64b749dd6cfc95242e6cbf49c160e29d8d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141477198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a88015792eab0a8bc03b316454745d8b27503d544817adec5748d54b2fa698`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:9225a2a808e874449ee822a282882a3c331aad2f5093c1062e16494d8bce3e9a`  
		Last Modified: Tue, 04 Feb 2025 01:38:25 GMT  
		Size: 28.7 MB (28744810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbfecaf30e64df0a0ebb56cfcbcbb62350f903855a9adb4e256a20cd7116daa`  
		Last Modified: Tue, 04 Feb 2025 23:26:41 GMT  
		Size: 53.8 MB (53822776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd520f598177c77497be9087aeb0b1643e26dbb2f3c8e9b8dab38adf4f25e3ab`  
		Last Modified: Tue, 04 Feb 2025 23:31:11 GMT  
		Size: 58.9 MB (58908968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358b3dcbcb800f528c2d6f673af25befcb5887e59791e9173cf54e3f0cc5388e`  
		Last Modified: Tue, 04 Feb 2025 23:31:09 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1501-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e0b91e6677fee868d19c122c9d2be6ae086e811e678dd160265a8ef1ddf9f83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01cb313db198110d69e46f6f1397efe846ac343dc95fcc30ed66329441bfa991`

```dockerfile
```

-	Layers:
	-	`sha256:b26a44cb4d7dd6b4b404ff29a389a83c8526d3a625fdb9397bb766aa3690413c`  
		Last Modified: Tue, 04 Feb 2025 23:31:10 GMT  
		Size: 5.2 MB (5245107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43a9e733110c1c8f0ab92571d2583cc4e619d0e74430b7a7c5cabfc126da4aae`  
		Last Modified: Tue, 04 Feb 2025 23:31:09 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json
