## `clojure:temurin-21-bullseye`

```console
$ docker pull clojure@sha256:acda748b2e5a6eee37d032f6578de75dfd49c96153cae0b0cdc526d3f71c3faf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:a2c6b06d91da01c5ea5a9e076d1769240067b154deffd6a612bfc3c14caca282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 MB (281533677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525a0d020f6152411e3c51eb94dec735fd4b766c8dc40a1b03dba6a5cb77a520`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 15 May 2026 20:15:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:15:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:15:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:15:23 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:15:23 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:15:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:15:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:15:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:15:36 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:15:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1c662d8f6b122c4f09d6ae1b210df55a5ba6e7b529807c0757ccba0c1ac508e0`  
		Last Modified: Fri, 08 May 2026 18:23:06 GMT  
		Size: 53.8 MB (53763343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3048568fdf641fc9ca600abaaf7e6e6c6dc02a3674e24141b42002e162d039`  
		Last Modified: Fri, 15 May 2026 20:16:00 GMT  
		Size: 158.2 MB (158166937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9c399701d9fffde6586d879e62f841dde3a4c18fb545e25958963b6c35637b`  
		Last Modified: Fri, 15 May 2026 20:15:59 GMT  
		Size: 69.6 MB (69602353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13892780f040e9a8f6c58615953ef9769deb30c6dae71040de6171b7ee9d6ef`  
		Last Modified: Fri, 15 May 2026 20:15:53 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2825fc176a71c11e1e33764076755d76c746b8d67d1d93841d016a5479b8aa`  
		Last Modified: Fri, 15 May 2026 20:15:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:bf8f7494b1e2c0c3180b53fb0f8b26e67160ee32f0d607b807de76b504ac2e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7426062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7364a4bbb2eb8c629c7c941e1c77d57438eda11b83f1d432570111e4602fb1b5`

```dockerfile
```

-	Layers:
	-	`sha256:231e970bff303015c1c9105815ffbf0b027730a2759597930ab5690a4bf85e26`  
		Last Modified: Fri, 15 May 2026 20:15:55 GMT  
		Size: 7.4 MB (7410130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3231445b19bb5e3d182e1952087b4238c0716cd01f427e7f099f0dffcbd97c88`  
		Last Modified: Fri, 15 May 2026 20:15:55 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5d1bfa54ebfcd0812305028a1b1f5fcd368a39154dd8d969cb0b7f67a29ce73e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278486563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07b3d53ee9bd6d158f0452cee14183248eacadef653f1dd05925057e8a1c1b8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 15 May 2026 20:15:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:15:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:15:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:15:22 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:15:22 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:15:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:15:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:15:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:15:36 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:15:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e298658925248ad4cc3d09090535e679c488343ac01aa6168c285702bd451d69`  
		Last Modified: Fri, 15 May 2026 20:16:02 GMT  
		Size: 156.5 MB (156461324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28e0b7874785e516f86016eb51747c6a14d942785cf330375c58154f6bf545c`  
		Last Modified: Fri, 15 May 2026 20:15:59 GMT  
		Size: 69.8 MB (69770985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9945af1d200e5556c9e49dc8d73d3176b6928eef458e08de5a39d3ada5714f`  
		Last Modified: Fri, 15 May 2026 20:15:56 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babe8810d377e7e6db51c4a3c23af98bf5c21e201e9aea635861ed80aaf81d2f`  
		Last Modified: Fri, 15 May 2026 20:15:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:67db71de6ed4d3cfc264166c4e29f668db8d7c854a8029e7f75b68e349fa53db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7431279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9565558d9d136a1d2f82e95451ed63c9cb4de0470c8c4878e19964fe98ba9d`

```dockerfile
```

-	Layers:
	-	`sha256:2636b6bad4e1672f9642d532c7e21af33f91c55937f17ec674aa47ad58a196cd`  
		Last Modified: Fri, 15 May 2026 20:15:57 GMT  
		Size: 7.4 MB (7415229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70765c6325079c752d2964141704780b4bdb75c98790bea8b4ec377a26981c15`  
		Last Modified: Fri, 15 May 2026 20:15:55 GMT  
		Size: 16.1 KB (16050 bytes)  
		MIME: application/vnd.in-toto+json
