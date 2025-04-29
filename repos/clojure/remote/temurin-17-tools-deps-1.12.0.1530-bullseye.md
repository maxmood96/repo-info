## `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye`

```console
$ docker pull clojure@sha256:86986d10a3b095697ef13ef5990394a09250f1f0bf947c46a263dc0f8a91a291
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:57a9416d4f2c4b9d4960d0789e5c213e027296d1037cf5101ef4a150d4d1b8f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.8 MB (267779777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae7da724e61880504d7ec58d414c6ca19170499f3e2d827971fd216f3f39058e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fee42626672a0ece1bcd8b8519d6179812bbc02a79630da24ce67e5561c462`  
		Last Modified: Mon, 28 Apr 2025 22:07:30 GMT  
		Size: 144.6 MB (144634976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb914edb1b7561412cb1567a5cf908281ff0cee20956754b10ba810c627f966`  
		Last Modified: Mon, 28 Apr 2025 22:07:29 GMT  
		Size: 69.4 MB (69396020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bde7fdc1476ca77b3a62902885853d1346205d204fdaaadc0d0bf04b2ea80d7`  
		Last Modified: Mon, 28 Apr 2025 22:07:28 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635634270f2c827a23ab962f6f4dbae41c2acd233b464dd1e0463b639b4f8c66`  
		Last Modified: Mon, 28 Apr 2025 22:07:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:047559784b643f6aa1ab333c6812cd9815b8c974960cd2706658b783e0457c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7222376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a637825bdfd4bee25ae70736d04c8c0888e1caeaff94c4099630f65338728d5`

```dockerfile
```

-	Layers:
	-	`sha256:34d17786fb34058b437a7c8da2a1ef58864f4728a2198cf98bd1a53ebc8dc6b2`  
		Last Modified: Mon, 28 Apr 2025 22:07:28 GMT  
		Size: 7.2 MB (7206555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a0a4d186c58e93eb9ef0436e3139685ff61b0b4a83087346574054906993cd0`  
		Last Modified: Mon, 28 Apr 2025 22:07:28 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:65daf6af311d69e80daf6f2fe7e287721510cef7959e94ec675a9a931a039299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.3 MB (265297339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2940cfb5eba07866d38799119f3f7f07f0555134e034e49824f3d97bcf2182b0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81a2ebf9d993ea072551f562bc3f4c69216a524aaafb63aed8b85eba29ec258`  
		Last Modified: Wed, 23 Apr 2025 19:47:04 GMT  
		Size: 143.5 MB (143512678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def098b222c26ed0a1d7dc15946f9a177bb894b71de873c3086adca55d797cf6`  
		Last Modified: Wed, 23 Apr 2025 19:51:30 GMT  
		Size: 69.5 MB (69529394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e486f8a3b96efc30eaf724ec576db92b711dfb15323f7ab2835ba0f63c3ce6f`  
		Last Modified: Wed, 23 Apr 2025 19:51:28 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6dc0812b64417f58d84bc7fe7acdcffce0f5af5503aaa2d0edf9528c4e08c82`  
		Last Modified: Wed, 23 Apr 2025 19:51:28 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2dd39311835437f681fc1fd1a4735d7e92f0b6241addf6e7649e7fd3754f7a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7227539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04a0996bb0ffa777e88a52c90dc9e947df5d1032371bb2bcb85279a2ba8a2557`

```dockerfile
```

-	Layers:
	-	`sha256:a71a1e091c34f3f0403bdb8bcf4558afe957178d4edea07645fa436748def4c9`  
		Last Modified: Wed, 23 Apr 2025 19:51:28 GMT  
		Size: 7.2 MB (7211600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a59d4318afb8c48c45acdfb31da106c6e15fb94a863f565e22bc0a682642bcea`  
		Last Modified: Wed, 23 Apr 2025 19:51:27 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
