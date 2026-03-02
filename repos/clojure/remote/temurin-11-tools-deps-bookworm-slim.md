## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:2024fce53ef6e37a6bafcdd3d2560c932fe248e17add2d359a32911bffd4b7c2
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
$ docker pull clojure@sha256:cc7f2d55417646c3bceac1b9f9abe004e6e96e43d8b0f15c299cb71e88aeec0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243734677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c708ee8aaaf39948962ec8e6657394360217341420700029db50162c6f06d43b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:45:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:45:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:45:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:45:51 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:45:51 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:46:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:46:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:46:06 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f805692c5b8f411ef73a5208896aed0a0d850db67bfe1a2d4cc119e3b9779b`  
		Last Modified: Mon, 02 Mar 2026 19:46:27 GMT  
		Size: 145.8 MB (145806756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19573c7ef4a04229aa88e717e1c6c6f9e9e9ce8fdaaa718b97bf955356ed853a`  
		Last Modified: Mon, 02 Mar 2026 19:46:26 GMT  
		Size: 69.7 MB (69690997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a31ff12a038018467634a951104ae4c696806ec3657c40fa83fef91f07af893`  
		Last Modified: Mon, 02 Mar 2026 19:46:23 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:67b9fbf4b6b5817a1beaa6c65f971a40478b188bca7c683785fe2d29bf11da04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5150575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1763f18b443f58275bfe494bdea40a8d5e7f2090e40ec74aa61603c6aaa339c2`

```dockerfile
```

-	Layers:
	-	`sha256:c851b8b2556163afcb8031185e9a1965ce8c40d87d567f01900b9a3724c09245`  
		Last Modified: Mon, 02 Mar 2026 19:46:23 GMT  
		Size: 5.1 MB (5136308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5603326843e437b625a3f5f418a213432a079e01a5026907f49e423222befcf`  
		Last Modified: Mon, 02 Mar 2026 19:46:23 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b1c6c6614701f36c3d54cf0ce8c903f40459b05ee454aa43ca555c93d90163b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240306364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31ce2bf45c5b4ea6350ca270f896aaa17f5ef6a2d5c3a41231466cb5ea868c3`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:45:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:45:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:45:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:45:50 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:45:50 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:46:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:46:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:46:05 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a343e7bed0edcf87da926c62e1728b1259e64bb05835df3cca1101cf9c831131`  
		Last Modified: Mon, 02 Mar 2026 19:46:27 GMT  
		Size: 142.5 MB (142501424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f50327fddf17fb552b798fae6e777f9e577c5975fe7ef80aa6f2cb68e0d23819`  
		Last Modified: Mon, 02 Mar 2026 19:46:27 GMT  
		Size: 69.7 MB (69688214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fb2f2aa4e69423542fee5f26d7b82c38fc2901c44cdb80fa2a9c4e30f6587f`  
		Last Modified: Mon, 02 Mar 2026 19:46:23 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2d8f02593bbb9860af29ab3a9dc64a9b5f63cb07c312faa2168c727d1aba0119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5157072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71bc6d450a9bbcfd301700ddd63ecc2764cdbbc3f1f92a9d3c09fdd80ec981de`

```dockerfile
```

-	Layers:
	-	`sha256:ecc130b616d5b6df672be9c5deba11df4b6ba5ac4395aa0c1b0b0f0619c296d0`  
		Last Modified: Mon, 02 Mar 2026 19:46:24 GMT  
		Size: 5.1 MB (5142687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2869808c56c389ea9b5faaa36a0e64cb79d8459cd767c633cf234d1cf756e2f6`  
		Last Modified: Mon, 02 Mar 2026 19:46:23 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:0271faf02f232cddacc0a2572fa3d048cfab02151af096b58e485823ee46b44c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240604532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1de11592d513246f17c8a061fdc1e0819d12f602390f326004516f4e24658318`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:51:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:51:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:51:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:51:13 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:51:13 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:51:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:51:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:51:56 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3def25e912c223ee8b3899e5ca048b2439f856f438ac690293817fbc0291fb36`  
		Last Modified: Tue, 24 Feb 2026 18:41:49 GMT  
		Size: 32.1 MB (32078334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1984d538ea5cf48291117340057bf192ca3108c6453696e981e6fa056f2db1d4`  
		Last Modified: Mon, 02 Mar 2026 19:52:32 GMT  
		Size: 133.0 MB (132997797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e143f44cb0425dd08e41c145e67c56ed4a125171b37f38455b4b59c72abb2044`  
		Last Modified: Mon, 02 Mar 2026 19:52:31 GMT  
		Size: 75.5 MB (75527753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef938a67f1f9b7543ed29770b9a33ea992bca1048282d1da8be7d763a78dfa2`  
		Last Modified: Mon, 02 Mar 2026 19:52:27 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:acb346dcd19c858b00a19655b92177a009a956f3bba81d9d02a466d95ea9f555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5155166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d725fd014a39b4ae4ba6d8928d1ed58d6a6ea5fc9876fad29e273fee6806f90a`

```dockerfile
```

-	Layers:
	-	`sha256:13e610a7268f22d1830680808778c2a29ab3d6d4fafc2f7480327d568a9d73a2`  
		Last Modified: Mon, 02 Mar 2026 19:52:27 GMT  
		Size: 5.1 MB (5140851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31015c96938e56390d8d98c685a382b5489434df082137a549f9bd8a5ce4f996`  
		Last Modified: Mon, 02 Mar 2026 19:52:27 GMT  
		Size: 14.3 KB (14315 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:ca2b4ac116d9c043345e8994d609ffd408cbcfc8577cab325c911a98f1888bf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.0 MB (221958009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15b8d85eab1c169616d92b26eb0f9eec85ddbe8c83f27a4729d43395fe7b3577`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:43:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:43:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:43:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:43:48 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:43:49 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:44:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:44:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:44:09 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4516a3d64dedb36867dfd0370b4c147205b1f54d4118dd32addfede7f46972`  
		Last Modified: Mon, 02 Mar 2026 19:44:38 GMT  
		Size: 126.6 MB (126561998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690d7404f15dadb4f1ebd760935d805c3dd8b090892fa3dee861ba768481a34d`  
		Last Modified: Mon, 02 Mar 2026 19:44:37 GMT  
		Size: 68.5 MB (68503842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d282421892380ef4c500ab0cb2f452a4c180bcd2cd1ae00955ce5b66ec33ba4`  
		Last Modified: Mon, 02 Mar 2026 19:44:35 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b4afd437044066a35fe235ebc31ec5dac33b3eba29aa1f21a8eb6d5ccf2049b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5141900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b30ede20a4945802153158695660937ca812853610832a266a7f72a19a532a`

```dockerfile
```

-	Layers:
	-	`sha256:ebcbed8c9b0049ae0d4e063f61aeacd17a2252776838ac3efbc43ddd361606bc`  
		Last Modified: Mon, 02 Mar 2026 19:44:35 GMT  
		Size: 5.1 MB (5127633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d7bc027a94ab5eecf044851bb52c97cb3f82cac5307f21257be960940ce9034`  
		Last Modified: Mon, 02 Mar 2026 19:44:35 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json
