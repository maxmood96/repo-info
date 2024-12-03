## `clojure:temurin-21-bullseye`

```console
$ docker pull clojure@sha256:f6178bf60425442c756122fc5e189a02f840a7d6a25c8325a1327823d80e3d17
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e6d81a5c92d96f2fdfda666323df58124d5f7960e531382fe0ad543ef4b39e04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280468467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe1f1913a22228a05ecb7d9342ae6b5bd6abdd43db49867bcbbdb16963f8e95`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cd606f6f489eb66f1307280aec321b3af3aa998dca447ae1cc91c6b884240064`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 53.7 MB (53739147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e90cf8378535604d9938b186be006972adeec072abf069c1ea8f34b1cc3bee`  
		Last Modified: Tue, 03 Dec 2024 03:25:56 GMT  
		Size: 157.6 MB (157568687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5442ef7ed80dbc8dc6b7e7ca74395aef040fe0b0902c55f07edec1a3835572`  
		Last Modified: Tue, 03 Dec 2024 03:25:53 GMT  
		Size: 69.2 MB (69159595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f910aa5e37e8276cf05c596787837807e448dcab69c81ac6c51d23aa6191e1`  
		Last Modified: Tue, 03 Dec 2024 03:25:52 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206e3223f9ff779b96fbaaf2172b6353884a812ef636a8452c9421cc18df3875`  
		Last Modified: Tue, 03 Dec 2024 03:25:53 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:cb5e7fdf6056e487123c84b6af91c9f73dbc79abc01f7ca2f99424f70d8fa926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7234347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6aa3c4aae2a84122daedc4c81ecaecf824ce82dd3f80692ebd713a365ccb70f`

```dockerfile
```

-	Layers:
	-	`sha256:a23d4bf300fecdf912ea66f34c747a1e9b7722e47ca06405d68de32bfc1e6d4b`  
		Last Modified: Tue, 03 Dec 2024 03:25:53 GMT  
		Size: 7.2 MB (7217850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:def7ed0d654e8650af7b3a31b54185e19d257074bd93d4cdae48048cfa43f96a`  
		Last Modified: Tue, 03 Dec 2024 03:25:53 GMT  
		Size: 16.5 KB (16497 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:61b1ca0aa5c8c6b9dc9af52b65576e51b1a860986e7d3d5edd26bee14a671e9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277325921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5eaabcfd73e72c36f2b43b3fcbfd731323f4b70a92e26da75043400dcc114d8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e357e1f94476a03fde298261e8c007d487d3cfade45a9eef064eba724a5c5e2e`  
		Last Modified: Tue, 03 Dec 2024 01:30:26 GMT  
		Size: 52.2 MB (52245994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1241a00b2c08e47f7320bdf5abd5eb13c51b426197535af726d7c54e86c5acd`  
		Last Modified: Tue, 03 Dec 2024 15:26:01 GMT  
		Size: 155.8 MB (155793113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e45d69aabe334befe2186e0e4ed233b72904e6a1c925cf8e0f20a8696afe52f`  
		Last Modified: Tue, 03 Dec 2024 15:29:50 GMT  
		Size: 69.3 MB (69285775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7cbbf8a05679b7d49e23426757bb567c694f5f86bc409fee2a376f6dc6e05a`  
		Last Modified: Tue, 03 Dec 2024 15:29:48 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd142aee7d5d5de73e96e0bbc3c06f52f4eef167840d78c1400b89e7a933e8a`  
		Last Modified: Tue, 03 Dec 2024 15:29:48 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:fe7a02f2ba1b1079d21bd0a9cafe487eaf3ad0ce5e446aa5948f94c6bfc77bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7239616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:390d4069e5e19279cc525859dfaf45eae97f0148465cef118f061ca30cd515f7`

```dockerfile
```

-	Layers:
	-	`sha256:e75a5c7467b52c10b5060609d6aa17436ababcc4a7fcd7f815f53c3be84892f1`  
		Last Modified: Tue, 03 Dec 2024 15:29:48 GMT  
		Size: 7.2 MB (7222977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55638b02da19285f7ccd4655d9442afb357851b3ea36975db6aaf14bcfe93c93`  
		Last Modified: Tue, 03 Dec 2024 15:29:48 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json
