## `clojure:temurin-11-tools-deps-1.12.0.1501-bookworm-slim`

```console
$ docker pull clojure@sha256:899a0e0acded7edd9c76758b70a9ba5ce01a11226dcb13708692ac32edbb5523
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1501-bookworm-slim` - linux; amd64

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
		Last Modified: Tue, 04 Feb 2025 04:27:59 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16c75b597ea9f888f5623e6f970ab403497cbe0d243f5a0ea7fb39f6a2e48fd`  
		Last Modified: Fri, 07 Feb 2025 09:07:40 GMT  
		Size: 145.6 MB (145598932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01769ce6f8941c58779852791c93cd58c520878b1afd04b332cced1c44b613cd`  
		Last Modified: Wed, 05 Feb 2025 18:17:30 GMT  
		Size: 69.5 MB (69531617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1adb767603eb77c3e6d48d196bff89a6199fc76452fa59ac1a263b9c3b00776e`  
		Last Modified: Wed, 05 Feb 2025 18:17:23 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1501-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-1.12.0.1501-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:932fb4b29b0bdcab7b1822b6db0ab8f4f92ba77e855a0aa64715547378b4f7ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.8 MB (239808892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d961452009f798f8d870f280229f8d4a43e2bfc480d12f26446e4940b6bcfe01`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 04:29:51 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f305d71243c4cf4c22bc4b182c9302eb11b39dcea5a584afbcdb527687c5af43`  
		Last Modified: Fri, 07 Feb 2025 08:59:08 GMT  
		Size: 142.4 MB (142385472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762cfb212bec5f129fa064c6183a685db68b65a68ac5e4ab3cc066bd3141c790`  
		Last Modified: Fri, 07 Feb 2025 08:59:05 GMT  
		Size: 69.4 MB (69381895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab42ba86bbe4e9cb582c3b22e7050ddbfbecd0e7444bc49ca51a710fe8ee25e`  
		Last Modified: Fri, 07 Feb 2025 09:33:41 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1501-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cfe120b4719086251ddbae3c30ac709452d149c9bbe255345b78604307a6ed8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4953515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2435889c0c56df683aecd31e4584c9875ef608c6118bffd1b6a002a98447aa3`

```dockerfile
```

-	Layers:
	-	`sha256:63a488d9fbc55d21327581c06346f3e6f768815a79f5905be04071bd0370caef`  
		Last Modified: Tue, 04 Feb 2025 23:39:07 GMT  
		Size: 4.9 MB (4939087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f2706b06475111dcbb2a8094aef17542803d537931171d235daa1761f4b6519`  
		Last Modified: Tue, 04 Feb 2025 23:39:07 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
