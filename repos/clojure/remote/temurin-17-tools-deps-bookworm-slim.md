## `clojure:temurin-17-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:2fec0da5f45adf650a4cf84f21844c28b71f44828e8283141d36765921344456
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8512d9681326bb4492a05c3922641a500122434fbcc5fa26217751600f04b2dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242389436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:092ee15f1707e3c9cb0425e22711834ebf221b89031afcf04fb87b6985217cc8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ca51f8c73c04db6b41b7420d903413894458ccb3ab6a00361f5f27d2476c0f`  
		Last Modified: Fri, 09 May 2025 14:24:49 GMT  
		Size: 144.6 MB (144635023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b70716dda9e4512c85e61acc0d2e28073314132c97b3ce470e31b5576600fbd`  
		Last Modified: Fri, 09 May 2025 14:24:44 GMT  
		Size: 69.5 MB (69525733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e3556ab6be4854261903eb041c25b9736c4e52c52ac989ecb4de250c6fe1acc`  
		Last Modified: Fri, 09 May 2025 14:24:35 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4498ed3211c771753eb0992cfc7899d7cef4bc66b6d71d97a9d84d71599186`  
		Last Modified: Fri, 09 May 2025 14:24:36 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:54214937c73830b5d5816b5e39af4ea72caa82b48ccbd625d5524601088744c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4929844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e4958434d56f2cdb22a8bc596ebee75c1835fb5b2dd93c7cc1c6c9126449861`

```dockerfile
```

-	Layers:
	-	`sha256:e093988c8d528b00235863f7f3a1d3055844d9408e86de465afb6266b4ba58d8`  
		Last Modified: Mon, 05 May 2025 17:07:40 GMT  
		Size: 4.9 MB (4913965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c70676a964e17a599ed510239c3d92dde06915245acfbe7ee8a7704521d1680`  
		Last Modified: Mon, 05 May 2025 17:07:40 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cdd2180abf1e1fe8b1b6f33b362037795c6cf8f8f1f7dd72f2e100e9865475a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (240957950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8600d767f890b095a76b78bb014f050631076cb85182b67179901f8bfdf806f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2269691f73db7860922dcc1e545febb157e0f587c2bb09ab497fe8397ec14cae`  
		Last Modified: Tue, 06 May 2025 00:33:15 GMT  
		Size: 143.5 MB (143512692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343734f3c9f642709b29b2b27cd2b15758101308f752817f746b409cde9d3a22`  
		Last Modified: Tue, 06 May 2025 00:37:34 GMT  
		Size: 69.4 MB (69377596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41b065f7269bf94e797809ca82770fc0fda07ffb5c9387fa49d74c96b6e3bb8`  
		Last Modified: Tue, 06 May 2025 00:37:32 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915b31c5353636ab49e5faf65180c589e39f6d65b2431a3667e7e48a2482518f`  
		Last Modified: Tue, 06 May 2025 00:37:32 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d894d126dedebad0da84871523254702ec6ae37c06159543198597aac0ed3660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4935723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c064540b39eb84984e892d8b34574928e3068ac4b4ee2671f95f65dd869034`

```dockerfile
```

-	Layers:
	-	`sha256:64bad214cd7d94bfee7a773caf2bdc26841702e58e28b07b304af3a4bdfd3267`  
		Last Modified: Tue, 06 May 2025 00:37:32 GMT  
		Size: 4.9 MB (4919726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e16aac8cfaea30a64c677f5563035aba358ff9099be49e300b5b7609bc7e6d49`  
		Last Modified: Tue, 06 May 2025 00:37:32 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
