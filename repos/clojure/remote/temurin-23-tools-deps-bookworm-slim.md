## `clojure:temurin-23-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:555f8efb2a02b7625b74956bf57f4f53841bf16efe91678b756184ecd9155f33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:61e784f3e70909587e54b87f8135a56c6493b48f209391b34c42944c0e3bc2b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263066726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:930048f9dfb614d4ea08d3e7050037272768b53c727ebb6a03ccccbfdd10cdcc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c144a35df342cbdeced747028d12847c39845eb8c430279c798a2a997de05966`  
		Last Modified: Tue, 25 Feb 2025 02:35:55 GMT  
		Size: 165.3 MB (165316182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1f07e82c82561294eb2fb2ca995abe60428e9a56ea4aab188bd61e553aaf80`  
		Last Modified: Tue, 25 Feb 2025 02:35:51 GMT  
		Size: 69.5 MB (69530202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d79478f9606f198bd1b4c7ce071ee9a71a2b0fd09f66a6113fcfb6dc8fdcf8`  
		Last Modified: Tue, 25 Feb 2025 02:35:49 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad39fda5a689241e98dccc4b0e57f80b4dc8d02fcfb965a6762329626137e1d`  
		Last Modified: Tue, 25 Feb 2025 02:35:49 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7b358dfee3614c67c93f4b13a017dbe73ebadfe7dbf55cb6b2e60ebfb74299c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4933468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66a09467a2356ed2f719c7f7e96db4836e6a0f83dad80e5202b326cbd0a50dd6`

```dockerfile
```

-	Layers:
	-	`sha256:d5a0760d018e53f56a187475fd574dbd330f450e90acb2036de5b6642234bfed`  
		Last Modified: Tue, 25 Feb 2025 02:35:50 GMT  
		Size: 4.9 MB (4917590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20fe3101cb1cf242f5d84e2ba03b4ea9787f4eb4f713591e294a36b014a67beb`  
		Last Modified: Tue, 25 Feb 2025 02:35:49 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1fb052d7151718bae852dbad3f50f115bf5e4f2fb018030ba9108c5966fd7247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.8 MB (260762597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:472a1974848cddead05fc7cb42d8510e5583d95748dbeb8eac207af95fed9fbd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d3d2b1c1dfa2977b74e155013c02da80d2fb8bfea30462dc1a42ab04348739`  
		Last Modified: Wed, 05 Feb 2025 00:01:01 GMT  
		Size: 163.3 MB (163341435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a164074736d81268f8e5e171b395f6f8b70f0baa13129dc5d8a819b623abd43`  
		Last Modified: Thu, 20 Feb 2025 04:01:33 GMT  
		Size: 69.4 MB (69379239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff9ac6c61ff9930b0faf771fc7991906feaaf16faa81c2898cb9510210fba67`  
		Last Modified: Thu, 20 Feb 2025 04:01:30 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db928b52e49e2256f7a7cc26b9557ad86a5446d050f6dc972a4eb4a9584d593a`  
		Last Modified: Thu, 20 Feb 2025 04:01:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3579da6bd4e1d60a257e8a3f2cb4010de665e93934223528d2f26984f927fc66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4938708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9da2332ced035ea2ebbcb70b2e9e04c8ac7dc25a2659b99c5e39dc23728253e5`

```dockerfile
```

-	Layers:
	-	`sha256:cb051926f5c3559ab85998928ec67ccb0f4329ca906210d067cdf591cbaa7c03`  
		Last Modified: Thu, 20 Feb 2025 04:01:30 GMT  
		Size: 4.9 MB (4922712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4305ded861fa7ad4823eab14cfd8c39b0a0d535b537142b245c9800f0de28ff`  
		Last Modified: Thu, 20 Feb 2025 04:01:30 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
