## `clojure:temurin-11-bookworm`

```console
$ docker pull clojure@sha256:affa40c0c07508de45beae93daf9086913c7ac633858ad2c19086814dd62812e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:7cdae752a9fc21423e4b59244d94483100208d13c5b7f28ec058d22071c84de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.8 MB (275806071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad66033c91794e2b993a546794ac92e41c47970b1d55068573e67a01c486b48`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:36 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Wed, 04 Sep 2024 22:30:36 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c99875eebe4850e399f045e382edbf96106aa5652ecb0782da125f00360a86`  
		Last Modified: Fri, 06 Sep 2024 20:58:16 GMT  
		Size: 145.6 MB (145550077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cf50eaa19818e123ce79a4e806e0b2b558794eff0120a24cc57bc81c56ad06`  
		Last Modified: Fri, 06 Sep 2024 20:58:16 GMT  
		Size: 80.7 MB (80698646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421d00b5d2c4be82322f0080f8a1be7908e5d94e193f01b3282e3ecddb78c4cb`  
		Last Modified: Fri, 06 Sep 2024 20:58:14 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:da7704fcf3fd2f6945144dc2de4dc1d305bc6c0ee20e22c73012cd55ddedd8f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7013336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a15f19ef72314c1371d09a97116d10a451096765f9b9317ac589cf98cb43627`

```dockerfile
```

-	Layers:
	-	`sha256:eaeffefceb72702a2d296a5b1a2ca7769825469961e46657fe8bc625fe544f95`  
		Last Modified: Fri, 06 Sep 2024 20:58:15 GMT  
		Size: 7.0 MB (6999471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:891dd7909b28c5b51d9d8aa87bb613b4a374c1b33f145b9d6719e296ba5fd678`  
		Last Modified: Fri, 06 Sep 2024 20:58:15 GMT  
		Size: 13.9 KB (13865 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7fa6008897cda9cc33613448761c08c1ed74309e26d9f88a5de7546992369f98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.4 MB (272388553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc27447d76c8c672836092984df350f987f481e89a0eadc5c0406a507c77ccf`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:42 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Wed, 04 Sep 2024 21:39:43 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393395a4d0c87c9bffae02a06bee32000ebf6954efeb8794bf23fefff730eb60`  
		Last Modified: Fri, 06 Sep 2024 21:10:13 GMT  
		Size: 142.4 MB (142354818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0b2d5e7b01fd0db416433dde37a55c7995c5266bb78ec700cf4dcea9ffe398`  
		Last Modified: Fri, 06 Sep 2024 21:15:14 GMT  
		Size: 80.4 MB (80447465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae5331fd0854d16c97efd010c51c62df8c97b9b4ff814f9285afad771479fdc`  
		Last Modified: Fri, 06 Sep 2024 21:15:11 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b270e51f6d84686299a383cab52ebd81cf56cc6ce56fed9f28abb38a05808149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7020259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ce2956f639b8b0daa897738e8ccd4e1026f36ec1edfd2ff3496b085a6b76be`

```dockerfile
```

-	Layers:
	-	`sha256:b4ba3bb0468276fd4e7e17e5fed3ed5862113f35802f5c9eb24dddf20a393fc2`  
		Last Modified: Fri, 06 Sep 2024 21:15:12 GMT  
		Size: 7.0 MB (7005858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f100dd00c7a6efbf0cb8587d18ffecf604c403fb7ec4f79e42f02c7b13af4175`  
		Last Modified: Fri, 06 Sep 2024 21:15:12 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json
