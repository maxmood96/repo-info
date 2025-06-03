## `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye`

```console
$ docker pull clojure@sha256:eabc509b9e9fc9f98d742e93f54f14acfee9580959631320671b4d07e0158b98
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:047a35e31f7dae1c2665cf932b1c4ac072c2734d3994673f66d0c32b8a6f1df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.8 MB (267785461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed08438cf73f6a3395e2219185f5ac004b78a370dbbf7567a296bd855db03888`
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
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2759b25f962276d5c941b87b4ee426d90184a15cd81228f42b8bb9c9495106e7`  
		Last Modified: Tue, 03 Jun 2025 13:50:12 GMT  
		Size: 144.6 MB (144634987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626e72aa06a109bcc367194575012dc027e4460baf958380960b523da0dc5a81`  
		Last Modified: Tue, 03 Jun 2025 13:50:05 GMT  
		Size: 69.4 MB (69399238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783ba34127d6d681835f335a93902a3488cac3acceb92b1c9753711eee009612`  
		Last Modified: Tue, 03 Jun 2025 13:49:55 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24d847bdc7aef64af08b426edca36df78a651fcf820c9fbaff6e98ac2c68bdd`  
		Last Modified: Tue, 03 Jun 2025 13:49:54 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3f094321a53ee76b180dac5acab00adbfc28180212de3be175b02dcd3d2689ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7272007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:761d9cc46b9d149cedc99a649527d4658487b483afa8aa685a91f5fba23b0d67`

```dockerfile
```

-	Layers:
	-	`sha256:d1bd1bec0a7684a5e90187545a76a7c3080750850390dec8f350d77fdbb09ae7`  
		Last Modified: Tue, 03 Jun 2025 05:16:27 GMT  
		Size: 7.3 MB (7256186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cc8f453255303ee0d787c5889d188fa9ef200a7a8d0a040bf462747c8633ae2`  
		Last Modified: Tue, 03 Jun 2025 05:16:27 GMT  
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
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f69f15673c2868db452eef23c09dcd3198ab0c842b3a65c6bd1d584a45318ad`  
		Last Modified: Thu, 22 May 2025 08:21:42 GMT  
		Size: 143.5 MB (143512648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
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
