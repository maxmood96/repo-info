## `clojure:temurin-22-bullseye-slim`

```console
$ docker pull clojure@sha256:d2865663fdb984850a32aab8a2a43b91cccd121748d400fdfcc0e8cf13a8589d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f2c7f26de195b4d6bc189e3f9ab2e1a15c2abef82f2e9e1432f1ace7a9c556af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246569913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59b38f5557133ec9cf9a09715f8005625e45121241a231b0ea1f64f9e260510e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ee27ca849a33dfc39ab3ac61df29262d075b0223d0737dbad425645fd2d5b4`  
		Last Modified: Wed, 05 Jun 2024 06:12:32 GMT  
		Size: 156.7 MB (156715537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf21efa5e52176886c77bf76b6a870afa27c8be05db27b70e8f8493b4225042b`  
		Last Modified: Wed, 05 Jun 2024 06:12:29 GMT  
		Size: 58.4 MB (58419400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7836a79ba7831be03f08c62cbfe4d459c8708c146e25596bc679ac065eaaeb`  
		Last Modified: Wed, 05 Jun 2024 06:12:28 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9a10afaa7289b5e95d76cfd2e91feedeba13ea5d4e2f1a1a18f801c2e249e1`  
		Last Modified: Wed, 05 Jun 2024 06:12:28 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:98a4b8d66a1ccc18f4704b094b27bd1873b20f9f5b669c4ba630e76f5334c26c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4924690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc201b699feb4a4a41698d74233a084e1cbd1a53d8711ed182805e881a359eb`

```dockerfile
```

-	Layers:
	-	`sha256:7d56c613b4a48a7e0813b8e4b7cf22d978cf611ca3b89e775a37ef7c016cd7e9`  
		Last Modified: Wed, 05 Jun 2024 06:12:28 GMT  
		Size: 4.9 MB (4909227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2adfdf93488205bb1f01a42fde51793c6256aa54a9b56054e8abee48c5fe7dc`  
		Last Modified: Wed, 05 Jun 2024 06:12:28 GMT  
		Size: 15.5 KB (15463 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:05dc80185829f0d2a992f9dfa11dd5ae7f392a2c78dff088dff7ced2d555db1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243365849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7ac391ec7843b03445baeef0506f1d0dacd695388454d51be50393f6bcb5c99`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acb0b1364c06c45eb5a4ccf0acaa92791b919919ebe7e8d6fe6830852e64dcb`  
		Last Modified: Wed, 05 Jun 2024 14:22:17 GMT  
		Size: 154.7 MB (154737997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc0b1451b6d3a4f35288fc2d1c76c424a4f56aea527caecdf8c907f79af4a3f`  
		Last Modified: Wed, 05 Jun 2024 14:27:05 GMT  
		Size: 58.5 MB (58539896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac8359768a3573d8c2ddbbd9747c350b465995e390857fcd53566dacda16b10`  
		Last Modified: Wed, 05 Jun 2024 14:27:03 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ad3c7faa690e520272266afa1d5933f1ab5ee62de8feab6ceca5996d0e418d`  
		Last Modified: Wed, 05 Jun 2024 14:27:04 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:315458bab3f1e010d4c360c55771bca4c52f378b23a4088f040d622b13ddc56f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4931587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c6fe9c00480eb8672b981c5082885f496d71c6e3e8c02a566ea0f6b3c057c6`

```dockerfile
```

-	Layers:
	-	`sha256:796e56c872b23e58285043d1f5a2aa3f0a7e19ed01e0f26d3d13bfc80f7bbb03`  
		Last Modified: Wed, 05 Jun 2024 14:27:04 GMT  
		Size: 4.9 MB (4915583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfddd7f61bed89878c41fcff87367e0736b5e43ec7cd09bc4513f154ddd839be`  
		Last Modified: Wed, 05 Jun 2024 14:27:04 GMT  
		Size: 16.0 KB (16004 bytes)  
		MIME: application/vnd.in-toto+json
