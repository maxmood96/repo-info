## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:937cee866c7369a4da6f4fba151e166c672528ec8ef7e8c6bfd17a7581e1dc53
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ec483cfb30b68c89ad2b6d6737c0b84c1f35cd9e4664537a0110051c5d7400c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235360153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f65401ccb35c50b42625f92ce550614af3f89f6644e9aea3a3e4cdb266ea9c2`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da5b7ff8cb33da28e13196aa5b2660131fd8eb4018207d2998ffcd1d9862ef4`  
		Last Modified: Thu, 13 Jun 2024 18:14:08 GMT  
		Size: 145.5 MB (145505162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d8694129088ce58f6d621cfb1ebfba821d1c7d861a32dad86f49542a3dc19c`  
		Last Modified: Thu, 13 Jun 2024 18:14:07 GMT  
		Size: 58.4 MB (58420306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c1c7d8245c7b06a7aa56febebf66ef12311d7c2a88d4a872e548324b95e008`  
		Last Modified: Thu, 13 Jun 2024 18:14:06 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9258159a23dfd89ec815828abf342a53ef25fcb3dddb21d3c128066b177dafcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4923170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:373c1ceba9692375a203917d979dfba0c69d9c7fb1a2e1f3919055aa6f9a4853`

```dockerfile
```

-	Layers:
	-	`sha256:4e1e80a9cb5ad05e4c75e74adf8bfd413b1041562afe481f16d666de5a05b265`  
		Last Modified: Thu, 13 Jun 2024 18:14:06 GMT  
		Size: 4.9 MB (4909233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95e13ab313bc099717585c25be164566651b4800b2bfd6530a50e58a1fe8376b`  
		Last Modified: Thu, 13 Jun 2024 18:14:06 GMT  
		Size: 13.9 KB (13937 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5cb4d4b804a96e1c047ae949477198150864832f4af765e38eafd4046c3c3d7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230931826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253e10b4fdc49d6393579db542920493b2a1bc6bb2d28dd8a4b59e00f70b9c04`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5737b1460bc8700dc97acb941195e47f2f3d16b9162522c09d5187556fa3189a`  
		Last Modified: Thu, 13 Jun 2024 11:30:48 GMT  
		Size: 142.3 MB (142304050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0794c5acb4a7a4be257025cd6ae06fa3d1b01debe26cc3c73db14acd5331ae94`  
		Last Modified: Thu, 13 Jun 2024 11:34:23 GMT  
		Size: 58.5 MB (58540154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b788d12b968a713c02f38c0b49061ca606ac1a19b7bbc3d1061a1b863ea8ca3`  
		Last Modified: Thu, 13 Jun 2024 11:34:21 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:108531394cf948c1778717791f9c464dc975ce04449963e5b4107c9e1a627c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4930065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbe3e8f42f7fb941b08b81a32bf0076e5a2358ef8fa45a545edfe47ec1c50180`

```dockerfile
```

-	Layers:
	-	`sha256:4cbfb1d9a3a15333c6de643f86c5f74adc07742b4167dab72885c53428c4f403`  
		Last Modified: Thu, 13 Jun 2024 11:34:21 GMT  
		Size: 4.9 MB (4915589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da074b648789c61b10d6b271fee09dba3deb79d412fe12deaf224b64c4a82f4`  
		Last Modified: Thu, 13 Jun 2024 11:34:21 GMT  
		Size: 14.5 KB (14476 bytes)  
		MIME: application/vnd.in-toto+json
