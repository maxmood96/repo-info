## `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm-slim`

```console
$ docker pull clojure@sha256:2892a25380624c1a56711225e4e8797c39a22d949e3ad019b29e0b87c84e9ebc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7b169ec90babbe1e85b404a3eb441d1dd2298f7fc017d79ff82f6c2b863f9aa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152639855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fcadd5fb39779bff4f270dbdbd4ccc0f52ad2a397aa533a40bc059cd35e8dee`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:53:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:53:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:53:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:53:43 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:53:43 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:53:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:53:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:53:58 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b83644c3a315653dc4599f38f7fb025f404364a5c6c9634e3355dc600f27b0`  
		Last Modified: Tue, 04 Nov 2025 00:54:36 GMT  
		Size: 54.7 MB (54731291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f29bb31c54361e23982b667444e8461c032cdda201eaf09a71af403a528bb55`  
		Last Modified: Tue, 04 Nov 2025 00:54:38 GMT  
		Size: 69.7 MB (69679355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdf01fdad54f054d4ed7c074f6029aa150e41482582ff80610dbbdfa2ce17df`  
		Last Modified: Tue, 04 Nov 2025 00:54:28 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0d8994e745173d1559e91e595ede8cc49f8549a5ec2d9d063398464a4005a495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5960fd93fe8ca95182ba3e5157933b3781ecd3e06f521118c4e03b0195b95e87`

```dockerfile
```

-	Layers:
	-	`sha256:185900f2bb7d1921aed787a936e400094eb7af016c048d60902d0570470d979e`  
		Last Modified: Tue, 04 Nov 2025 10:47:42 GMT  
		Size: 5.2 MB (5234998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f2570a84c1d9819dde3ce5531861bee58ed456d65d6965de377ddf746db9a39`  
		Last Modified: Tue, 04 Nov 2025 10:47:43 GMT  
		Size: 14.2 KB (14248 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c24757afd157b370bffe6dd10ec6a087993b18a10e8eea43822cfeacbc30eee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151498902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92593b382ef88203630f8023bc7bf68f719c6c25f432d7bdc0923efd63373f30`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:54:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:54:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:54:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:54:03 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:54:04 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:54:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:54:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:54:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8305024387475e0a878f887025d6d7dde5cf07862bade7b138366af80f0d6c41`  
		Last Modified: Tue, 04 Nov 2025 00:54:45 GMT  
		Size: 53.8 MB (53835605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa04c6b2bf0c0594296107b359009868131fcaac5f4300095b0ac17aff172160`  
		Last Modified: Tue, 04 Nov 2025 00:54:48 GMT  
		Size: 69.6 MB (69560277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5be7035f8a58cebde07c9ed6c49ba534ed016495fcad46054341f9a71bfd25`  
		Last Modified: Tue, 04 Nov 2025 00:54:40 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dc00c7e766cce2dff8e1be1afe384c072ff1d2e5a71661bb724666400d27431a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b148f86a1a8ed0a5683b5cb63491410c7a11622c20d88713d01b9bee63e65a42`

```dockerfile
```

-	Layers:
	-	`sha256:34bff5743006c2fbd3112016bb81480dcf266573b368a9eb9f2298170d5e77c6`  
		Last Modified: Tue, 04 Nov 2025 10:47:49 GMT  
		Size: 5.2 MB (5241457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d108acd415551bb961ea7aea1ba228c722028f9392aa4e624a54334010321a75`  
		Last Modified: Tue, 04 Nov 2025 10:47:50 GMT  
		Size: 14.4 KB (14365 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:be6a186f90e8c2f4cf1fe649edcfd7ecf94ecfa27e64b2fb06858486d4b0946b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159748032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d9167f04d7944cae1032106e7d23b9bf2434cd6780569368d67815f712707d4`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5a28d569c39dc949a4743122d7b5ec2d2e0664f1276c801bf984a711d80f2a1d`  
		Last Modified: Tue, 21 Oct 2025 03:26:43 GMT  
		Size: 32.1 MB (32068780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d89a65814f3736d04ea661a93b7918d79980e381d31c840dc077f702333e34b`  
		Last Modified: Tue, 21 Oct 2025 15:21:39 GMT  
		Size: 52.2 MB (52165368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc093f31c1d891fdc459775eb11ed81839aaae71e5958aa676942f1b6aec109`  
		Last Modified: Tue, 21 Oct 2025 15:28:01 GMT  
		Size: 75.5 MB (75513240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb30cefb078c1e1f5a6748bf92b3c804e6c9ecec37826354b3c9779450c448a`  
		Last Modified: Tue, 21 Oct 2025 15:27:57 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4dc51c19ae0eb5e32a1b74aa9232046e4f28f69184ee4ade15340bc75cabc8e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b537645648ae6f8997aca69f559f7ed25f4ba2b82e103a9399027a050d4dc2c8`

```dockerfile
```

-	Layers:
	-	`sha256:b46f4c503d1e2f05708fc02d2c756adc5980f6322938f2cd6f96937aa2ee1ef1`  
		Last Modified: Tue, 21 Oct 2025 18:42:07 GMT  
		Size: 5.2 MB (5240749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:794f81c757153508a5bd618fee9e691a0abcdcb32d1f0898cd93d3b94f9e2a0b`  
		Last Modified: Tue, 21 Oct 2025 18:42:08 GMT  
		Size: 14.3 KB (14339 bytes)  
		MIME: application/vnd.in-toto+json
