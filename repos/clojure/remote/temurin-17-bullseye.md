## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:d474d43634f1db227feccfafc4f149dbc3659cf7c13338668ad220aa4be67821
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye` - linux; amd64

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

### `clojure:temurin-17-bullseye` - unknown; unknown

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

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e6e0b4b911003b256b2b3fd4e81911ef270a5a558057afcf5e51e41e01e74cc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.3 MB (265288767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9a6f585ba1e93fd335fb8f71210ee41e0d20da96a8da08b630088646af8426`
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
	-	`sha256:c15db720bb6866c9beb74c234152feba8348255939932f31dcad2f9f22ef4c80`  
		Last Modified: Tue, 06 May 2025 00:34:07 GMT  
		Size: 143.5 MB (143512639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76a3c49a5436ce2b5d381debba4cf53e07ecf9fca04db6ee5e32f4ea768cb3b`  
		Last Modified: Tue, 06 May 2025 00:38:25 GMT  
		Size: 69.5 MB (69529107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6011b55e73cfb60cc22b189febe95d68d73e1fa0d09152e3c6d057e6d918226`  
		Last Modified: Tue, 06 May 2025 00:38:22 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463b5e4a930035499328dc745c48385c4c2ffa47a52bec35eb17a542d7ccb76d`  
		Last Modified: Tue, 06 May 2025 00:38:22 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d1c37f40a79b3fcaaf493c4632ea7bfb2b252d31118d0d4b82d966a70c7efd31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7227593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60470ed9213f493822629382639960bda8e1277424de6e27a6854865cdb3f58`

```dockerfile
```

-	Layers:
	-	`sha256:575642bd16db110ba38e5dabba3bd39c4a3b3453178163b7a3a12e46351ed60c`  
		Last Modified: Tue, 06 May 2025 00:38:22 GMT  
		Size: 7.2 MB (7211654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5912b974a8f2e209ae474905e68b0564e88d31a6e8757857a6182eb9d95ed19e`  
		Last Modified: Tue, 06 May 2025 00:38:22 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
