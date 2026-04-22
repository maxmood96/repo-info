## `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm-slim`

```console
$ docker pull clojure@sha256:aa5eac3672b5d3dbbddf2df0efdacf18f8a371c65d4b1360b8c9fc639f063996
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

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c8a9518ecdabfaeb941c0f6321420eadcf98f8adfc22098ed6d4153b37502ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243742851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0ca2bff7a5e606615cec864c9dc7a8c3bf009d88381fc4fd2740c47212f6118`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:02:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:02:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:02:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:02:42 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:02:42 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:02:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:02:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:02:56 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3cfa662fa234719df3f2565822c6792eb79a9321162173858b92399ee9e065`  
		Last Modified: Wed, 15 Apr 2026 22:03:18 GMT  
		Size: 145.8 MB (145806794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da6908f73afce1208af2e54ab620a342c24082369ef4d460c51e763fe9c01ca`  
		Last Modified: Wed, 15 Apr 2026 22:03:16 GMT  
		Size: 69.7 MB (69699080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c2370e5f410505c0909a4d71a6a0232944e33867625a3776878b1ec1dc0d49`  
		Last Modified: Wed, 15 Apr 2026 22:03:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2fffc19141c13cc625cda1b236faa299f596fbb933b2eec288814379dd62f358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5150575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957e33b193126128dc205948927008a74b657292a90236cb011a429d3259615b`

```dockerfile
```

-	Layers:
	-	`sha256:1ba370c1f4cef414e39a51da1008d0becc5ede014f8596ac589fe5a1caafb2ce`  
		Last Modified: Wed, 15 Apr 2026 22:03:13 GMT  
		Size: 5.1 MB (5136308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ee9fefff295157ffb0dd22729d97341d307c725a9015c5279dbf309f285d92f`  
		Last Modified: Wed, 15 Apr 2026 22:03:13 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a6e6d138ebdc51ab09e5dd039caaf76ad99396f0aef137c89255dc4676457816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240310183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e13252b095b22cd2fc7191b4eba173336ac87b36a502dd7ef1583d5f15b478`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:20:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:20:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:20:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:20:47 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:20:48 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:21:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:21:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:21:03 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209817363c82d50cf84693114194dcf44dc3c0b271a8b51001b2af0ef2ded7f4`  
		Last Modified: Wed, 22 Apr 2026 02:21:26 GMT  
		Size: 142.5 MB (142500803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c1a474635bee62349ada8a7558eb1996598ea047241c9b301b16a496018f07`  
		Last Modified: Wed, 22 Apr 2026 02:21:24 GMT  
		Size: 69.7 MB (69692622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e945de864aadd73334d3da5f83fbe4b5e23efefc10bb432be6b975f51b2e5126`  
		Last Modified: Wed, 22 Apr 2026 02:21:21 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:233c593960dd6bd33ea6bce82d15c288fa7ca9853a8eeec5f8c0406f9f953d7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5157072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54e5fc5dd35e103e063c128ec72049bbd0ca0b9555f643bb9f9201f853a81560`

```dockerfile
```

-	Layers:
	-	`sha256:412e04676c4f74c6af90a2e5aada6995e409a7fb63dd91aa7b113e4bcaa1550d`  
		Last Modified: Wed, 22 Apr 2026 02:21:22 GMT  
		Size: 5.1 MB (5142687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:364eb751736af75a9c769f9e5775b49153b48ada7c111989825382b6f2afe0d7`  
		Last Modified: Wed, 22 Apr 2026 02:21:21 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:aa640915843b1b5d9099a297a815312519911c44cdd456f97a8375451b20ab65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240606068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c64512702759f988f7e151f25887dba5ef4854ed19f07c631e7d504094e3d6e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 02:39:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 02:39:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 02:39:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 02:39:38 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 02:39:38 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 02:44:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 02:44:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 02:44:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b1c56220ca211bc9d02f1ed5c589465809676b6ab2cef705f1e2fb8e9726de76`  
		Last Modified: Tue, 07 Apr 2026 00:09:42 GMT  
		Size: 32.1 MB (32078464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c2b4249a5f9d02d5abe9b0b44777395a74fe0b79fd16dd95566bff1dc3ac16`  
		Last Modified: Thu, 16 Apr 2026 02:40:45 GMT  
		Size: 133.0 MB (132997415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43535613a306265f32441fcd7dd909349f6c2acb860304f238a32280ab2d708d`  
		Last Modified: Thu, 16 Apr 2026 02:45:32 GMT  
		Size: 75.5 MB (75529543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac7ffd4cc71e80ac60b7baf21bfe13d0f23ca06edd34e2a723e5f0d8f62177d`  
		Last Modified: Thu, 16 Apr 2026 02:45:30 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e32381d490ee28bbd667cfc3237c358718be5e330c63148b713304a25e552a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5155166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27d3aeb40619aa816c81ef400355b3918de0feccb607aaeda200f508458ef8f`

```dockerfile
```

-	Layers:
	-	`sha256:06cb04f68b456a1ddd763cb400b1c56fcbd7fb014a175182141ddd8cc1f40a04`  
		Last Modified: Thu, 16 Apr 2026 02:45:30 GMT  
		Size: 5.1 MB (5140851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc0d1e6e6a37494e4f50967176b322d48f88ca1840924096ebe6fcb92baf9cdd`  
		Last Modified: Thu, 16 Apr 2026 02:45:29 GMT  
		Size: 14.3 KB (14315 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:4c74f51a0b7c7db1d25b750b05271df9dc177c93fc0c5cc3bf5b2bfff3732f6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.0 MB (221967231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b09581f0c974887971fb271cdc98cd7205406c15edd908fb25a13fd68f6a32a4`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 00:34:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:34:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:34:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:34:59 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 00:34:59 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:36:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 00:36:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 00:36:49 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3136158d6d52c18c8b86a696a972abe97e7e16324bf358cbdcffb25ae4dfaea6`  
		Last Modified: Thu, 16 Apr 2026 00:35:35 GMT  
		Size: 126.6 MB (126562154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca416aac9e78d256c4fa0697201be3e3af0c053ba1f97435353796eb55f6001a`  
		Last Modified: Thu, 16 Apr 2026 00:37:11 GMT  
		Size: 68.5 MB (68512797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c65eb0ff1d5b0692fa326613d661305d5ca7be37a9f00628ae84fe1913ee287`  
		Last Modified: Thu, 16 Apr 2026 00:37:10 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f82980dc06e286ff647b7444392a6bd62e0313c5ff4de962b4427863bc0f8538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5141900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad00f4067ab0fa450c306756e9aa41b777780a49c01ed67b79ec86161d05967b`

```dockerfile
```

-	Layers:
	-	`sha256:6e7d6a046d78ae0289038c03b454a01f33930b4ec80b0e6076845f50e902836c`  
		Last Modified: Thu, 16 Apr 2026 00:37:10 GMT  
		Size: 5.1 MB (5127633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac4950ba56726f62eef358a5e5f37560b9ae3eb9984cfacaa54d63dd73fab1bc`  
		Last Modified: Thu, 16 Apr 2026 00:37:10 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json
