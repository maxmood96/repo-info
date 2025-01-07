## `clojure:temurin-8-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:db8c2d298c4fbc58035f92569a2703b6c492c5e07892277970a31ee410da0312
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
		Last Modified: Tue, 07 Jan 2025 02:29:15 GMT  
		Size: 5.0 MB (5034787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21d7620e0dc59591b1d5f2e5f1ba996d0d446d68a41096b2ffa080c3187b1771`  
		Last Modified: Tue, 07 Jan 2025 02:29:15 GMT  
		Size: 14.3 KB (14296 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:da560122f746fafe01275344cf1e7b33ab08cfd4522c2f9d4ef7ef4cad8536b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.9 MB (199948249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0848ae82a8c6aa3452302aa7132c838ee7e84228ed9b3c43530ed714757b61a`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
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
	-	`sha256:bb8ff4d546d430e27c2d41d8e7f03f20ec420fefc32c5a86451ee0831952c51e`  
		Size: 69.1 MB (69141129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819f344ed1e0ae6483fa78f982519849e110447f9a75ae044c6bbef14dcfac49`  
		Last Modified: Wed, 25 Dec 2024 07:15:32 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5cc1260095cea2f5f4f8f2ac5a33edf98a06fb74af2cb33d0fd10cc5aaf76c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5055597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c828d280f8365d2d3e7352974bb246b069ff2089422a3f1864334189b05ff7`

```dockerfile
```

-	Layers:
	-	`sha256:a77724acb0195d56c90925c0200514d0348e8f5410db437e0c9f0e502f715de0`  
		Last Modified: Wed, 25 Dec 2024 07:15:32 GMT  
		Size: 5.0 MB (5041184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15be42e8fb5712f38acb3966622b3432f62e463d11908eec3825980ab0c93125`  
		Last Modified: Wed, 25 Dec 2024 07:15:31 GMT  
		Size: 14.4 KB (14413 bytes)  
		MIME: application/vnd.in-toto+json
