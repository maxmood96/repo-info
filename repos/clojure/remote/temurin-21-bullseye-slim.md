## `clojure:temurin-21-bullseye-slim`

```console
$ docker pull clojure@sha256:a627cc08f2518e9e982a6a8d20ad7fdb075c2cc2e5185a9e56103723ed890b74
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e1c78b11de0d1a8ba4cd496d4b6d9a2e73f1ea4d14b2dede32b97b1513d989ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.3 MB (247308106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf8b98209bc5fa39dd880c572e4a7a401aa34f734a87a9316ffefaf9922d5a3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:05:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:05:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:05:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:05:34 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:05:34 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:05:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:05:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:05:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:05:47 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:05:47 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7630267f7564171bdcaf989c60bc746580da069489e9945be7b3136434a761`  
		Last Modified: Wed, 15 Apr 2026 22:06:13 GMT  
		Size: 157.9 MB (157857060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3cffe32cbcde9a6777125dccc8385773f5b919b0dfa9c3c6e7e02ec9eca1346`  
		Last Modified: Wed, 15 Apr 2026 22:06:11 GMT  
		Size: 59.2 MB (59191984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f989607a3b35a02b82791e15794d7f4bbce1384facc535535e76f553e2b890e`  
		Last Modified: Wed, 15 Apr 2026 22:06:07 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46c78bf30db179be7bca6702610f41c0c699ffa60d97405a07d44b0d67756cb`  
		Last Modified: Wed, 15 Apr 2026 22:06:07 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:52c42fe92bf8fc8f06b0f9e66e66f87b259f639058e0057ce1e388e500474144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5337740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b96d8aa75ae900f59a52ef14b5183e747384d99cd7e26403d897bda9919eae92`

```dockerfile
```

-	Layers:
	-	`sha256:e287cee5e5a44591eedd046f4bf68bcd657dc1ba504908ad4e8e240efe98a7a0`  
		Last Modified: Wed, 15 Apr 2026 22:06:07 GMT  
		Size: 5.3 MB (5321905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:744c2c76ee7e85cba08350e425a1bc697a04a83152c26c4c977a5c4e7ca69884`  
		Last Modified: Wed, 15 Apr 2026 22:06:07 GMT  
		Size: 15.8 KB (15835 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:02ca382bdd7ff09e6b8f7c7c2cade470b85dc6e42d992f80fdd7735eae5398a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244208622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c1ea436cde2a2679560dab5bbeea2b3f35400e97c491a1c589e76d04d32dfb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:17:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:17:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:17:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:17:04 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:17:04 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:17:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:17:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:17:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:17:18 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:17:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa34eae78d4c0abb2d8e6604191c337cd49e55c331e6fc92520a29d3d6988de`  
		Last Modified: Wed, 15 Apr 2026 22:17:41 GMT  
		Size: 156.1 MB (156133067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5258942260d8384df1224b9e28c72e14089cbd537d1e097c0bae8bde070aced`  
		Last Modified: Wed, 15 Apr 2026 22:17:39 GMT  
		Size: 59.3 MB (59329827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c164be0e65a0e394877768c826d566e8e16e68d3088ae28ba8a59dfeb9edc1`  
		Last Modified: Wed, 15 Apr 2026 22:17:36 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad82164dc0dac5b7904ebc9a9d087f5f8d15e2f704b3281f553d7ba852c21b93`  
		Last Modified: Wed, 15 Apr 2026 22:17:36 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:902f15cfe9df8f4238db6e8446721860909a94c0effba7c58f7d66228fa528a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5343591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2d5af699b3040a70971a1ec5dac0fb1818589032d2113761bb8e1c01ee1c99`

```dockerfile
```

-	Layers:
	-	`sha256:d3c085fc18db3b6ce96b02a2cd611606ccf366740dec63124e50a4f40bb9c301`  
		Last Modified: Wed, 15 Apr 2026 22:17:36 GMT  
		Size: 5.3 MB (5327637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:321717a627ba97e80626346085a96565a553dd7ac6a6c378c8ab1909c2da003d`  
		Last Modified: Wed, 15 Apr 2026 22:17:36 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json
