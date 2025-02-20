## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:8e1602d0facab4a33ea1df5481211087abd26ce774b6b164488c2ff13aec1693
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:e81dac75e50def9649ae567f3361493246733622ff6238453b660510138e5c93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.0 MB (274041705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8410baf04768cc1e62cc181eea17393f71105fd73c1389305636636f7acaaf8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 04:24:49 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6048acceeec9fedb5760971f10a8ca2c7cafd6901dbf35ab4138e7e1837722`  
		Last Modified: Thu, 20 Feb 2025 06:41:29 GMT  
		Size: 144.6 MB (144566550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421392bfa028ff4dbe4ada55b8efaf596ce648d04386312322847c402b0f2894`  
		Last Modified: Thu, 20 Feb 2025 02:31:49 GMT  
		Size: 81.0 MB (80994428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24e1d80c78bb567c321bfc2100339244b74f39067a65fe31b0a090e2e491989`  
		Last Modified: Thu, 20 Feb 2025 02:31:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657b52111f1cc6370af99126698cdec8640e1dfdc2a0bfb708485d0f7694dc24`  
		Last Modified: Thu, 20 Feb 2025 02:31:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7625280064ce1f218948c9e26e4cf60e1c37e57dcee919ee02504716963079ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7186899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:634ff253f176892bca8d6de1690fc5a7dfc02f01cd8294fd12e091497d4a8e88`

```dockerfile
```

-	Layers:
	-	`sha256:e113d0b51980dbd68524ae59b815bcec23c839a6aafb21d30d2f2c6e002c44a3`  
		Last Modified: Thu, 20 Feb 2025 04:35:36 GMT  
		Size: 7.2 MB (7171078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5e17b98a98bbb2b658ccc265f36659c09d1b415ce61bff5120bd60062e0f7ea`  
		Last Modified: Thu, 20 Feb 2025 04:35:37 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dc0aaf02b51bad0426fdb3cb48a0096db130bee8e23cc4dda2492094df7ecd95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272606586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9d7da7210581fd0a1b440603c6a9e7b77851a5dbc99d34caf9464c8655031a1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 04:37:12 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece757aa0497472085ecc56d9989c1c60e5e6753869c29bf01bb2400f7d2e1ba`  
		Last Modified: Fri, 07 Feb 2025 08:24:45 GMT  
		Size: 143.5 MB (143454729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad32cece22e6a1d58a283361b902e540de86d3ca6eab8287c8afea8f21f05cef`  
		Last Modified: Thu, 20 Feb 2025 03:51:44 GMT  
		Size: 80.8 MB (80844263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740566a2c093bcc89a81483ee8defe18f88a06981901d5e6aecef8e071119fc1`  
		Last Modified: Thu, 20 Feb 2025 03:51:37 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a55b19fb68963cc370df6c30ae66d99825d7771f02f81c4078b9e4792d44363`  
		Last Modified: Thu, 20 Feb 2025 03:51:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5705b7ed44bf9eb291c6fb3d1e758b2df3010df817bf35c5981590c127db6c8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7192780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f2a26855ab4d5bbd11a7969ef63d1e0506a2702c11c0504e5bb960666b04c3`

```dockerfile
```

-	Layers:
	-	`sha256:54e0679c41228882c7b52fcb7b29185f244a8b5fe6080a5b5faeef733aef5f82`  
		Last Modified: Thu, 20 Feb 2025 04:35:40 GMT  
		Size: 7.2 MB (7176841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33e77f44ec568990c4a1d96e51462e08d333ff31a84138939ab3336fe1fd9d87`  
		Last Modified: Thu, 20 Feb 2025 04:35:40 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
