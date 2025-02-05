## `clojure:temurin-17-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:32c3e6d7bcc9a4c4231d57baa185f5b3aca30732873de4365c899333e1384b63
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a8e89ab9d80900f81c8abab279d8aa15112c743facd86c6c88e8838bec697acb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233607954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b9ad39f11eeeba7130cf126bc701476dc770323ee3d8ae7f0699bf56ab47a6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f354d0c243639024e6b8ebe6a50ea49a87b3f125a6b05c59b864607763bdcebd`  
		Last Modified: Tue, 04 Feb 2025 05:21:28 GMT  
		Size: 144.6 MB (144566522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4b02f4c1fefd727d3cd53a16ce49cd60b3072a9c48bba8d94eafb641139539`  
		Last Modified: Tue, 04 Feb 2025 05:21:25 GMT  
		Size: 58.8 MB (58787804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf34abcced0b9ae3a567eb52e6407e150a0afb607520d3be17c01f1703d698b`  
		Last Modified: Tue, 04 Feb 2025 05:21:22 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2838a0bb4d9287b3a6cf2296789271a55eb40c92621431fcb6e946fc57ba9fc7`  
		Last Modified: Tue, 04 Feb 2025 05:21:22 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:59b165504b77bc1e22e6aae43d7482ad596bd80c070c4698c6731f6e6887f0ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9fa1d7ce0fc85eb4940d1cbfdc60f9a275eb6363169726f4a6c0698cb252130`

```dockerfile
```

-	Layers:
	-	`sha256:4527aca0f536f156749b7f92e4a6710857d41e8269f6c86614318a38930eaef7`  
		Last Modified: Tue, 04 Feb 2025 05:21:22 GMT  
		Size: 5.1 MB (5117067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f79fe451a448fe504209d6332d198d9cf8fa6f39bd0994c42ccf73af6e2a1eb9`  
		Last Modified: Tue, 04 Feb 2025 05:21:22 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a8d1fe5ef27c0d946513e16b0889ed329611cca9c538fb6a7f06f3ce4159ba1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231109422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4397da02fd82b01c5d553dba189922311d7dab4b6830347e982c1b54b9f1d0e6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 29 Jan 2025 19:11:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9225a2a808e874449ee822a282882a3c331aad2f5093c1062e16494d8bce3e9a`  
		Last Modified: Tue, 04 Feb 2025 01:38:25 GMT  
		Size: 28.7 MB (28744810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348ff9ac1b37388eb3a2a2be1629fee6895100908a9151629f94915c2adee8bb`  
		Last Modified: Tue, 04 Feb 2025 21:13:28 GMT  
		Size: 143.5 MB (143454729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d63f8d6ee165ff06e5c814fd9290da5d74890a48ed85be398167be9e20701d1`  
		Last Modified: Tue, 04 Feb 2025 23:49:31 GMT  
		Size: 58.9 MB (58908845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af10e822e4978531eb274fa94a2db760e61f06d6e91333511d7ea3be92590a8a`  
		Last Modified: Tue, 04 Feb 2025 23:49:29 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1a92d57d0acd75687debdb8298dc0650e87637db076dcd3db3e345ee2c4b10`  
		Last Modified: Tue, 04 Feb 2025 23:49:29 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:992b0d9f4e317ad3cda83962455be102f0241f0002973cea5174db4c5c50599c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cfff138fab6dcd3a023bdbfd274e70bf1f30f78ce160bbd11ef5fdb07286dd6`

```dockerfile
```

-	Layers:
	-	`sha256:6d2bd2e7948eb9a3c3b51ace9e2ba966d8041cb25710e0aacec3e1b57f8cc809`  
		Last Modified: Tue, 04 Feb 2025 23:49:29 GMT  
		Size: 5.1 MB (5122799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9d5a2572c2f2b0428e0d8d828f257cb098696597e6359279387b4330d0fbb1b`  
		Last Modified: Tue, 04 Feb 2025 23:49:29 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
