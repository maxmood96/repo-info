## `clojure:temurin-24-tools-deps-1.12.2.1565-trixie`

```console
$ docker pull clojure@sha256:d8c998611214a96e8a01408a259fbf7d4b452486f076a431f99df770ad7a63c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-1.12.2.1565-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:91e816646a2f71eb10cb2f2f78fb70453fbeb630d30db054728a91ae9a878d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224787358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7059b67699c2e6b0d9b4683e84b4ac44357951a4767c63e5db611cf813b910b1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:80b7316254b3093eb3c7ac44bb6c34bde013f27947c1ed8d8afe456b957ebfdb`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 49.3 MB (49278280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0884f5f9a14686d41242b06d9b572a502db9a1e13703a15e16c68bb54cb018bf`  
		Last Modified: Tue, 26 Aug 2025 17:27:48 GMT  
		Size: 90.0 MB (89975190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2f85f490c90979c69efd8d470b1f502c44384b8bdd5cb372641eb2ef5a8481`  
		Last Modified: Tue, 26 Aug 2025 17:27:48 GMT  
		Size: 85.5 MB (85532844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7b54e014dfee69fdcefdfc76187d90a8d20dd8a91899446a2023ee0c8a241d`  
		Last Modified: Tue, 26 Aug 2025 17:36:50 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8dfe227732b1ebf2ed90e57e8ed8b727bad6a6b6f01ce22169d42b8a775413e`  
		Last Modified: Tue, 26 Aug 2025 17:36:54 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1565-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:58134c6f2539e29b3d7afda83a5e30a1851f5177e0685ea864a78f67b385cd7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7428659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea2ec0eddbd34cac2596cea198d3eab22ea937a331005fdca8b0d6e7a6367d90`

```dockerfile
```

-	Layers:
	-	`sha256:b3b1eb61223190f2402074501e20137978f1bb4759c5256ba64a667dc1caa421`  
		Last Modified: Tue, 26 Aug 2025 18:42:59 GMT  
		Size: 7.4 MB (7412869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7dd997a2e9c43c1ef06fbe43ef6b39ae5be970c27df5597f21ac091bdd4acd9`  
		Last Modified: Tue, 26 Aug 2025 18:42:59 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.2.1565-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3f690acb4fc41380bde28f39606e5599304229108161238a4c0ca6ae6359d7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224091832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b602c8b10870689ec8bc0857c402a0d6b41ff7cd6ed166e03cf417a9966857`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d1e40442030765a3ac5d135c39154d052eba20953ea0e5d35a066f7722cdd93d`  
		Last Modified: Tue, 12 Aug 2025 22:12:36 GMT  
		Size: 49.6 MB (49641603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3eb89d12affa8d8ae917d4a7451665386ed8fa42334a8c26fd85c84363bf134`  
		Last Modified: Mon, 18 Aug 2025 17:24:18 GMT  
		Size: 89.1 MB (89092502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239940211b6e0a61f3d1ba2160aa0844f82945c8e74687fa976a15d9289adbb9`  
		Last Modified: Tue, 26 Aug 2025 17:58:28 GMT  
		Size: 85.4 MB (85356681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fc8c06b775a79516b7b549b1fda72712625ad83aa974aac4f916698480763d`  
		Last Modified: Tue, 26 Aug 2025 17:58:11 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb583f445e720acf6dfd30df140db69378b93c8d28705bc8b4ec0912edf44c7`  
		Last Modified: Tue, 26 Aug 2025 17:58:10 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1565-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c0f2fa1048ca886b6381ee033a730eb1b399e81ae157759353221d61a9c9a9c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5112b232795a42dbd94cdca1433b426df57aed5b2f0f6e9b646cd8c88b25ad7d`

```dockerfile
```

-	Layers:
	-	`sha256:e8d5c5c247130d95f4c7636bd9a7abcf3e7717c864389739ca4c2a8f7e107f14`  
		Last Modified: Tue, 26 Aug 2025 18:43:06 GMT  
		Size: 7.4 MB (7419896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1008312253f71136f85b59ab8bec6f771e4a939525fc50324558750035ed1ff5`  
		Last Modified: Tue, 26 Aug 2025 18:43:07 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json
