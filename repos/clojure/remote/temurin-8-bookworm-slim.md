## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:c86c8c3bebf50d2de473eca68c49a5b2eb9dfc4c1028bead33bf29049456b22c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4c268ccaeabaa81b7208e79c974f5f057829e6856f75b8fb8505fcd83ea6d0be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152465804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd6485f1638e75708dabf6f5c27091cff69d892361c1d8c9e9ce27f76600aefb`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09573f7d118b180da5d4fde41955074b8c82b9aa6b609edf29699f3a12f863fe`  
		Last Modified: Fri, 31 Jan 2025 02:13:58 GMT  
		Size: 54.7 MB (54721249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00be8afa89826248d3d8d15fbd2307f2c5f93237f5cf0d7e17acd47b4163c15b`  
		Last Modified: Fri, 31 Jan 2025 02:13:58 GMT  
		Size: 69.5 MB (69531492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9c36dc376e007535936e1cccadf222c3a48741b76b99f7267fbecec434cb1f`  
		Last Modified: Fri, 31 Jan 2025 02:13:57 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:250daf02b010c5bcf865b3a3569e89a7c0013046f4f2b6d00fd9c3ed6c4a982d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5048468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991c9cbc8cfae8fe020fba66d4caea440b85af843be593e058dc5b6f45f1bf6b`

```dockerfile
```

-	Layers:
	-	`sha256:dcd65a1ac0fd4a511eed850250fbe15184c05fa5b05aeb502bfac28d267d4c55`  
		Last Modified: Fri, 31 Jan 2025 02:13:58 GMT  
		Size: 5.0 MB (5034177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c11b0fd1362522e3dacb5e4a3deb7bfec94923bb631d8c809d41879195e464b8`  
		Last Modified: Fri, 31 Jan 2025 02:13:57 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a13a4ce555db259b5baed1f8bfbb123f5427573e174f05e5a9982ba8d4631569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151246148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc99ab21ccaf94b3194c7966e9659a028cb77d17735f8370a647d809eba55b3`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df06cce5db22c11379358b8770d8e45c7b8def7c35a6910da2a498720c17d0f6`  
		Last Modified: Fri, 31 Jan 2025 04:52:25 GMT  
		Size: 53.8 MB (53822735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2dac8c434950e3404f4113aa00db7208160b6d7e11e9fd9f5fa4e3cf4c44231`  
		Last Modified: Fri, 31 Jan 2025 04:57:17 GMT  
		Size: 69.4 MB (69381738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6428f12083007495c4e09b8e5b6182e9b528d7a97a8dfc62faef93274fb1f6c8`  
		Last Modified: Fri, 31 Jan 2025 04:57:15 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0393fee36aef1f3dbde6d078830fbf5de8a01914b112b981cd0f2c4001fbd633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5055045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1d7385b3180bafb412072c62caa899d5eab5610e53eb422814459f4031deb8`

```dockerfile
```

-	Layers:
	-	`sha256:4b2ba812fdb75e4c3cc54d211988562c4503058b740eafad3a25aa5e1b568332`  
		Last Modified: Fri, 31 Jan 2025 04:57:15 GMT  
		Size: 5.0 MB (5040636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2f0d325978daf5ef9a4a4c1547800dc9a608be0c91e444d6dd2b7c0bcfb4522`  
		Last Modified: Fri, 31 Jan 2025 04:57:15 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json
