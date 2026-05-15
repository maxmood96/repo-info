## `clojure:temurin-17-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:da70f8b3a97431b76c527aae334e86f8ffe314a34946a0fa8da2cec53cdbc6ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:81320df420576f32a70f90afbb551620059b1387b6a78745e44bef38f4bb44ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235379438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15b3a5b099a66ec5195304d761f3dea8eea12bc234573c35a70ca340686add19`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Thu, 14 May 2026 23:35:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:35:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:35:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:35:08 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:35:08 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:35:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:35:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:35:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:35:20 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:35:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:77e30ef52aeb52d8466baf0f50b54ed2fc0b421f44c49e5bf93682b27110f4d3`  
		Last Modified: Fri, 08 May 2026 18:22:59 GMT  
		Size: 30.3 MB (30257958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfffd1a06858ac8a8829ad49684a2a2927a1bb7bb57240302dc03f43a8b2446b`  
		Last Modified: Thu, 14 May 2026 23:35:43 GMT  
		Size: 145.9 MB (145905444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5c5fae34841dc9df52206f4b57fbcccdddb933622d20699bfde2ae4530bc3f`  
		Last Modified: Thu, 14 May 2026 23:35:41 GMT  
		Size: 59.2 MB (59214993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c621ce10813c53acdf9fc6de75f0efbfa1fa921dabe5170516ef8b00513679a`  
		Last Modified: Thu, 14 May 2026 23:35:38 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54371cb0236d14cbdbb0af1d0ea909b5097407d04390d2540129e95295c99f15`  
		Last Modified: Thu, 14 May 2026 23:35:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:56b5c7959c7de3c36737fef9e773983e1f784223fd22bc726f402a227cd06e2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5336668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d39c3e8dabe328b5d3a1193f26c71027ffd78a44186b5b426a1314ca88dd971`

```dockerfile
```

-	Layers:
	-	`sha256:a5cb0caa672446ac6a886ba62dc08ed1428fac8ad10900c21c3f8c3ef2f772e5`  
		Last Modified: Thu, 14 May 2026 23:35:38 GMT  
		Size: 5.3 MB (5320678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99d573b84c1ff24893d98175a910a5ad6eae008b0be54d8806f371d863347455`  
		Last Modified: Thu, 14 May 2026 23:35:37 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:af4e58ad5c4f72775388654c19b8598b101eb007ed11be92acb501910272e9ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232826083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33717dc2cc3fc704631eb468523ae9c08515884524eda4c019e4884f8a9f3b70`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Thu, 14 May 2026 23:35:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:35:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:35:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:35:08 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:35:09 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:35:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:35:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:35:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:35:22 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:35:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ab0f13d792ff9100407906fb422a0b62a8b437abde4c245e03f0366814be9aae`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 28.7 MB (28742591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7094a2ba9ca54b337112cffd915d8da2236ff8219ae5e8905809b4e2793c61f`  
		Last Modified: Thu, 14 May 2026 23:35:48 GMT  
		Size: 144.7 MB (144724357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0ecb43bfa4023678f8a3998106e7ffe7ec9828e724d32e9bb5ca6b3bba3f6e`  
		Last Modified: Thu, 14 May 2026 23:35:42 GMT  
		Size: 59.4 MB (59358091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5669fa1a28d64426ac0cb8859095d5a70bbc3a5ff1e3e8c2dd94cfb7d5265c67`  
		Last Modified: Thu, 14 May 2026 23:35:39 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e58ff65ea48b1fa5fb9dabc4a45c2af71e20e503af59c63ac535924231f9ced`  
		Last Modified: Thu, 14 May 2026 23:35:39 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3053d08c3e2e9a3a850fa1f257a670600902e06dae79dc0de97b5e71a093bba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5342518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb91ff08a3ddb5d8e920933825725d81cda21684be35fad6c7982c94e2768e6`

```dockerfile
```

-	Layers:
	-	`sha256:71c378ffdba307cb50b8fe0232571dd177208f69228123c8b227240b577bfb24`  
		Last Modified: Thu, 14 May 2026 23:35:40 GMT  
		Size: 5.3 MB (5326410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a183d3727ee9fd3a7bda8a9a6ead56653bfdc93d3b3e551ea4a03855535adb8e`  
		Last Modified: Thu, 14 May 2026 23:35:39 GMT  
		Size: 16.1 KB (16108 bytes)  
		MIME: application/vnd.in-toto+json
