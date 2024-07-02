## `clojure:temurin-11-bookworm-slim`

```console
$ docker pull clojure@sha256:46e0f0f93e505ff1720fec190642ca19cbcba379cfde254a0b8e6468e1e19624
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:90b6ca97f76e3d9c298df21badc7a2f348fccb4065fd2afdce0f1c97d75ba754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243698523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956d6f1a3ca689fa366c0d1f70b219d5f3af79b380df86f529922b5eb9da626b`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c381c94c802de9e548e21c3c211534a487651d51e482397a4ff9510b170699a`  
		Last Modified: Tue, 02 Jul 2024 03:02:55 GMT  
		Size: 145.5 MB (145505213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aafd160750c75bb866dab4888517b54c958ec04b43fc6dd0459af004e6ebc0c`  
		Last Modified: Tue, 02 Jul 2024 03:02:54 GMT  
		Size: 69.1 MB (69066387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea5f0e49549cfa075e6feae21376a099139e3e02495b5f7df4c09a3b38b255c`  
		Last Modified: Tue, 02 Jul 2024 03:02:53 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1ef2b2a0538b996a047c645ecc6a4696c630169225ba77dd311d242e59d012e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4718975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:770a30573552688db909ccf79a2536f8a3729ee4fce8b32490d9d097f8bd6891`

```dockerfile
```

-	Layers:
	-	`sha256:85b29a67dab5efb5a0e82e042c904bb88bfd6bbf3e8c9581411fce58b38758b6`  
		Last Modified: Tue, 02 Jul 2024 03:02:53 GMT  
		Size: 4.7 MB (4705039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d323e65dc43e72cbf44d8fd2821d626f6e4fa31c51c76f2a1143879b8b9fbd2`  
		Last Modified: Tue, 02 Jul 2024 03:02:53 GMT  
		Size: 13.9 KB (13936 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c30c8414fefa0751e0a444aa43d3ab940e2149e5625ab18f6574890bdcb0f36b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.1 MB (240105078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a088543a51dc4705c05ad1c802d9909aa24ae065e4c21ba71092edf342816ec1`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
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
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4da0edc1758d81eb3c66f753c37cc4200c2b16f103c1e9223f076a2621e0a63`  
		Last Modified: Thu, 13 Jun 2024 11:29:10 GMT  
		Size: 142.3 MB (142304075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8a264ca04c6dd046d06b0468b02d90bfbc10c47af61da5a378aa60ef237916`  
		Last Modified: Thu, 13 Jun 2024 11:32:53 GMT  
		Size: 68.6 MB (68620690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01308a837d82f12997fc79287c914d39f7b8181c97d5f41d05e8c7e0e99ad53`  
		Last Modified: Thu, 13 Jun 2024 11:32:51 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d1cdac2f022b184d0b9f64bd25f0168cf93bd9c0df0c4bfb13d3905a9120842b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4725801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47157c037faaf44feb59db3993ee8505b405b985c6f2e15e2b9274b91832acb3`

```dockerfile
```

-	Layers:
	-	`sha256:36a5f2ab57c52abf66f8c062265edb693c021a52fe623128ef0d0987f73bff3a`  
		Last Modified: Thu, 13 Jun 2024 11:32:51 GMT  
		Size: 4.7 MB (4711323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1d03b8ca34c297afc7e0ea4093e5d146cd1b2a04d14135bffcc82b961156cdf`  
		Last Modified: Thu, 13 Jun 2024 11:32:51 GMT  
		Size: 14.5 KB (14478 bytes)  
		MIME: application/vnd.in-toto+json
