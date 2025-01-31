## `clojure:temurin-8-bookworm`

```console
$ docker pull clojure@sha256:f2590f3b668f7d8ed7af835761295c17885b44b67690f6f2dd692b60ce84e4a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:794c63f1fd906aa322e64d1e92f134de90b1e52b009d9c0eb3ffe191518a377f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184195578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9faa6c6a4314ad271feacf5e1741e5d922716036a4487cd33602cba26b3b8b31`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1061dde6977c4c383b141840856cc97d23887ae36756ad018f21f7cd6c8c1e9`  
		Last Modified: Fri, 31 Jan 2025 02:13:56 GMT  
		Size: 54.7 MB (54721244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c07d3541b90e0b5e5fed12fa024a01f23e2c86169065e6f3853957e1150b74e`  
		Last Modified: Fri, 31 Jan 2025 02:13:57 GMT  
		Size: 81.0 MB (80993726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69ebce3ef19992e7345fd0e7be3ced6666c9bb3dd2ebcd687bfc6887cd2ae8d`  
		Last Modified: Fri, 31 Jan 2025 02:13:56 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f8fc7a97595c80edd138394e2f01f5fa6d6017dda6c6203fffe281eebde41596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7306925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a851c89402011959ea32de7590e278aa9e0a4c8f20834b6a5615c93f3401ab`

```dockerfile
```

-	Layers:
	-	`sha256:cc97c44067d6da08c5de6cb856f53a0b4e91da27fd68a4865d3bfdd39cc622d0`  
		Last Modified: Fri, 31 Jan 2025 02:13:56 GMT  
		Size: 7.3 MB (7292688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18b9a17f36b3be0b733a467f082c2aaf9b49c6c4cb2c9617b4806d2527facb5e`  
		Last Modified: Fri, 31 Jan 2025 02:13:56 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:741d212b169013e7c2fcfdedcbe4c05a1e4fe5f60bd125e333d5a2888aed424d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (182975957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe8a49661a6b2f92306ff08c831a9bc95eb2052b4a9e1f67ffa2f9038a06d87`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a648462208ab1df73c5399bb9e6f0d3bcd3dede4cd630624767d7c11a567b1a`  
		Last Modified: Fri, 31 Jan 2025 04:56:33 GMT  
		Size: 53.8 MB (53822754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d2636c46ed3a58376d5a2efabf581c50e9ebadc6d1b45990434731bbe6974d`  
		Last Modified: Fri, 31 Jan 2025 04:56:34 GMT  
		Size: 80.8 MB (80845661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a30f91d27b8ff2ba63bd2360efd43268e38ce892bf890022bea4b40b3693bbb`  
		Last Modified: Fri, 31 Jan 2025 04:56:32 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c15a60b1b112bdac3490a336cf9478773c1b9be213fdfc95f9873af40d50e957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7313504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4feecb5de0b99a4268b62a50bee4174be3266ca9eff734ee64202535d8e72c`

```dockerfile
```

-	Layers:
	-	`sha256:d38745e5f4b1dcb4d339c11ecef7aa2dde90ad8da57e8b5727238b100b9afccb`  
		Last Modified: Fri, 31 Jan 2025 04:56:32 GMT  
		Size: 7.3 MB (7299149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a15a87045ce6394793cd28d588372b9354f24517c6eefb7c8a4361063ca99db`  
		Last Modified: Fri, 31 Jan 2025 04:56:32 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json
