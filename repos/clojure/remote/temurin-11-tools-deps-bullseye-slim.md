## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:3dd81ae5951de33ea756c7b4959a40d4fae1a329b4796de3b178ca0144382156
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1d0d8684abb788cd158a114d089fd78617bac1f1d20ef8f9ff503d0ad232688d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234610827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:465b1b25b02bce145a4388c8c5cc5ffa51b1ec92711b00ebe7ce4f052d15cecf`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
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
	-	`sha256:6c87eefc1f428634061bcdc9ec95ccceecd7c7475d35a777479af83f64ee6915`  
		Last Modified: Tue, 24 Dec 2024 21:32:32 GMT  
		Size: 30.3 MB (30252643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9156ca0798536b0ff82e87f1ee6915f8b27915a3363ff99a3d5b53aacf5d4104`  
		Last Modified: Tue, 24 Dec 2024 22:37:56 GMT  
		Size: 145.6 MB (145601480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3539948fc54de06c0423c1e729d2827e8931b763aadd2b85b671b47d280440c`  
		Last Modified: Tue, 24 Dec 2024 22:37:55 GMT  
		Size: 58.8 MB (58756061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5463b2443c792448e6a7402987ab0757ba1348cfbfe482505854d2f04763da`  
		Last Modified: Tue, 24 Dec 2024 22:37:54 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:11b257e526a0d6a34796e88f625e7dbdc6e8b8ff969009654755eaedcbbe78ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5151456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f600d77a719325c822edbeddd7284d07e54471c20171ab81d6071ba39aa9c2`

```dockerfile
```

-	Layers:
	-	`sha256:3c32ee727afbc38656b0ed59ca9a465ff87de184f4deda8f6d078b3fc7d80be4`  
		Last Modified: Tue, 24 Dec 2024 22:37:54 GMT  
		Size: 5.1 MB (5137146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a07de9835f2f3fcd436d46f4e193f1a98fb8facccd322cf802948807cfdfdf2d`  
		Last Modified: Tue, 24 Dec 2024 22:37:54 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fce7f5be215d2bc854f13f530dfa6849b377353c362302fac0a98667f1b64800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 MB (230014897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea04b3e656d706dda027c3fa3af9a61874a28a63eae3eab3ede3a3029efdf467`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5dff04b2bf13f7daa9b187569e3dac438596fb37c4f93fe7d65747f4fe8d7b`  
		Last Modified: Tue, 03 Dec 2024 14:04:51 GMT  
		Size: 142.4 MB (142389020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784cef2ecb3d0caffcc594281fd2cb30cb5d16abfa913be8ce35c6ff6a106f50`  
		Last Modified: Tue, 03 Dec 2024 16:14:55 GMT  
		Size: 58.9 MB (58880311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b39d8110de115489cfff712b00eea384021eccf1b1eed9224206514e2736c6`  
		Last Modified: Tue, 03 Dec 2024 16:14:52 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0c3785b359b46151635ea27b8338e3eedab35473189c462f67e5a26883ee138b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5164503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:091b2de8d0edfe597e48dd9b3aa9921eff086b891469f359492bc87ee96785d8`

```dockerfile
```

-	Layers:
	-	`sha256:51d291d6af6d070acf6d4770d97a8e823ef8ab75c7453ed086638d6fda1ba034`  
		Last Modified: Tue, 03 Dec 2024 16:14:52 GMT  
		Size: 5.2 MB (5150076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fffb6990a2a5d072a69e90872bbb6808b56951ede34d98427138376b222c0a9`  
		Last Modified: Tue, 03 Dec 2024 16:14:52 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json
