## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:d43dec7dd86f55690395838a4f3b016c83907182df50a25ec86a25df913eaa05
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
$ docker pull clojure@sha256:752a28d951ef930f0582ec3351b67c27988379cc460b674767feb077af5aedf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 MB (230014508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:477e3dc4ecafa85dd1878a484308a2dda29d95e1755a1a8b5305bdac3db6d1bc`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
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
	-	`sha256:879a6187682fc52c69294a2f450abdb54e257a50e8133ec6e89cb140345be6ce`  
		Last Modified: Tue, 24 Dec 2024 21:34:50 GMT  
		Size: 28.7 MB (28744853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d6e8a0ecf26b49b1c4a639d091d9deb08eb6ed53b180dd11fffa44874f935f`  
		Last Modified: Wed, 25 Dec 2024 02:17:17 GMT  
		Size: 142.4 MB (142388996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b423299a06603c95b6257b4912f91042c3c18fd8022844810da5fb0cc5f1daf4`  
		Size: 58.9 MB (58880014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e03097a5879988990ccd5e838ed95ea3204d7ab541f926c7dcc3de9aa7bf5b2`  
		Last Modified: Wed, 25 Dec 2024 07:23:43 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:632cefcf37e8b36566c1ea278ff0c7642d56d0c4f62987808ea3ff2eb987c939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5157923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b467abbbac43a70267695135aa7708d6a57351b1414ccaeaea2c4cfbb32479c`

```dockerfile
```

-	Layers:
	-	`sha256:4f9c5d906f88b4a73352b728cc9625f3f82c0c5e81931f1a9c401a896f772e7a`  
		Last Modified: Wed, 25 Dec 2024 07:23:44 GMT  
		Size: 5.1 MB (5143496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d82fe1f7725cfb13c785a70ff5961bde16f84c3c04ef5f40d240cc6beb981e5`  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json
