## `clojure:temurin-17-tools-deps-1.11.4.1474-bullseye-slim`

```console
$ docker pull clojure@sha256:5c67c5a35eb60c0cf1994f80b57218c7fdbee590e45db65b274833c5e04748e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.11.4.1474-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3a573f6411e05a97f06969ef746d5acec1f3eb2334d9b2d398c9c064472edada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235167839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854d5ed78de97f8ba922974d1fc9ad189456b19b5270d023344b25e2e7170e81`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ab073e97ac8da7b00bb6a6d5f9c2f4620ff702cf5d6c1ad2ce10e2fe7717dd`  
		Last Modified: Fri, 23 Aug 2024 20:02:24 GMT  
		Size: 145.2 MB (145166504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a09b186cad1c07583197e5c7d3fb77594804d8453b1e760c80912c8342a2545`  
		Last Modified: Fri, 23 Aug 2024 20:02:20 GMT  
		Size: 58.6 MB (58572005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1194fa4a230a4b2c65496a4331e961cddea98123ca2ca13e547c09fff10df2`  
		Last Modified: Fri, 23 Aug 2024 20:02:19 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53dd6fc8e45d3938fe4dc6e46988d705b4c114eed8ac80ac074568a34e67b18`  
		Last Modified: Fri, 23 Aug 2024 20:02:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.11.4.1474-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c6c235e169baa0d0900f83c3d883f992b78abad458e1d4ce61c70c997eccbd87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4965339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1210bf73d41890262cd8a887caadb5b3a656a145eec5dbe18f7d8ebf9b31da`

```dockerfile
```

-	Layers:
	-	`sha256:89856ffaf0c89a2f2457c38e0e5161e96837d32d0d608651b662ecade9d9d9c3`  
		Last Modified: Fri, 23 Aug 2024 20:02:19 GMT  
		Size: 4.9 MB (4949826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:537182865e46224b74c606a4a18aca3abf36246518f806e2ef39b7a607daedf3`  
		Last Modified: Fri, 23 Aug 2024 20:02:19 GMT  
		Size: 15.5 KB (15513 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.11.4.1474-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b6c958d426df8f900fc474950849292ba068a63265f168ec76a3365863ebbaf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.7 MB (232735526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9cf60f83d8df56ab947073b887d22d4ec21bc199a2d205f36673119b98d9ac`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c229b6d4698a9454e9c62693654360cc097801af308b176ca82da1b9fb41517`  
		Last Modified: Sat, 17 Aug 2024 06:14:12 GMT  
		Size: 144.0 MB (143959474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a91291455040cff420fa71f83969b905d0298ec68183b3a4083c27e86030e4c`  
		Last Modified: Sat, 17 Aug 2024 06:19:04 GMT  
		Size: 58.7 MB (58698920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267b59a924409234079f22c36b94a7313731aca893e2f75448b8ccb01431b590`  
		Last Modified: Sat, 17 Aug 2024 06:19:02 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cebc1f718b2e4690337204eb89c527293ac936bb0719d326401a0945206be6b`  
		Last Modified: Sat, 17 Aug 2024 06:19:02 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.11.4.1474-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ff286bacef7bf7b96c3c68aa68a7a191021de748a314bb30079689855ff2efb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4972235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d82a1ecde09adbbd064c59337e363785fb40cdc74457d01a543a05b05ccc2ef3`

```dockerfile
```

-	Layers:
	-	`sha256:5a20cbca151242c79a0988485107b756dc7bb46423b6dba2692e70aa5fb45725`  
		Last Modified: Sat, 17 Aug 2024 06:19:02 GMT  
		Size: 5.0 MB (4956182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08ef6fcf0d36160dbe12a578b789cb2b2b8370858c41621dcd7d7ac1b22ef291`  
		Last Modified: Sat, 17 Aug 2024 06:19:02 GMT  
		Size: 16.1 KB (16053 bytes)  
		MIME: application/vnd.in-toto+json
