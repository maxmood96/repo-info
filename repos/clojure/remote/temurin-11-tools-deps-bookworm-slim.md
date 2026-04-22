## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:636dc4668b818cb17f23eeb90f69875362ee423f1dad858160bbeabd1d08c88c
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

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c122acac24f847440d6eeef353b25e209e644c6d2a1c61c95c08d0ce1f5a75a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243743014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09060b9ec7ac9cbb24886911287b5316739cfdbdd4f86ec9a5cebd26880e4a29`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:17:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:17:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:17:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:17:25 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:17:25 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:17:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:17:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:17:39 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faec9f813f339a346fcb31b3b5f549e7ea7c1c0561b8cdad51ec55da2336e72c`  
		Last Modified: Wed, 22 Apr 2026 02:18:02 GMT  
		Size: 145.8 MB (145806833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee04f888966319818431621f6ec478653e7ec31e3e49993cdd11e121597fad8e`  
		Last Modified: Wed, 22 Apr 2026 02:18:00 GMT  
		Size: 69.7 MB (69699284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44b92179227e472ed0c20f64bf6a226734ed0518bfb70dd934b67a0aad7a50b`  
		Last Modified: Wed, 22 Apr 2026 02:17:57 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7ccdaa169d2ed159353990a0cf59e3459ef7ae37e4722c31ac5e9ea98d94d844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5150575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a04948ae70aaf067171a2fadb34abf88fe94018a99fcb06fdf7e4fe6830a6c7`

```dockerfile
```

-	Layers:
	-	`sha256:9b68cf17193946ce2f97d6d9bf96962d3d971dfc89a74ae05b485d67f2d57be9`  
		Last Modified: Wed, 22 Apr 2026 02:17:57 GMT  
		Size: 5.1 MB (5136308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b144c83f7ea756d87344caa2a07792a9945d963396a5f82b4e03392e81d76a12`  
		Last Modified: Wed, 22 Apr 2026 02:17:57 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; arm64 variant v8

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

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; ppc64le

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

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:802a8ac9d142e039f64120181b19d076e69a132156c9f51043e75c4aa4ab88aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.0 MB (221967418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fed57a37b5ec8dcbf3dd4cc3323d2d8c93532047801262c7a86d89d2eebb03e1`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 03:58:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 03:58:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 03:58:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 03:58:25 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 03:58:25 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 03:59:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 03:59:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 03:59:38 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8e0b2edc82a3ba082e9f30dfa4358139881cfd62d2d6d055012699a091c83c`  
		Last Modified: Wed, 22 Apr 2026 03:59:03 GMT  
		Size: 126.6 MB (126562180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:162085e80c55a61d6f199c47fb4aee22a896013ad324eb6bc0fb66c0986b2ace`  
		Last Modified: Wed, 22 Apr 2026 04:00:02 GMT  
		Size: 68.5 MB (68513031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5119c507d7142fff323bdfc0fefe4b1138d709ce6d159f0fd47c650edca715c1`  
		Last Modified: Wed, 22 Apr 2026 04:00:00 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a7a4b2bd3bfc21ed30382a596f236fd3bf3b9924d523cf8b23da51abfb3ad690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5141898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:283e506b17d43c15bf4c05026222b60c727384ca1537c3707f60101bd91e68f9`

```dockerfile
```

-	Layers:
	-	`sha256:3630e7c3eae94d0bf00b562be7487522894887ff0c8dc5a9e118e4c84096f4d1`  
		Last Modified: Wed, 22 Apr 2026 04:00:01 GMT  
		Size: 5.1 MB (5127633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87c40a09032009cff59f4472b597b06f90d159da9c41988e329b386e2aac05b8`  
		Last Modified: Wed, 22 Apr 2026 04:00:00 GMT  
		Size: 14.3 KB (14265 bytes)  
		MIME: application/vnd.in-toto+json
