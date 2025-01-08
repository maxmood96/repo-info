## `clojure:temurin-8-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:6db9f5364d3bf5e647ce2ca077a8809eb1b2dd5a1999e657ea97687a7f1b918a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4e65fb791941d40cce4c855bd92412fbb276fec43d0fe409eb4208c142338cd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201179126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987fa3c309792ac81a3ac1befe63efa98d63c2d80a7f0009e5cac40bb1181643`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
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
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45609a55802a8310ad918e4f02c95730d9dc808b7e578b43435225fcf6552488`  
		Last Modified: Tue, 07 Jan 2025 02:29:16 GMT  
		Size: 103.6 MB (103633936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c8d27261ffd2581677ca932f7b3aa4ef53366281f70500d5298f34bf4f68f9`  
		Last Modified: Tue, 07 Jan 2025 02:29:16 GMT  
		Size: 69.3 MB (69312965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4e75acd7be3cc7280ecf4d0f07847e3fa418b2eec2a3014f9fe0a87dfb3d85`  
		Last Modified: Tue, 07 Jan 2025 02:29:15 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:389acd847d2f919db8e319ec48d75a13e2c2258ba3e69452901b470c2e310732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5049083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9658b2482e4b7aa3e567c0d11dd4c9fc7a48fbe9e0cc3d05f8d93cf946280f3`

```dockerfile
```

-	Layers:
	-	`sha256:c48bd4b18cc6f8014573dd23bfb53eba9b8bf7c1d964c4ec64752f94d9d86e45`  
		Last Modified: Wed, 08 Jan 2025 00:32:50 GMT  
		Size: 5.0 MB (5034787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21d7620e0dc59591b1d5f2e5f1ba996d0d446d68a41096b2ffa080c3187b1771`  
		Last Modified: Tue, 07 Jan 2025 02:29:15 GMT  
		Size: 14.3 KB (14296 bytes)  
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
