## `clojure:temurin-22-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:a83372e0614112207e00a7dd99cf2b63f1a98093363f7805ac6b4957332b0d1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:1a3cce4fe80eb6d269983c2986d2cc1cba06f11efdf51291df4c01b3b674944c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.9 MB (280899161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d95a814eab8c8ee829f80d276f1cab8a0c37cb6c40100f30fe30c564de610632`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:56 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
# Wed, 04 Sep 2024 22:30:57 GMT
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3649be72b9e35e408bcad18dabe91b305a102f549385e0eb5453e821590952b8`  
		Last Modified: Tue, 17 Sep 2024 01:59:20 GMT  
		Size: 156.5 MB (156481645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c129f19f2d6b4289f09199718defbc65d7027654ed0feafc18906256bb493e04`  
		Last Modified: Tue, 17 Sep 2024 01:59:18 GMT  
		Size: 69.3 MB (69335146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22322c018bd8ed83fd774d8e19b24dde4dcf6a18c3912e125a671a0f3a1c1e8b`  
		Last Modified: Tue, 17 Sep 2024 01:59:17 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2af11449a7ea5d7187b7bc6a2e80fd2e0844708dd00cfd1a8684b2bf39bfce`  
		Last Modified: Tue, 17 Sep 2024 01:59:17 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:acd818dd836cb063e73ec85cd678171d12c9c7d122b3d7b92758cababc184244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7055778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1754bd144a5f9cb60312587c69a966450d0201f5bc3c7f85a908a1ba23c86758`

```dockerfile
```

-	Layers:
	-	`sha256:a859a415080fec2ae188dae462b20c288168851e1ea8dbf563236a855237f800`  
		Last Modified: Tue, 17 Sep 2024 01:59:17 GMT  
		Size: 7.0 MB (7040338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e583c21a4c84345d65ade7f55130cceb6036bcbb152a100bc2a78df1b910cf38`  
		Last Modified: Tue, 17 Sep 2024 01:59:17 GMT  
		Size: 15.4 KB (15440 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f0ab854e9afa26cb51358a7516dada14ad84259b5eb4bdfffae379d5f87245d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277703038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2efa0a6527ff3ce5e079c88e6e57d3ecd1d6ddb3c3b3671bd595683fabdc052`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:59 GMT
ADD file:aad8b86b3a958bc07504985acedcc819faa4f1ed12ca8b46d8d94c4d564cbdfa in / 
# Wed, 04 Sep 2024 21:40:00 GMT
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d82c4492ee91810a42e0c53e955a661e9a092364bc474c9db559ea5b24b7047f`  
		Last Modified: Wed, 04 Sep 2024 21:42:52 GMT  
		Size: 53.7 MB (53731619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b373f6ff7665f36b6975c9640d57de81ac735f9d9d471698a770405ed8e4253f`  
		Last Modified: Tue, 17 Sep 2024 04:53:53 GMT  
		Size: 154.5 MB (154503778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa838df5b1261a6b1f7fd7e40c17a84fc51b101ec85b1e27a8d084663ec36e2`  
		Last Modified: Tue, 17 Sep 2024 04:59:17 GMT  
		Size: 69.5 MB (69466601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f9fa047036c168cd6c658aeded610b206b08640900a06e8d9a0e686de97285`  
		Last Modified: Tue, 17 Sep 2024 04:59:15 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913f18db21f4ce84011632c32f258fa21ed47a18b9c2978b5b87b9ab9baf899d`  
		Last Modified: Tue, 17 Sep 2024 04:59:15 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:6c691ce7bdce5a42264fd2cd8d35478b5a0a7b8d909d74f36d5a13281a99e82c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7062036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:274569044f5db49c89c92ce004fe03a5619fb904df0aeac42b65cb485a7da66b`

```dockerfile
```

-	Layers:
	-	`sha256:2f7fd70c378f6068f12d6b1850d64e39dd21d83d475c90b00024479b536ed604`  
		Last Modified: Tue, 17 Sep 2024 04:59:16 GMT  
		Size: 7.0 MB (7046060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a66200118646622e2245e1b735b2d8170b5b9947e85f89ef201ca51a07407294`  
		Last Modified: Tue, 17 Sep 2024 04:59:15 GMT  
		Size: 16.0 KB (15976 bytes)  
		MIME: application/vnd.in-toto+json
