## `clojure:temurin-21-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:cb38de9bc45ce894d7b594d0b0da7b3724ac0135b8b6549a60e31217910156a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9790250368d6ca8495a154d8654a3ed0c5d46f2a6aac29a9c444ceec20635d85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250210924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ecd5d357b6b80af229c4e24eda07dcd8723527bae5124f05b952cbf9542bfa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205b70c2d552e52e8052a8b6b4f823f79abccc83f70c7f8f52fa520107b5ae1b`  
		Last Modified: Thu, 24 Oct 2024 02:00:43 GMT  
		Size: 157.6 MB (157568700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48e8af76912b10c42b2387d9ff42d6241a19731f7327e4583c648464be32548`  
		Last Modified: Thu, 24 Oct 2024 02:00:42 GMT  
		Size: 61.2 MB (61212384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b655da7b61301710c25946f39f746bd081db21c18cde88dceb6992ca42ed6be`  
		Last Modified: Thu, 24 Oct 2024 02:00:41 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb3466fff0bf489f58e361f70f61c8271c070aa87a8e1f3ab698ccf392368f1`  
		Last Modified: Thu, 24 Oct 2024 02:00:41 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7e3951b87cdc7c40aa7c300aee22ec2e93cc7a5627403fd0908f6cf89162dc59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5145534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a187e21ec5db8769eb2aec5e47c008b60281efa74f23037b7931eba56c987792`

```dockerfile
```

-	Layers:
	-	`sha256:86663655c925bed38c1329b8f23245666b2745711828ef49f7ef6ae099b928bd`  
		Last Modified: Thu, 24 Oct 2024 02:00:41 GMT  
		Size: 5.1 MB (5129119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13ed34e9b8b553d3fcd88d576999183451f487202fbbc8c1267022ddbd7ce277`  
		Last Modified: Thu, 24 Oct 2024 02:00:41 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bf8d56c8fb4f97c84317991d5972a89a2f969f3da8259246bb65960bd2217152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247166678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf5b31200ac081c4c1ef726b0aae4c9accfd5e35b5a22e92570d291c1bf657e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cdc35f8305a192807fb33aedd2b7a354b336ed58f1b2833dab6105e7715666`  
		Last Modified: Thu, 24 Oct 2024 09:27:50 GMT  
		Size: 155.8 MB (155793065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02cbae495c0ee313b3f322c3fc555c1b22996516df56037f6e38caca4b53fdfb`  
		Last Modified: Thu, 24 Oct 2024 09:33:17 GMT  
		Size: 61.3 MB (61296815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb7e69df2721f488eb4cb6836f73c33071b08c0195cffd4e92358e4a165f093`  
		Last Modified: Thu, 24 Oct 2024 09:33:15 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f856694939e4c6197cc0e02451217ed752f26cfc6108557a387a983fd4565ba`  
		Last Modified: Thu, 24 Oct 2024 09:33:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3d3d8919ef4ac0a31ebc7503582373766047b870bc959e747a2ed1c378677a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5151431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5451436cd9a0afb94a70ee2fd0d73cf5ab656199ad6d706c4c0643d3516340d3`

```dockerfile
```

-	Layers:
	-	`sha256:4acbff6a2b76d696c17182604749d33f621c70f4c323437db47fe2a6d72be69d`  
		Last Modified: Thu, 24 Oct 2024 09:33:16 GMT  
		Size: 5.1 MB (5134880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dec1541f806c5d10e69b5d8db77cd2afaf34ec14c4f2c1f00b7ae42b5647cb8`  
		Last Modified: Thu, 24 Oct 2024 09:33:15 GMT  
		Size: 16.6 KB (16551 bytes)  
		MIME: application/vnd.in-toto+json
