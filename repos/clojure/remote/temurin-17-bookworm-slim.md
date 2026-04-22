## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:e87598eacad41cf8f7713ce6e5ae456270373dc9154e4737e3f9c59e519c0da7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:aac90455728acf79589a5fa45b86b0e022c58da5497f30daa71d87bb437911b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243564961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce09dbe1fba95ba0068719a7da7b2a0dc56e2ea35cf86b90479935edb661d86f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:18:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:18:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:18:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:18:46 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:18:46 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:19:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:19:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:19:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:19:00 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:19:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b075ce9bb31725cfb2cd20f09304d82511a855081803dd47c96c5cd2600ad7c3`  
		Last Modified: Wed, 22 Apr 2026 02:19:21 GMT  
		Size: 145.6 MB (145628762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6128cf7622f2eec9447dd3fc2fe3a3df5c9edea4cfdd4509748c73d663aa87`  
		Last Modified: Wed, 22 Apr 2026 02:19:19 GMT  
		Size: 69.7 MB (69698903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf110fea7878257dd21183667c82360a6360c9ba4cd3aad2c751e4cede89fd6f`  
		Last Modified: Wed, 22 Apr 2026 02:19:16 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4cccb4940190f1ea7b69683bc316f6d23d8053a1560db9b6daa3ac0f43a749`  
		Last Modified: Wed, 22 Apr 2026 02:19:17 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9f717bc18c1335f3c1b8bee4485074c4a7daac19b6b203d5d1be3e03e4875ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d8e81427be3159c99043dba5c170c511f6f9e68b0ae18798b60f74351154c4f`

```dockerfile
```

-	Layers:
	-	`sha256:fc686ac5988315060ed5fc1c444974103ec981e18582d0a98be908de135fdaac`  
		Last Modified: Wed, 22 Apr 2026 02:19:17 GMT  
		Size: 5.1 MB (5116167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:890147a574f303918181931328af7def5c9b66f1ca26f238d64c8f7acf316307`  
		Last Modified: Wed, 22 Apr 2026 02:19:17 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f0786a004779639ba347dd79e9ca2c9468c31dff05d7a4f0f44ccfeefb565a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.2 MB (242245987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8650afd5758323c19c252604341ebb1c890d87b6999430a625c563344c56b9e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:21:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:21:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:21:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:21:44 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:21:44 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:21:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:21:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:21:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:21:58 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:21:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4dd97e5c0cfee2605dd60f88cd61a824961aee85db94c068ae4ea42a74d737`  
		Last Modified: Wed, 22 Apr 2026 02:22:20 GMT  
		Size: 144.4 MB (144436188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889e182c742644c652ca2d31ba90393330f7e87e390fc36be1ef301650a1dcbb`  
		Last Modified: Wed, 22 Apr 2026 02:22:19 GMT  
		Size: 69.7 MB (69692644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b0209caf6967eec244cc49a1df8af551219113359244c5789fa87447de0e19`  
		Last Modified: Wed, 22 Apr 2026 02:22:16 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7eb401b1d4e61d15d702e7107361446bc8b3e5790d8d8f4f69554f72530f91b`  
		Last Modified: Wed, 22 Apr 2026 02:22:16 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a8a024be83bc543a1d28fc4590af950c17a1dac915fb083d94701273898bb899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348ee3203a7a7efdef779dfeef8c3f97183aabcc73442fade39307699aa0ebdc`

```dockerfile
```

-	Layers:
	-	`sha256:fa9c4ec51c901b82bf704b8437a7ab3365fe2b21016ee06e00609b19b8451069`  
		Last Modified: Wed, 22 Apr 2026 02:22:16 GMT  
		Size: 5.1 MB (5121928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67c8192a713d0d91b5c08138364d3cc457bf2b9dc09e434e07e36e4267c9f5d9`  
		Last Modified: Wed, 22 Apr 2026 02:22:16 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:127b00f44d4ca95894a6270dd12294176e849df470840527a7274100eb77f359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (253047297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf2a4af3db8d7a12afd1a679fcc8a2ed83f5b5fba948fa399f9f96cfe601e1fc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 02:49:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 02:49:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 02:49:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 02:49:09 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 02:49:09 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 02:54:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 02:54:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 02:54:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 02:54:25 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 02:54:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b1c56220ca211bc9d02f1ed5c589465809676b6ab2cef705f1e2fb8e9726de76`  
		Last Modified: Tue, 07 Apr 2026 00:09:42 GMT  
		Size: 32.1 MB (32078464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac07d766af011abbea5aa154cb16be5509f5ea8687e2050966b40181dcca495d`  
		Last Modified: Thu, 16 Apr 2026 02:50:31 GMT  
		Size: 145.4 MB (145438295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be861dbe36138889a98f1a69d8a1492c0ec1cdd48894d0f2a74d018b769865ae`  
		Last Modified: Thu, 16 Apr 2026 02:55:05 GMT  
		Size: 75.5 MB (75529493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4745bed3e6e3c11c73aafa9a6fc3620938cd2a60bd8c27a5beb2deb3863fb61`  
		Last Modified: Thu, 16 Apr 2026 02:55:02 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce9273f10bc056901c484965125ab10fd2a2db64ce330d93c2326343dc2e647`  
		Last Modified: Thu, 16 Apr 2026 02:55:02 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7634b146b0237e2032c1334ef8521eea240824fd2fd9b17ac65df9766e741233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:845664851705c6e7ae1d1a480b1da8a421d99f3438944b389a1df1914b898e52`

```dockerfile
```

-	Layers:
	-	`sha256:d3bbcc9b9f3882410814704ef3a8c561baf0cba6a24bccae0eb3613834077ed7`  
		Last Modified: Thu, 16 Apr 2026 02:55:03 GMT  
		Size: 5.1 MB (5121325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:077fde46c4e473e146c4130146dbb913dd04c3d0d3d38cd1c7cbd1c3063ebf14`  
		Last Modified: Thu, 16 Apr 2026 02:55:02 GMT  
		Size: 15.9 KB (15883 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:2515356c7ce53906fdbaa412d6fbf9583dc61c1b413c3950adfb5632f3cf54a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231032351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b41ce3b2c8ed8e8fa44e66e6a2b7e3f28847ecaa4d754fa612e3abcbf058def3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 04:02:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 04:02:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 04:02:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 04:02:01 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 04:02:01 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 04:02:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 04:02:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 04:02:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 04:02:15 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 04:02:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770c29abe6e48bb12a50bc724696449ab9dff23f79b8688dde7d5e64a7f8299d`  
		Last Modified: Wed, 22 Apr 2026 04:02:44 GMT  
		Size: 135.6 MB (135626975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b982a63674c52b9e96f2523d4c48094427bcd4392c458558b5d5821ffbd9d103`  
		Last Modified: Wed, 22 Apr 2026 04:02:43 GMT  
		Size: 68.5 MB (68512773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87dd16e2dc9291a5d8e9b1722f958fcf1609f1a4cf6900179d2b70cae7388bec`  
		Last Modified: Wed, 22 Apr 2026 04:02:41 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7efbf8dfe880d6d9f6d73dcdbcee336e81d813c4ce8edb52bc7e09f91d9124be`  
		Last Modified: Wed, 22 Apr 2026 04:02:41 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:931f538c765ac1ea183ce9ee5b5ee8dbceeed7530ba2a37e192f499c6ebc68f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5123324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab96491ddca4e3ef6498b8c4fd3672e8ff385a92705e304632f5041f8ad2fee3`

```dockerfile
```

-	Layers:
	-	`sha256:a510673d1ea5bbc7afe2ac33cfd802ac8d8f6eb04cc85530a7431bea9c0a8b6e`  
		Last Modified: Wed, 22 Apr 2026 04:02:41 GMT  
		Size: 5.1 MB (5107488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d099a95e62a7a893d9a5e96d1c07e13e6b97249277575bfdbdcc701496ee7060`  
		Last Modified: Wed, 22 Apr 2026 04:02:41 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json
