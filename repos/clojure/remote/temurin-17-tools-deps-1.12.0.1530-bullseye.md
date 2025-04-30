## `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye`

```console
$ docker pull clojure@sha256:4d128e1b3705dda036f2a353bc51759d42ee3bbba28fb029d736b76750914e66
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
$ docker pull clojure@sha256:95bd7b7514df67ef1a88d908f0e17097e9d7e1b77875801575d0d217715ebc87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.3 MB (265289018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5efbd3c247775a8db9e0215646852eafba3fb42ff0f7493bb9b8371e92d30dd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
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
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Mon, 28 Apr 2025 21:20:53 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c441d9b4a0e858b97a1d7c29b1a927fdf6f835e7f9d6713307867ec981319cb`  
		Last Modified: Wed, 30 Apr 2025 01:35:05 GMT  
		Size: 143.5 MB (143512607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a931fdf7ba1225445d2a74248590d09d2ec004e5b3ad55a0a1ac202662015a35`  
		Last Modified: Wed, 30 Apr 2025 01:35:04 GMT  
		Size: 69.5 MB (69529394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8a9e30f5a5a48361248340d469ad25ba73834d2f9298c92ccd9f2bb59bc070`  
		Last Modified: Wed, 30 Apr 2025 01:35:02 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaad5e370a36c0656f41d483ffe67652651b2bccf30cdb84b927b63183a5103e`  
		Last Modified: Wed, 30 Apr 2025 01:35:02 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d50c2c458c9132f5c5bbfef0483ce1c8d7f0bf9f8f9b1dc477b6fbc1a15686fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7227593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461dc1f2cf73e680f5215fe3b783de1a69932084dea0acd714b875b4fb5cff27`

```dockerfile
```

-	Layers:
	-	`sha256:712c07cc0de47655331782ffdbd036271c3c66534911e59182664b591fee142e`  
		Last Modified: Wed, 30 Apr 2025 01:35:02 GMT  
		Size: 7.2 MB (7211654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7e907b0214947770c70394ad2be89880ad5e0ad4aff51449b67c310e83ee2c6`  
		Last Modified: Wed, 30 Apr 2025 01:35:02 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
