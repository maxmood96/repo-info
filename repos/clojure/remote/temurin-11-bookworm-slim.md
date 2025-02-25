## `clojure:temurin-11-bookworm-slim`

```console
$ docker pull clojure@sha256:1179e884eb9b5e7aa25a3f1fedca5df881e7297fad82599ec469216b855624c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5f8d6c6fe77774fd1642b0c272fc4f465dab16089a1da60f4fa72f6a2e3abd9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243349301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7380c424ef6ba5ebb58eca0f3ba8fcf711dad943c7546a10d17a9f2d9c3ed56a`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60142f10a5604d4d6c4532056fe5f1ec19b6f118972b98028c0ebfba9f7c3c9f`  
		Last Modified: Tue, 25 Feb 2025 02:16:05 GMT  
		Size: 145.6 MB (145598925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffbf6c8d59020c0ab1a3bad975aca975b918f90bc1be1399b4d2890b9223edd`  
		Last Modified: Tue, 25 Feb 2025 02:16:04 GMT  
		Size: 69.5 MB (69530427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d6d223edbafb45a9fc0aada54e6afa0388d5dff60368bb80d953125d307e3c`  
		Last Modified: Tue, 25 Feb 2025 02:16:03 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:692654187bd2aaea6cd9c710716ebf071ab43a00b320164874c746e6a911b5c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4947036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73bb7e731971bfab68cc9119c0f7e71a4500388d6680d255ce9764ba8260ac47`

```dockerfile
```

-	Layers:
	-	`sha256:9f3dadb327192bec0815595a57d3bce93d9623a1c5625b5424672b5c328b25e3`  
		Last Modified: Tue, 25 Feb 2025 02:16:03 GMT  
		Size: 4.9 MB (4932726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd1e47b07bbe4a87a72029c2261140feb966f457a9e4ec4018d906b2a4a67d32`  
		Last Modified: Tue, 25 Feb 2025 02:16:03 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e5a710874a55be2d053d3838b49db98c16296949da4fd5e2ea0f1c0324849531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.8 MB (239806423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:669dc15566a407adf6bdb62f5c969313dfe3175f9109fd74ea6a6107b3ccb87d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f305d71243c4cf4c22bc4b182c9302eb11b39dcea5a584afbcdb527687c5af43`  
		Last Modified: Tue, 04 Feb 2025 23:34:25 GMT  
		Size: 142.4 MB (142385472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c099384bd2e9d12835c7bd5f0430eb9014d68c379acdfbb90627056f92129992`  
		Last Modified: Thu, 20 Feb 2025 03:46:05 GMT  
		Size: 69.4 MB (69379426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3120a50f6c57a2cccc4a44b8c6e6f01f7708c00801e658a50a4a71424cd31100`  
		Last Modified: Thu, 20 Feb 2025 03:46:02 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cce07ac57122cfba3836cf0f07150757305c49279eaca048a93d2415ab091382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4953515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6bc730c35db8eec92ea112d90648912b648e71a724d67e358bcf64a377c751`

```dockerfile
```

-	Layers:
	-	`sha256:4b89ee98ee0bcec4bc5d26b84126de856d11a384cd094556421825c88646e3cb`  
		Last Modified: Thu, 20 Feb 2025 03:46:02 GMT  
		Size: 4.9 MB (4939087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5ec2fc09985d11d1aba2f854c5eacb5e324108f3872ae57e7de9c2abd801b4d`  
		Last Modified: Thu, 20 Feb 2025 03:46:01 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
