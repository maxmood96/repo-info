## `clojure:temurin-8-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:1e62d3c59471d453efbd08adcc882e5b498ec488067bf1ef8684cb3b35af3516
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7c77d6c1fac7f97b6ba06bd5cbdf1e2f298da0423104f7bd98ddcad807140fef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.4 MB (201373240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942521239d76c1d54776bba889f8b488dcfad8ec0dd592ca5d3588fe96ec5ea0`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460e204999ce5299fef3c7c28d099854a158d2ea164a83656df1a1ccf31647cd`  
		Last Modified: Tue, 14 Jan 2025 02:43:29 GMT  
		Size: 103.6 MB (103633884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fea83de4d9af4f8b3b27e04c2012d8c2c29d2acc5cb5a618d3517db5022fee6`  
		Last Modified: Tue, 14 Jan 2025 02:43:32 GMT  
		Size: 69.5 MB (69526296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bdf83267af9f7cce4a619d720b1faa4e5a34c21d8e0c1220d80f58cd2ac85db`  
		Last Modified: Tue, 14 Jan 2025 02:43:30 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:64d4cf73f3871c3d4b13d0bd95ed0a93e9357252ef389f74fe8912ed9bd24352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5049082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e5b6f3d6a7b8d1d77fe7033e43e3dea3a16e23a9a43f58bf243e87d4e0e7b31`

```dockerfile
```

-	Layers:
	-	`sha256:3b97477585071cfbe4e2496079262a21f557e4fecf1911860ffaa2ebf1197d47`  
		Last Modified: Tue, 14 Jan 2025 02:43:30 GMT  
		Size: 5.0 MB (5034787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90fe0f18730262a3079476aac2650e0121110dc13acf347ad670838cd97c3c0f`  
		Last Modified: Tue, 14 Jan 2025 02:43:30 GMT  
		Size: 14.3 KB (14295 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5ca5826fcecd8be35d873bdb050452d653fae95b9eec07b2f746864d8be95558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.0 MB (199977462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22f91f2720d8b10e655881ea221afe59130e3bc9b48ba2e4890e51408cd64974`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1cfe902e794cc801f92f679144f5d6a2eda6c1dabe35ae94bc730cf925e2044`  
		Last Modified: Wed, 25 Dec 2024 07:12:06 GMT  
		Size: 102.7 MB (102747754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f1e0bbfd776737f464b199c9498d165f4e5e42971e48f909603970b239b910`  
		Last Modified: Tue, 07 Jan 2025 03:17:35 GMT  
		Size: 69.2 MB (69170341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2739e21587ef006c5fe334d16ad45ff9b7a4a5576722d4434b87b1e43bf2c991`  
		Last Modified: Tue, 07 Jan 2025 03:17:32 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8ca6acd2f495b564c8a7eebd6e1fd8f5939cfadb9e6a313e4b36cc3b6667c6f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5055660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:226484b443d2b1da1c5613906033438fe14b430b3b6d9b5bc0c52c8b22180c7a`

```dockerfile
```

-	Layers:
	-	`sha256:c75e3a29e777117afbb9842412d546d578e32398e5c1fdfb265efedd915866a4`  
		Last Modified: Tue, 07 Jan 2025 03:17:32 GMT  
		Size: 5.0 MB (5041246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7df7c6cfc7b4dcbabacf988498c9de77406d0867fb301328c8cda9a23c8c7f74`  
		Last Modified: Tue, 07 Jan 2025 03:17:32 GMT  
		Size: 14.4 KB (14414 bytes)  
		MIME: application/vnd.in-toto+json
