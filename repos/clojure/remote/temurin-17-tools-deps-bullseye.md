## `clojure:temurin-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:a58afbcd9958f8bfc0571680235db15b322cabf68409e25723d48b41cb4e0951
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:2014218731ee0b9a80148e0b6a9dbd74a0f651230dd9bca4be7d73d23d38e622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.2 MB (268167055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081ee1633317ff0361e6f61f9eff5504db5c8276899d8747087828d9e8b2f306`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Sat, 08 Nov 2025 18:43:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:43:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:43:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:43:07 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:43:07 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:43:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:43:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:43:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:43:20 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:43:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0436715264d0b8e21fbe44e8250538bcc9b0ad17d15d959bf5b2cf5bb7979672`  
		Last Modified: Sun, 09 Nov 2025 03:51:04 GMT  
		Size: 144.8 MB (144848051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9282d35086e1b2c79115df8163128792d1e82a1190fad07e2d2738080f85c5b6`  
		Last Modified: Sat, 08 Nov 2025 18:44:00 GMT  
		Size: 69.6 MB (69561265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3377a7dfb0589ed5f7326500334bf5bb3cebe8aa772abb64faf083f1e99bcebe`  
		Last Modified: Sat, 08 Nov 2025 18:43:49 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61753472561913e686c702efabbc26c0678c1705fe2c5825bd57f82beaaa895`  
		Last Modified: Sat, 08 Nov 2025 18:43:49 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1752c806693d97ff479bca46b1ed46e6cf48ff986423f68b55172b28d9337dfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7411447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77b19c107585ddc1a68615b301605ce377c1e9ecbe38ca61ae7d2abc7615c9aa`

```dockerfile
```

-	Layers:
	-	`sha256:92f2784d1b42bdfa9907a36699e9360b51c56dbb46ec34641a76194ff5a7da44`  
		Last Modified: Sat, 08 Nov 2025 22:41:20 GMT  
		Size: 7.4 MB (7395669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed948825e41f7d21cd6618430ded89043dd31f30ea2ad902dfb46c827f7e872b`  
		Last Modified: Sat, 08 Nov 2025 22:41:21 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b3d35ad5f87922ae5702a699ba7bf4f43ef7aa4ed10b86edb6b09cf17fede7e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.6 MB (265627337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c5a9724ba9b0131d4dcde6be51ea2002e49f61a25c4893ba73b4bf1dc2b10f5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Sat, 08 Nov 2025 18:42:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:42:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:42:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:42:38 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:42:38 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:42:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:42:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:42:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:42:52 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:42:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092db33a5cfd9ad23fb2a0d3d17f78d2c08d4b8b44eb9c61af94f12a8d608880`  
		Last Modified: Mon, 10 Nov 2025 05:12:56 GMT  
		Size: 143.7 MB (143679948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847a2b516632b4f667d875f2228ddd67f996f7e6cb632a6fa9c37858fbf6b9c2`  
		Last Modified: Sat, 08 Nov 2025 18:43:53 GMT  
		Size: 69.7 MB (69688379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec76ee14bc7c1010fc62d9c989996ae0b93028559f839195d0bf7319da76cd7b`  
		Last Modified: Sat, 08 Nov 2025 18:43:50 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834bba3af68bdcb80db9a0cbba43756b8ebf9514b426f85968b82421adcb240f`  
		Last Modified: Sat, 08 Nov 2025 18:43:50 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:0611a1aa0725bca2c401bf330879526fd1416fe98b464b381c88bd9a2c336f45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7416664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf6d0c1282159543ecf54dca692428b04b2d1b6798644dce978d628a2ea6a5a`

```dockerfile
```

-	Layers:
	-	`sha256:35c2772662246c979c943e8a03c8f9624bc2bc3a8181d0e76167d575287b7ac5`  
		Last Modified: Sat, 08 Nov 2025 22:41:29 GMT  
		Size: 7.4 MB (7400768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cea415cc8e9a7392645f737143b6f874b6daf1ae2891f53e998ca3e39a4d5b9`  
		Last Modified: Sat, 08 Nov 2025 22:41:30 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json
