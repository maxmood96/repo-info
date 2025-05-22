## `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye`

```console
$ docker pull clojure@sha256:b7f22b15ef39445624cd7e68079d566b389ec2b7a94e7b571f31b887193e3ac3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:26210a6fa0adeaa93a4985f3b9c0ac6461a78d5dbe38d0dd8dc37e6fd0f9c925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.8 MB (267785147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49faffcb7d1892e633aac8f6916e59e8afec900af7426effb2d1294cf7c0bc29`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a90d692b2ea3be47c643ab64b8218fe1c7d551e158a1e76fd0e12f75c3fb20`  
		Last Modified: Wed, 21 May 2025 23:33:07 GMT  
		Size: 144.6 MB (144634958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87e4d5bf6ffc651321c491792a616229f99f2d1260289cf71781cfb65ea2e3d`  
		Last Modified: Wed, 21 May 2025 23:33:07 GMT  
		Size: 69.4 MB (69398953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70662e698d2575ab14b49f70b3e7845ec37ec32de11b5978deb0a6c27b1f0cff`  
		Last Modified: Wed, 21 May 2025 23:33:06 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea80929a053bf830bb7204833d1235931628a6b89f4b202235a2bd6e0e9b1c1`  
		Last Modified: Wed, 21 May 2025 23:33:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e3e172fb01fe779fc707138ffa23ebf3fb97a5f96f0bb781fb2fed4dd7e07d18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7270411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2647ea2f2ef45b951400757ed29e691890574b7941c02e773b20fb83383ba8a4`

```dockerfile
```

-	Layers:
	-	`sha256:7a3434d6368e16b51b6a824af21b5771a783b5fa3901a2cdb96ab06c86600a16`  
		Last Modified: Wed, 21 May 2025 23:33:06 GMT  
		Size: 7.3 MB (7254590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db0e6ffaa105e4556115c8b6b35801fda46d6b84c2504b33f6b841f9f98b0bed`  
		Last Modified: Wed, 21 May 2025 23:33:06 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:abe8a0ca49e8f811d964305c50ab319cb0ccbb27c481cd8b924e8089a5f4dd6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.3 MB (265292104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f5be5b511816aad742bab194e4f7b330863de1db2fd3826990b32217d021511`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Wed, 21 May 2025 22:28:12 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f69f15673c2868db452eef23c09dcd3198ab0c842b3a65c6bd1d584a45318ad`  
		Last Modified: Thu, 22 May 2025 08:21:42 GMT  
		Size: 143.5 MB (143512648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89272afd836c52a71858edf619981e57ee8463deafb472da29d085f507fc23c5`  
		Last Modified: Thu, 22 May 2025 08:26:29 GMT  
		Size: 69.5 MB (69530659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6656394013333b597e6fe20442d500515358974b1af10473e588f43fe122ad3a`  
		Last Modified: Thu, 22 May 2025 08:26:27 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237550cb1a3574dd4cda44e4eb85bd1c90113762d619fe42220073d9c27045ea`  
		Last Modified: Thu, 22 May 2025 08:26:27 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1b1715207a0e353630457016ba51e8be111628ecaa0f1ed04b89f3255b5a5a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7275627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a2aa66045fab38d265289fe5eb7e82179dd20fd444ffcfb986bfc6004de9fd3`

```dockerfile
```

-	Layers:
	-	`sha256:eb16ae685fbb09c3b9d082c67d9f2d35ae37521da385883fdcbc15899cdc88ac`  
		Last Modified: Thu, 22 May 2025 08:26:27 GMT  
		Size: 7.3 MB (7259689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:041786aff723df558f420224616a9edf61003073bcb5d93f01cf204199d0e994`  
		Last Modified: Thu, 22 May 2025 08:26:27 GMT  
		Size: 15.9 KB (15938 bytes)  
		MIME: application/vnd.in-toto+json
