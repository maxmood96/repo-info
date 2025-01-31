## `clojure:temurin-8-bullseye-slim`

```console
$ docker pull clojure@sha256:4c95be7474ede454fb2b63206cdf0011a5f079a591852f423bfdbf5aed8dfc42
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:344c11bb3977e384d9478e9fab525dad4d1caec1cec3b30b1d165e40123f1918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143752994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef3e4f926eebc9ee716e29cc9949b91f75e175d9185afd660747858394ba4da`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
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
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216eefbf26a2dfbe22b2ab5d750b81140744e426ca203e4873391a6682d79b3b`  
		Last Modified: Wed, 29 Jan 2025 20:27:38 GMT  
		Size: 54.7 MB (54711727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab09998309b09843c5c8fe710bf714a15c40aa94018d7ba3b51b647e0708027`  
		Last Modified: Wed, 29 Jan 2025 20:27:38 GMT  
		Size: 58.8 MB (58787956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b01fe6c918f2fd795ad1e02136f4c980c2cfcaabc99e806dd0f6fa56ab050df`  
		Last Modified: Wed, 29 Jan 2025 20:27:37 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:729047f0dfb5fceafebcb21e31e0e6f2994edaab7a604b41f1b9511e63696652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5252967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cbafce94d9a5854c55d8c9d77ee3017961c402bc6d963af4c056b5842c760f7`

```dockerfile
```

-	Layers:
	-	`sha256:9d3f54d58dde47ddc77e6651d19d35f6dbdbb5e8ebd1240696ce8924c0cb05c8`  
		Last Modified: Wed, 29 Jan 2025 20:27:37 GMT  
		Size: 5.2 MB (5238677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b97d36edbe366378e4aeeb8e7164d47fc1dc0dc85d667bc197886ff7693f900c`  
		Last Modified: Wed, 29 Jan 2025 20:27:36 GMT  
		Size: 14.3 KB (14290 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8b351e2572d79a475c33c50e278d7a03f19518c7ee419f31c6ad958d6693ebf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.5 MB (141471064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b25893b036fe81ed98c94e09bc87ca9916cfc10ec875e20e4dee911d2cc435`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
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
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d98c3b0df4d7e43fddbb9464d103364cdebc6bb3887c057766dc088321ed2cb`  
		Last Modified: Thu, 23 Jan 2025 02:27:53 GMT  
		Size: 53.8 MB (53816395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4986db85260763defe92a8dfa9f2445dbcdaff02be2c1ff4f1fabf63c2165357`  
		Last Modified: Wed, 29 Jan 2025 20:40:25 GMT  
		Size: 58.9 MB (58909112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f18bc276de719ee0df8b7e3476b1ceb29baea903720ce130313ea792fa0deb`  
		Last Modified: Wed, 29 Jan 2025 20:40:23 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6b69d1dd7382ef4a23ec0e8d9bc77e0c45e32c9a590a39acfa8675259214365d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d830e1b69e47edc458b8ddc5b9b4cf71c36ec232f0a443addb020e812e2a749`

```dockerfile
```

-	Layers:
	-	`sha256:b35bd248017d42555bb65a410452863ade6ffafe030f4dd851bb70206377098d`  
		Last Modified: Wed, 29 Jan 2025 20:40:24 GMT  
		Size: 5.2 MB (5245107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c9503a66fc1fc52e8d03d86cdafeb86c6ae2ded7cfc3c91b03eb5e084a4be95`  
		Last Modified: Wed, 29 Jan 2025 20:40:23 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json
