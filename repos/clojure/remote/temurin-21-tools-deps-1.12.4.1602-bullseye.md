## `clojure:temurin-21-tools-deps-1.12.4.1602-bullseye`

```console
$ docker pull clojure@sha256:e1c05971a4377b066c29fcf9cff8f87f90e0c3ac4b00087badb5a798377c06c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.4.1602-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:240167900f90c9d3601d28d7cbe8dbd9ee457b6814756ca7cf6df4a03f1601ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.2 MB (281156077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72033fb09c74f535db5ae3dedb46dfb95cf6a478c19db3beb44657202f418285`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 17 Feb 2026 21:44:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:44:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:44:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:44:42 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:44:42 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:44:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:44:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:44:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:44:56 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:44:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ee744420bf0675528b9a0f23b36509f68b4666b8451241e6463783cc8df09a`  
		Last Modified: Tue, 17 Feb 2026 21:45:18 GMT  
		Size: 157.9 MB (157857066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad14aea3b10ed4c1f09471fa766b1498276e4b86810f4788c882eb3237045e69`  
		Last Modified: Tue, 17 Feb 2026 21:45:17 GMT  
		Size: 69.5 MB (69541710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a290b16bdd4ef9f916ea758cf3f02939d184c0f29f8c9007e20fed6d66c21896`  
		Last Modified: Tue, 17 Feb 2026 21:45:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67b2ddbb2a63ed4bc59e2ca230c31089105cc7f624534e4114ac75bb8e5d83b`  
		Last Modified: Tue, 17 Feb 2026 21:45:14 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:679f0eddb6d1ec9c43973b18ee6ae1c7fefba3810abc480ad7528d8b5af5318d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7415348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3210fcb96792d77b3adec6510cf7dc1811efd5d3bf1de3dccb96d44abc63fd`

```dockerfile
```

-	Layers:
	-	`sha256:e155f8f7c6fbd8c8791a3fd1d83a1cd1996a7582dae68838bd1f56d22bf9b09b`  
		Last Modified: Tue, 17 Feb 2026 21:45:14 GMT  
		Size: 7.4 MB (7399572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:931e17a1eac82dab86d9242573da572c2363b3a7abdc4a4c41e791019c2f67ed`  
		Last Modified: Tue, 17 Feb 2026 21:45:14 GMT  
		Size: 15.8 KB (15776 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1602-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a8fec194fbe5d077a456de8521ba8235ce9b44a50eaf5e8c36a09252819f190f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278085934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8198b953d44a17f4f5463a2406ac6028b3e421d4a62e2a8fca36378602b6e87e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 17 Feb 2026 21:44:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:44:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:44:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:44:44 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:44:44 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:44:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:44:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:44:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:44:58 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:44:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0742c20cdb1eb0c212cefb0ff441553e29e6ccfa92b808cca3d7e8548a6fd569`  
		Last Modified: Tue, 03 Feb 2026 01:13:54 GMT  
		Size: 52.3 MB (52258320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62956f2eaa59627f43e370a2b4157f821fc3a8a8fa824e2cd0463e3ecebc598`  
		Last Modified: Tue, 17 Feb 2026 21:45:19 GMT  
		Size: 156.1 MB (156133079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50d2db4d93b50f3029652102c2092959004facd81e496ed5cec2ca7f571300f`  
		Last Modified: Tue, 17 Feb 2026 21:45:23 GMT  
		Size: 69.7 MB (69693491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd11a04a2fc255f30c4d81d019a4e670730686cd8b89c542e518e0fa5219f3b`  
		Last Modified: Tue, 17 Feb 2026 21:45:19 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07058ea4f6a5b9319f76a3f8a9147a06b215fb5e31dc4e3caeeda8486fdc35ec`  
		Last Modified: Tue, 17 Feb 2026 21:45:19 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:16bf50bc54581226e4edf2562a97cdd5e23da7bde40f0a62566888c0d9c0ac19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7420566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f5391e7d9d33725c9d17f1c095d47116dc7bbf0c01833731e3cbe71569427c8`

```dockerfile
```

-	Layers:
	-	`sha256:dd72ce4c76a9ccb8afa00e1b76f3a60db26d38478966a93ec2a9c5afe456b479`  
		Last Modified: Tue, 17 Feb 2026 21:45:20 GMT  
		Size: 7.4 MB (7404671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eef54c61071d32639cefc36bd5c8b4b508cb93c99f76c6fed1e3fe88bd0689aa`  
		Last Modified: Tue, 17 Feb 2026 21:45:19 GMT  
		Size: 15.9 KB (15895 bytes)  
		MIME: application/vnd.in-toto+json
