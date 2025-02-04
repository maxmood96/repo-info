## `clojure:temurin-8-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:381941d6fc973f1c9bac040986629824265417ed2b89e510d9cf3db2853edb80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; amd64

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

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

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

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7dc1edcc1797fe025508368eb87b2d13e1a4d99c720b73f25fbcfc353b60c9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141477288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd96326effc9aa4bb211b729f5afc0b3f3b866bf2dfec2c1274cae3c8b86d416`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
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
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db478d01bea4643df26b64fe9a50f7c84edd495d82622ff66034cebe48d79075`  
		Last Modified: Fri, 31 Jan 2025 04:54:13 GMT  
		Size: 53.8 MB (53822757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e81ba0776792447a20809fcc28221a325e6d210c5ad8896bee22db2ca96066`  
		Last Modified: Fri, 31 Jan 2025 04:58:50 GMT  
		Size: 58.9 MB (58908973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dabe1bfa84f99d6ac26fdc102c8eaf74031b4282af4c2e67d6266854c9f30d3`  
		Last Modified: Fri, 31 Jan 2025 04:58:47 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5a468a1db891d7040cbd0c061e6fbc0e6f76dea8352042c38c49a796bf886ad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83bb82595bd8010dc566482ca8beeb1037b7411fbfff414318b820555dc97d0d`

```dockerfile
```

-	Layers:
	-	`sha256:4c40d7d2a9ccfd07d879c8eb15ed2f0cacd8ae051d99816ff3268520b459886a`  
		Last Modified: Fri, 31 Jan 2025 04:58:48 GMT  
		Size: 5.2 MB (5245107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b223e12446229fefe1ebd624a306e11a24c19a9568877764d71a0f21fe498a9e`  
		Last Modified: Fri, 31 Jan 2025 04:58:47 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json
