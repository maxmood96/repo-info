## `clojure:temurin-21-bullseye`

```console
$ docker pull clojure@sha256:97e4359b792545e377d4ef0ae3703daa2ac18cd7291b5c0a299e5afebf942445
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:015188d5c8580627a270278719c01acb5ce9d80effd020870212f57ad4766d32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.2 MB (281208082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb03210f6ea778939281d883c5391a73acf5af76e88545cdb67a698c4b924ef6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 02:59:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:59:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:59:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:00 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 02:59:00 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:59:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 02:59:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 02:59:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 02:59:56 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 02:59:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e759575b5b0029fea51256b7ad3afa90c8ff1a6a9457787359c2b05b4a964edd`  
		Last Modified: Mon, 16 Mar 2026 21:52:53 GMT  
		Size: 53.8 MB (53762481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088e979cb2fb1d2494e2eadca33d30761342621b61f8f00c4d40673685b8ccb7`  
		Last Modified: Tue, 17 Mar 2026 02:59:36 GMT  
		Size: 157.9 MB (157857117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c055417d672d0f26e3264a464734daabe0ef18736012b76bb089578ac82874d`  
		Last Modified: Tue, 17 Mar 2026 03:00:14 GMT  
		Size: 69.6 MB (69587446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fee75b3c208c86cbee00ee8a2afb87a178855b746affe03a532a63fca1df7f9`  
		Last Modified: Tue, 17 Mar 2026 03:00:12 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0012350e5f2f5e3b40d75847b70b9d911dc5641aa392ae4528236287d5bafa6`  
		Last Modified: Tue, 17 Mar 2026 03:00:13 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3ff7d69aa1200880dd4ec0792ea544869779b958733c2f7ae3dc77cd78e13613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7425283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16bc5873ece65aa574e49eb1293bd8ead7c72aa5d0327cf41fa1baa7d69537c8`

```dockerfile
```

-	Layers:
	-	`sha256:0ce05f21529ee51422add6425dffdcfe4692aa90e2dfb5949a2a5fe310ff4c3f`  
		Last Modified: Tue, 17 Mar 2026 03:00:12 GMT  
		Size: 7.4 MB (7409505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04199897dc5b6bb5fbbbc9ba4c3a0174c8a47f57320ef04c776d79977714fa14`  
		Last Modified: Tue, 17 Mar 2026 03:00:12 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:577ba94ae896d10545b5d543290c0589e97b0be6dd5c9a879a1980c56cedbc6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278109724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06e05b4343c022e8a836df5a2530f91843f1414f79b75543bc6bebf84ef9b5d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 03:04:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:04:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:04:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:04:32 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:04:32 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:04:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:04:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:04:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:04:46 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:04:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:da8e260297fdb91b3f012b26dd982feb43d0bf977ff8adeb7a850ef9c5829770`  
		Last Modified: Mon, 16 Mar 2026 21:52:51 GMT  
		Size: 52.2 MB (52247254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a83ab3dbff79f8f09874ed99952039e0118b8e2417680670858faf1e93e294`  
		Last Modified: Tue, 17 Mar 2026 03:05:13 GMT  
		Size: 156.1 MB (156133120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0766e762d29bc873dc424aa0208c7a6f9c60b590220522134702360c87bd24`  
		Last Modified: Tue, 17 Mar 2026 03:05:12 GMT  
		Size: 69.7 MB (69728310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c380644d6e001a1604879fd5cfd6c517d793f33aedfe2611f141da18531a564c`  
		Last Modified: Tue, 17 Mar 2026 03:05:09 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ddb7b8b10da60b74eb294177a05dbe122d1d6686be6791c295629214366aff`  
		Last Modified: Tue, 17 Mar 2026 03:05:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:0ae00504a58ff56cbc51ea51ffdb49cdc7f591fcc32e6e53acb63d5b0c1338ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7430500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dc1abcf112bb46a2af1e0791033710987a010427298870d287b78b5a4987220`

```dockerfile
```

-	Layers:
	-	`sha256:6e99d92f7de63158e421fdae424de172e8fd516642fe5e5b5f0f6fa016976f99`  
		Last Modified: Tue, 17 Mar 2026 03:05:09 GMT  
		Size: 7.4 MB (7414604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02548c5f61fe4066c4ebd341c38caf000468514a31277d4fc11017870b96e4f5`  
		Last Modified: Tue, 17 Mar 2026 03:05:09 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json
