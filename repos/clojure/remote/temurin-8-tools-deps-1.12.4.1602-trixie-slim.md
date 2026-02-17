## `clojure:temurin-8-tools-deps-1.12.4.1602-trixie-slim`

```console
$ docker pull clojure@sha256:7942521338cfe34265bfe46391b0685c489b5690b340724e9ae90d4168d977d3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.4.1602-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0301c0748bd001ccc9825ce5747b4183b1268c53dc4628ddd18207ee48ccf537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156945207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7349c78379b27c5461a34a74698a38178e67286274c668708b8ecc14278abd82`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 21:41:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:41:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:41:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:41:04 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:41:04 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:41:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:41:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:41:23 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fcf5506bc8be628b41fb02204f7f8bf34b1159092ca8b512b7bdb75c9a5027`  
		Last Modified: Tue, 17 Feb 2026 21:41:44 GMT  
		Size: 55.2 MB (55170146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9d3b142d676b9ea9044d50262d68a3ce125ab3736cdfbae9194c897233c478`  
		Last Modified: Tue, 17 Feb 2026 21:41:44 GMT  
		Size: 72.0 MB (71995820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afaa4cdce375267290c95e7cd080d1305646a4800f8658377427de1d6c3a2148`  
		Last Modified: Tue, 17 Feb 2026 21:41:41 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:451c91bd39b9dbaac103c9205061ecae5d95b8f808863ba0b048f7dbf9f8b02c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5392765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:735d21e4788c1f7369840edc0447916649cad6f466caa608327f5afd7f9e1ade`

```dockerfile
```

-	Layers:
	-	`sha256:91d294f7e845cd87e8c3897700aba32dbe663c5c4c3d8ee6038f3fbb6d105268`  
		Last Modified: Tue, 17 Feb 2026 21:41:42 GMT  
		Size: 5.4 MB (5378538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a15ec4ce6623a6cdeaaa389dcee53723f4ef8908ae00601dc14eb60a4ab6f9d1`  
		Last Modified: Tue, 17 Feb 2026 21:41:41 GMT  
		Size: 14.2 KB (14227 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1602-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b850954b5f1294e0ddd69cf16934beada8127af31497dd55cdc5db42d16c7f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156198912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d12e2705d50cb2bf5d698ae157558b4087ce308f0b38c818bf1f3f4d1251945d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 21:40:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:40:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:40:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:40:55 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:40:55 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:41:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:41:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:41:14 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8b4e73a04751df016eb1618cdfbd6f3c73fc231666074206fd0d41d09de71c`  
		Last Modified: Tue, 17 Feb 2026 21:41:36 GMT  
		Size: 54.3 MB (54251630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f278dabc413648d6d8063530d3b32b5fefd2ee14a9ca8a167ca37e32049ebd3b`  
		Last Modified: Tue, 17 Feb 2026 21:41:36 GMT  
		Size: 71.8 MB (71806571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fb281442ec1838d8faab622c91716e6aa5c331363b0eb4fbeb58b8ebcdb173`  
		Last Modified: Tue, 17 Feb 2026 21:41:33 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d6f0005bfcafdaf9f2e9ea00ad3d46d31cfedb145d7e763553fe279f82d93cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5399353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7677c424e7811a9c27974e69bae2609c00d92384df010c856ccbad38745926`

```dockerfile
```

-	Layers:
	-	`sha256:bbdfd83fcc3dc54111656c60ad4b466e7d8677a7c04e273073eb7de2d28688bc`  
		Last Modified: Tue, 17 Feb 2026 21:41:34 GMT  
		Size: 5.4 MB (5385007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a21f8e94c11d743444325d28d1b833daec4d1e11b9d29b79f488006d0bd82fcf`  
		Last Modified: Tue, 17 Feb 2026 21:41:33 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1602-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:91f0d0e149e4d16d54ebc074861c9c57dea17a0e30702ebc9746c34a09babc8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.6 MB (163641758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2664422fe25744d74aa4c7187c585f55d35bc9cd78de34b3e24b56811fc6c979`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Fri, 06 Feb 2026 00:00:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:00:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:00:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:00:11 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Fri, 06 Feb 2026 00:00:12 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:07:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:07:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:07:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e89dcc3b95f00f17f7b2d6872744c6220cb1fbbd573cd216d9413691c73b51c`  
		Last Modified: Fri, 06 Feb 2026 00:02:21 GMT  
		Size: 52.7 MB (52650394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ccfc408e8ff54ba791a45ce0440d8c1e26e720d22e4eaf8ee74a5fb7f0f675f`  
		Last Modified: Fri, 06 Feb 2026 00:08:51 GMT  
		Size: 77.4 MB (77390534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26c858ae7504b91d032e21c47b2803e68ab2e6aacb9b231c2363351a693b12c`  
		Last Modified: Fri, 06 Feb 2026 00:08:49 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7c525aa42f361a02faa7c3b1be9b71b337134687f26cb083d1208b94cd6d223d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565e9ead29647a58810ab4eb876d7a26f976f5e132fad779658aa4dab86a50ac`

```dockerfile
```

-	Layers:
	-	`sha256:8a242450eeeacba4751e9d00ed92234a66ad768fdc9729fe1ca5df82d5ff84d1`  
		Last Modified: Fri, 06 Feb 2026 00:08:49 GMT  
		Size: 5.4 MB (5383504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4f15d0eeaf67385556c42044b5b28bc49a25b85e81ac75ff1c21f9ae74ee5cb`  
		Last Modified: Fri, 06 Feb 2026 00:08:49 GMT  
		Size: 14.3 KB (14276 bytes)  
		MIME: application/vnd.in-toto+json
