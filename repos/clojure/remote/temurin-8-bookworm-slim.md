## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:4f1bb28a360e7aa97480f1d1c7e77288f87134a7f59ba7b3c4020728930ac4da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bookworm-slim` - linux; amd64

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
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
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

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c2e05d895c7ea34704acf20729fa13a7ee8d2fbd643c6f493be30e5862205297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.2 MB (200163635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ee4fc98885d3e51364aca388d5413e9516edba9328e96b475fcdae8e03748e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b83bb1fef68478b6d0dd97b3acb6cff6ee3d23805e652dee5532d597769fa4`  
		Last Modified: Tue, 14 Jan 2025 12:14:10 GMT  
		Size: 102.7 MB (102747716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80df508aa71d44b83f591de8cf026278390fc0cec0ac64929ab3cdfb0c993eb`  
		Last Modified: Tue, 14 Jan 2025 12:17:52 GMT  
		Size: 69.4 MB (69374242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c498a0b5337859a552c6f1153e368b9c32a2ec60a224139e4a340b3eaf7923b`  
		Last Modified: Tue, 14 Jan 2025 12:17:50 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5b73fe67a67cf9159ce38364819f3f8419952170a177d007c8818af5dd68cfd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5055660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92d7a7a8ab5eac74189f7647c79c1d95e22b7874eaaa67b5b2d7e7663e943581`

```dockerfile
```

-	Layers:
	-	`sha256:beabd75739d9292757fce18b7ae51330ee5a801569a819ce4694bc6c650b0147`  
		Last Modified: Tue, 14 Jan 2025 12:17:50 GMT  
		Size: 5.0 MB (5041246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07a12513a119ce45fdf0755d5a4739b25e488c8aae97ac3851d6e1d8603aa830`  
		Last Modified: Tue, 14 Jan 2025 12:17:50 GMT  
		Size: 14.4 KB (14414 bytes)  
		MIME: application/vnd.in-toto+json
