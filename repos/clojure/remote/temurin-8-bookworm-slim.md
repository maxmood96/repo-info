## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:7c9591663a75099ad193d49a9f10d900a9269c94c69e6ef024e7f7314b4cb201
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e40b17295e2cf0f1cb263b357b976b76e32ac71f3033d6cfd85060296d624486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152477228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2caa0cd4fe2da46a992dfaa8114ac979ed7b27cf90286e026f0942f20440fff`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9482b26d5cb7220aa2b058cf61b9a52dca25e8ad321f92f17ef640b39227893`  
		Last Modified: Wed, 09 Apr 2025 02:18:12 GMT  
		Size: 54.7 MB (54721244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2372eb1019cec59436c8db38cb9acfc36f87be1132aa4282fc3c6b054ce645`  
		Last Modified: Wed, 09 Apr 2025 02:18:12 GMT  
		Size: 69.5 MB (69528078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e651c427fad7da9735b555a234e2f932f302627e743e0c0654a00d084466ded`  
		Last Modified: Wed, 09 Apr 2025 02:18:11 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7d8e20d74b806037d17799a594736ca83e0b28a351b25b05549b22774cd7f7c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5049866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310eea8d7503406b32b8f28102f9fd192524663ac85337654155bfae08e2e66f`

```dockerfile
```

-	Layers:
	-	`sha256:70a4977ff62e6b942341f56ead2497c96f4a9d10cafbe4dbc5e8500216db2f50`  
		Last Modified: Wed, 09 Apr 2025 02:18:11 GMT  
		Size: 5.0 MB (5035575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9eee349a3754b271de992eba8096991cf3cff997d158f010afe80bf2c1570ec`  
		Last Modified: Wed, 09 Apr 2025 02:18:11 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d628291b2c41979f2beae7e7e3bea92e756a0b9016066f390a8af2fbca8d7db5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151267197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa54477de742328c8b40c8908247c60862e658631564bb020136e9b5a33ae84`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434b93f7622fedc3ddb5d19dd10d934bb18362a2c3cb11837f3ebb83f2802917`  
		Last Modified: Tue, 08 Apr 2025 11:13:02 GMT  
		Size: 53.8 MB (53822752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b08d45555a70bb3ab33d7969eae4db119e756a0d3eec9d75922e5cd5b26d6c`  
		Last Modified: Tue, 08 Apr 2025 11:17:02 GMT  
		Size: 69.4 MB (69377480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56dfa4b11df9863d54c216453ba550110f7dab114e2dbce362e3757026852c4d`  
		Last Modified: Tue, 08 Apr 2025 11:16:59 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b62ca2fef06357ba1b17ceb60c3019585ac028fd4f94d110624ffd8a83a7d7d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5056443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab6833e952c674f32f79d06c9a3999bc0a17b96fa05440b7959baa17ed26f26`

```dockerfile
```

-	Layers:
	-	`sha256:c3052278833d44608ac4a2d71d40de59dca2e0cbe256a5e831ea3e4022d553c9`  
		Last Modified: Tue, 08 Apr 2025 11:17:00 GMT  
		Size: 5.0 MB (5042034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:093dea7f695eb38ba66251b35bc9feb1f21266fd2eb322b60838d02bd3f68bdd`  
		Last Modified: Tue, 08 Apr 2025 11:16:59 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json
