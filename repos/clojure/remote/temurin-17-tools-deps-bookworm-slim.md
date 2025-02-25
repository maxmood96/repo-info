## `clojure:temurin-17-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:4f4438091e9bc5b09663021b63d0fb1d8a4f3d4266f43a6125b28e74f0994406
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2df42ded5be2abfe34d548effcaa63603e1fdae8a234e1d033491b801ba0e8a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242317297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9ac90879e65b002f94e2527853067325c589e4a64eb9a55df36036f7b7ca54`
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
	-	`sha256:5cf03e0c3a6ea52e34458201dd1df27704b40eb46ad9cda6d082511cab298db7`  
		Last Modified: Tue, 25 Feb 2025 02:32:50 GMT  
		Size: 144.6 MB (144566549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb5a3b2112dbc54431f248175e553ad90397c078a5092c5b37887f0bcf47a3f`  
		Last Modified: Tue, 25 Feb 2025 02:32:49 GMT  
		Size: 69.5 MB (69530406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746e55a5ce7c9708040f2f58115927ce6fcb42cacd0aeb4dc7178b8c560a054d`  
		Last Modified: Tue, 25 Feb 2025 02:32:48 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8aced933c9daf6a4a5dfecf1878aed6d464b4a67c222d42d92aca85234a0ae3`  
		Last Modified: Tue, 25 Feb 2025 02:32:48 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:424c368e9718220bce3f5106979a96024a2858d953a624654674723691a19342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4928464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a12a3e91381aea86036d77d8209ca5a81d20cbb4d3be243efb0d000b6eb0e9`

```dockerfile
```

-	Layers:
	-	`sha256:75b98daa5a54ed26720778d3faed0ffc2a9a55a1c6f0075bbde4940311ff04d5`  
		Last Modified: Tue, 25 Feb 2025 02:32:48 GMT  
		Size: 4.9 MB (4912585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53f333401330b68bedaa3d2070bd294acb6f34f9833fd8a94d2b723aa931450a`  
		Last Modified: Tue, 25 Feb 2025 02:32:48 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:357200bf4d5f1bee71542e0a717ea097438fb33544d36f6cecd45b528c8cd1dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240875823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f98419e8bf7d683de1af94334011644aa883f345f5a6d4102230d287fea2a2c`
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
	-	`sha256:f0ae012ff89092306c93163c5501638b4e1ea553e25181d4997dd7d40d4e9812`  
		Last Modified: Tue, 04 Feb 2025 23:43:37 GMT  
		Size: 143.5 MB (143454713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e0b1c679d5832c6d1e337091f8afa07a4bf9c8c671ef00239c9b57df443d4c0`  
		Last Modified: Thu, 20 Feb 2025 03:52:20 GMT  
		Size: 69.4 MB (69379190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8432733fee2264253931c5fb978fc791428416c34bc6876d8ccacc5a21aba38`  
		Last Modified: Thu, 20 Feb 2025 03:52:18 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2e45b26206972a3fb49a62187b9b595ba3fa46498a18a595ef5731651e30b6`  
		Last Modified: Thu, 20 Feb 2025 03:52:18 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8eecbdd1cd4cb2d9da3b503d7756abe07cee9762467f6c8ad203a4df6aef7592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4934325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d304cdb797c339b215f32b78be591a044b7baad2f6fb88a87a79f07dc1daaea`

```dockerfile
```

-	Layers:
	-	`sha256:c13f78f6ac90e898bc4f6209776aee2b1830727e1bc4d4b01dee8ccc6600c886`  
		Last Modified: Thu, 20 Feb 2025 03:52:18 GMT  
		Size: 4.9 MB (4918328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef0a944938ee701ec25f412a5a6e1a085e66ef587575cb124850ccbf11f7b558`  
		Last Modified: Thu, 20 Feb 2025 03:52:17 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
