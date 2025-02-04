## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:cc62447b5273fdf163cea2c1d2a0a054470ea545f17950efd9e092304ed7ce02
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2c9e3fe45357d203b1bb3974562e21e73a03769b0a2bd57556c89a4efaba3afc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243343496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e2677581f7428ccafb86ee9704a713c2b5950d989f56d3878d548f24b3e7488`
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
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16c75b597ea9f888f5623e6f970ab403497cbe0d243f5a0ea7fb39f6a2e48fd`  
		Last Modified: Tue, 04 Feb 2025 05:28:08 GMT  
		Size: 145.6 MB (145598932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01769ce6f8941c58779852791c93cd58c520878b1afd04b332cced1c44b613cd`  
		Last Modified: Tue, 04 Feb 2025 05:28:07 GMT  
		Size: 69.5 MB (69531617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1adb767603eb77c3e6d48d196bff89a6199fc76452fa59ac1a263b9c3b00776e`  
		Last Modified: Tue, 04 Feb 2025 05:28:06 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:db93f4f257615364190c1ac01e6a9179afa55e89e13d0265b5530286837bc367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4947018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:052a2ca3931051480ae26f5453496ebc86a0376705c30fc95dc90b02dfb336cd`

```dockerfile
```

-	Layers:
	-	`sha256:803c8f9c17086802faba5861cc9228858a36eddaf6bfb1ba3e8a866dd839b7c1`  
		Last Modified: Tue, 04 Feb 2025 05:28:06 GMT  
		Size: 4.9 MB (4932708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f59239a0c36db51090d9ca77eca3a1c8835c3913d57caf890266420f5bd0a00`  
		Last Modified: Tue, 04 Feb 2025 05:28:06 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:59499aaf9ac42d48533372f4f42010e52630d6d1edd6e9c59c0dd7c651fd91eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.8 MB (239808949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6579010991a009a5e992d42233be97a8dbcdbccf9c86c182d456444e327c87`
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
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9060b028d06a8fb22c11eb150c07167cbc0d14bcb2ea774f5d7146748ed43f`  
		Last Modified: Fri, 31 Jan 2025 05:02:00 GMT  
		Size: 142.4 MB (142385501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bce7986d1c8a409734dfbb6960948c461f101b74dace29dd180c9b7985d258a`  
		Last Modified: Fri, 31 Jan 2025 05:06:28 GMT  
		Size: 69.4 MB (69381773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff1ebce4ef9db6d767f57999a2ecc75b9204b5fb50efdfcf6bdae9d01a61b8d`  
		Last Modified: Fri, 31 Jan 2025 05:06:25 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2eb5f9b6357f7bd1b07f391dc8998ada61128437c18c6abcddb11be141107b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4953515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81cf6bbf7c6c256584f273aa3c6af79d43ab3e4b93dc88a396665662d3363953`

```dockerfile
```

-	Layers:
	-	`sha256:9b729db41ce302fd05470ab4e07b7ce0a2aec96dde90740bcc259bf6f26cb461`  
		Last Modified: Fri, 31 Jan 2025 05:06:26 GMT  
		Size: 4.9 MB (4939087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:279fb210626d7ee5f01d80a11e9793faa0efa7fa8356e2aa28ec06c9c04e58de`  
		Last Modified: Fri, 31 Jan 2025 05:06:25 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
