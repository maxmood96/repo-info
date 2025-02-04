## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:9321b873bf56ae4538bbdf0cc3d37b95cfe24b9806d9c7c5e6a1d216688737ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e8eeefb18f668243c72f3641e387ec7b9809d3098aae552415a30b63df94e24d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152465709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebed26f8ea94a58a52ab4619e92879ac350bd2d2ba2ad8cb86419c75a0212ae7`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29095b55e076344a3bbca81eb22a309e8665171416c55854c07118e296e1447f`  
		Last Modified: Tue, 04 Feb 2025 05:27:47 GMT  
		Size: 54.7 MB (54721258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3cc32b5c27e4ebc664a71b139356fc510ddd3f9e7ee512b40bf7355544c043`  
		Last Modified: Tue, 04 Feb 2025 05:27:47 GMT  
		Size: 69.5 MB (69531503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4332715fbd8b7b773fc7b7d227d14b858703e74e9f04c023bf9d60f13cece2f7`  
		Last Modified: Tue, 04 Feb 2025 05:27:46 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c3da9845ba7f181483995c09113e82430c12ce46ab6897acd2f72cb1d4b7191e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5048468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4759b2f6f77d822e961661c9b6413685aef47841f4bf9559b13f20be98ee12cd`

```dockerfile
```

-	Layers:
	-	`sha256:86bba673b0cea89494438e56699568ae2e2042e638a01ff18f91bab448692c6d`  
		Last Modified: Tue, 04 Feb 2025 05:27:46 GMT  
		Size: 5.0 MB (5034177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9878f5ba972b3cb05e0683ad0bf2bef88e200ede6eef3b75c9beef09b8a7f9f4`  
		Last Modified: Tue, 04 Feb 2025 05:27:46 GMT  
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
