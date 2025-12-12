## `clojure:temurin-21-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:8b72c4e17094de2fa6e7120acc5b3c0f55dc41eaf26c6c8c311371cb32cf3a17
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:fecf96dd7dd3e60c1f3c699ae59c0d6f9fe00375ae9f4085c605edd8b5ce1b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 MB (281140221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37ab1562b386b3bb0bae5b5496f6a5c36fd4d0f35e47d608c51a969d8aa816c8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Thu, 11 Dec 2025 22:39:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:39:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:39:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:39:44 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:39:45 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:39:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:39:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:39:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:39:58 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:39:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:437b5b60e3a4b64e2c621589a67483eeef6d4b3fc4926655006ef41bd44f71dd`  
		Last Modified: Mon, 08 Dec 2025 22:16:49 GMT  
		Size: 53.8 MB (53756413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb6a580a0a1c46f4b94122fd9795fcb39c5c4368818f7e6d42440aa7f71fa8b`  
		Last Modified: Fri, 12 Dec 2025 18:27:13 GMT  
		Size: 157.8 MB (157825967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a723581cb531f81516921ebc3a1b1739bf0fd2e0919e47067f9a6a598332b2`  
		Last Modified: Thu, 11 Dec 2025 22:40:33 GMT  
		Size: 69.6 MB (69556801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f998f43c12977423799c05b6c310d818f01bcb0df2c24a77019119d17a5917b6`  
		Last Modified: Thu, 11 Dec 2025 22:40:25 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3c5ad52343cf12b8b27a0948740431d6bc17b7978f7f0c5fa9b293a68134ef`  
		Last Modified: Thu, 11 Dec 2025 22:40:25 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a952cfedcd94d40b35227ba7730f3a07951c97cd3c0687c852b757aa97abd7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7414549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:622fc5aab7710267bce9a71ed4dd2782efbdc7bb5f282b67e03614ab71ac4695`

```dockerfile
```

-	Layers:
	-	`sha256:7f673b810049038350ab3ed5fdfd04604e3ddc6e8d85bbf82f668a79cca4faa5`  
		Last Modified: Fri, 12 Dec 2025 01:41:14 GMT  
		Size: 7.4 MB (7398771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcff07b83d4b4347f81330c6f42cb914c30360724845841dac9d18d3a515916a`  
		Last Modified: Fri, 12 Dec 2025 01:41:15 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b34108e8e30d3a815901b667e735d7b1c7e2a40c4e27ee7d391908845c4d4768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278053439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b22158e42f06ac095b45ad8d3afbd93dd265f30ed53e91cab4f92131ac9c02e6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Thu, 11 Dec 2025 22:38:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:38:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:38:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:38:21 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:38:21 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:38:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:38:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:38:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:38:36 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:38:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:24bca79f74a34f86894c8fcdc6ce8d7dc3c11dd0c76b7e9fa80c7c64df65d166`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 52.3 MB (52257713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8930deabb3a3f2a70880cc847dd7dc1ba9408bcf8f7c85df9ebdd7a9a5746d1`  
		Last Modified: Thu, 11 Dec 2025 22:39:15 GMT  
		Size: 156.1 MB (156107638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1171b4aa7bdd8cfc09cacd948f80eb22545c447111ab28d82a8ad6a294fed3`  
		Last Modified: Thu, 11 Dec 2025 22:39:14 GMT  
		Size: 69.7 MB (69687047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c9bd8e51006e208fc55a1715dc0df81657f25288f1116027042537b52fbe243`  
		Last Modified: Thu, 11 Dec 2025 22:39:04 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1edb165698fca5e2b9ec08b838186e0cd115204b93c4bcb3f0f8621a3bd04af4`  
		Last Modified: Thu, 11 Dec 2025 22:39:04 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e7014698e2bfde5f07987f801f74babf5a321ccf84538c3289dc435a34ed4111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7419766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f4d3b9c62612ddbca14a6ecb6eed0ad380a50a753e57df65f4b30ea29ca7dc5`

```dockerfile
```

-	Layers:
	-	`sha256:358b89ea0ca0fe8732948bcfd1c0e301e054a9872dccf8661704b42cc27a9bde`  
		Last Modified: Fri, 12 Dec 2025 01:41:21 GMT  
		Size: 7.4 MB (7403870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7519c699deb86eef42e89c0ee10897bc1ca1171afcc86297a548f615b6be063d`  
		Last Modified: Fri, 12 Dec 2025 01:41:22 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json
