## `clojure:temurin-8-tools-deps-1.12.0.1501-bookworm-slim`

```console
$ docker pull clojure@sha256:09ff288b969d724d5b73cb3cd1e21e61ab999df459eb5c04a3e71bcc3144f58c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1501-bookworm-slim` - linux; amd64

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

### `clojure:temurin-8-tools-deps-1.12.0.1501-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-8-tools-deps-1.12.0.1501-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7badb88de385aa92edc5ebbc2784f8b29a1f6275a56912e016fdff3f26e6904d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151245910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e70ca89db849984e17a288f5ecc68b5a57a402063c9e01b37ec64317be03babb`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
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
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369cc069c8bd5d579d827d5defd418fea2cc6c0b401c91c66c1194709652d556`  
		Last Modified: Tue, 04 Feb 2025 23:25:04 GMT  
		Size: 53.8 MB (53822735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d015b06cdfe5b1526a04fe9d8e2d4722b7853e3e2f01a7a1713446c59167f9`  
		Last Modified: Tue, 04 Feb 2025 23:29:49 GMT  
		Size: 69.4 MB (69381652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1693f064217a224e5f58c2ed14701e75e9d1d0e788192359d086cb8894dbdc`  
		Last Modified: Tue, 04 Feb 2025 23:29:47 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1501-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e7be7adb7a51ea2b91159cfed718195f502f15834173d6256bb27ddd14cd604d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5055045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a655d5b851d788fcb18a46fea888443ac168689964df2d367873f49120a86c2`

```dockerfile
```

-	Layers:
	-	`sha256:3f42348d4fa909d52ea68e5f4011782f4668fd74e44ee97a39e4492e1d107f13`  
		Last Modified: Tue, 04 Feb 2025 23:29:47 GMT  
		Size: 5.0 MB (5040636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80c8abcb0eaed161d6781ff5cfce212e1ba2825e0f490acc6a84c423b377e3d8`  
		Last Modified: Tue, 04 Feb 2025 23:29:46 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json
