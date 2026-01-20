## `clojure:temurin-21-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:f9a4cee606379275db34725a4f9cff1bdc49ad53c21390619405ae0c6abc09fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0456fd84d306f49faef3a07d7cbc979354e3f6c1668267f8617bb8719640ec58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247235315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af22604bff52436df6a3f348be169d487db92122f686af1d06cb5cb4afbc35b3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Fri, 16 Jan 2026 02:00:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:00:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:00:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:00:52 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 02:00:52 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:01:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 02:01:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 02:01:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:01:06 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:01:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bd1b97a95a10ded4767bfcdbb3d042b961d107d141121fdbb255239f0ca115f4`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 30.3 MB (30258497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b622e22ab3d91f9f6761af0427265365889610d5e01c25f62e106410c0860c2`  
		Last Modified: Fri, 16 Jan 2026 08:32:37 GMT  
		Size: 157.8 MB (157826001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d945782962f93ff61c16f3186586e9dfabf46399ac3944cf3dfa1769e48620`  
		Last Modified: Fri, 16 Jan 2026 02:01:26 GMT  
		Size: 59.1 MB (59149779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:921ea677f248157ab5c0f1a0a0840d9432c43aa799bdee082a1c2a86701edd1f`  
		Last Modified: Fri, 16 Jan 2026 02:01:34 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd542880d3f3d3ef67aaf821bd35577bc022322b533efa21c12158041783bb1`  
		Last Modified: Fri, 16 Jan 2026 02:01:24 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5a8ba3a48880c3b6530fd4d0fe67586fafc3bd36fe7040297b08701a13ad63bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5327007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d490d0d961a0e01c3ed701c4444cd42195b07f82455dec2f7b91da0d9e3b41f`

```dockerfile
```

-	Layers:
	-	`sha256:a28c50ac44ee2666529acb59bd969ddff5b96d2a176d439d1be87aea7abbd070`  
		Last Modified: Fri, 16 Jan 2026 02:01:25 GMT  
		Size: 5.3 MB (5311171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d5f631bad272dc8bd0e8b873d1487493873c651e8e42f4cb9aa6016d30e3120`  
		Last Modified: Fri, 16 Jan 2026 04:45:40 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:44e4a780b20a14f18cba913dc135e8a9ba4ec9a9058502522ab7b566665c32d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244140936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa08bc70a092e868304377f3417adf41e1c2bcd6ccdd6cfb5b6f29b1456f88ff`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Fri, 16 Jan 2026 02:05:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:05:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:05:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:05:48 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 02:05:48 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:06:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 02:06:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 02:06:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:06:02 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:06:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:59 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d389dbc97ee68e9c081ffc622e65f4e93ef19817f3cb94a267e26d8af8f766`  
		Last Modified: Fri, 16 Jan 2026 02:06:26 GMT  
		Size: 156.1 MB (156107636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e598703d814f63073308c7cf4f13c62ca097bee63869cb8f7d314c67d905bf8a`  
		Last Modified: Fri, 16 Jan 2026 02:06:36 GMT  
		Size: 59.3 MB (59283740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d9df3773a916fec9ad33592fd982942b79020e372a1961541b2bc8564372b7`  
		Last Modified: Fri, 16 Jan 2026 02:06:22 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a85692c5c38bf74f6a44c2f611e257b52005c6dddac6ee633e48c2ebb9fc46`  
		Last Modified: Fri, 16 Jan 2026 02:06:22 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:92559c34c6983f87201b833f36bcf382b2b2d31638041306794238ebc8e0b1d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5332857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b58f4d3a0412893008364e914c74f92c6cd640990b6b86f7e0efa8a46d2cfa8`

```dockerfile
```

-	Layers:
	-	`sha256:038a4a173de3f5e1fe83891887cd26958d92f41e41395378ced36d0160ef89b4`  
		Last Modified: Fri, 16 Jan 2026 04:45:46 GMT  
		Size: 5.3 MB (5316903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5908f0447b623e095cac936f2471a8d877dabcb5a1301908825349d76c2f6223`  
		Last Modified: Fri, 16 Jan 2026 04:45:55 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json
