## `clojure:temurin-8-tools-deps-1.12.0.1501-bookworm`

```console
$ docker pull clojure@sha256:0404e930cc77d8c0ecb69f1099f4fb5970357364c14fde90d0894eb42da2b561
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1501-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:58d5355c599eb822d44e0a7cf0115d61b045240ed96c84d4128d8efd867d45c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184195577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d952945f06ce4bc563eecd7bcbf27f0dc5e95834af01f9ac075bed830d98f4`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 01:36:22 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29095b55e076344a3bbca81eb22a309e8665171416c55854c07118e296e1447f`  
		Last Modified: Tue, 04 Feb 2025 05:27:47 GMT  
		Size: 54.7 MB (54721258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c9fe67c6daa5241ebbc1c4c6642b4fc04176ccdffec207a564f5e84bd13984`  
		Last Modified: Tue, 04 Feb 2025 05:27:50 GMT  
		Size: 81.0 MB (80993987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4332715fbd8b7b773fc7b7d227d14b858703e74e9f04c023bf9d60f13cece2f7`  
		Last Modified: Tue, 04 Feb 2025 05:27:46 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1501-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c75feb9b654eec772f8c0bcb2ac6dff3dfb8b93d1563d61b1b5bbeae220194e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7306925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:210cda7d221ab2a56ec32945b8f1ff8fb2a244c6deecf41e0c293e1a8d01cef2`

```dockerfile
```

-	Layers:
	-	`sha256:2e9b9e797c3e4cfd87c9463639b1fdc40c8b4cc9fca3307966504c04d575ac2c`  
		Last Modified: Tue, 04 Feb 2025 05:27:49 GMT  
		Size: 7.3 MB (7292688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:019760b00b768c24f7f1025894045a0408a53e593b8bfa0fa7297db7273e4996`  
		Last Modified: Tue, 04 Feb 2025 05:27:49 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1501-bookworm` - linux; arm64 variant v8

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

### `clojure:temurin-8-tools-deps-1.12.0.1501-bookworm` - unknown; unknown

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
