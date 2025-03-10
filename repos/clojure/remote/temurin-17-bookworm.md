## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:83dd86b9bdcf6b9eaf22c107c8b3e131c8c74f33223c3f4300559d21432fefcd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:0cfc14e5f734d4deae5a2d196bbfbd1707a058a3e97ec4f7e331602e8f90e5ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.0 MB (274037020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f193ef590b925515b55db0b33c916890aff9938d60ff038fba24b4ea45351cd3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a188d02295656d11eba221010636b3a2a18040f12e95838b26baaa70deb371b`  
		Last Modified: Mon, 10 Mar 2025 17:40:31 GMT  
		Size: 144.6 MB (144566594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd945ba5b0a3136862b31512965aae27348a216dd98a4de4cf2ec6177dcf2316`  
		Last Modified: Mon, 10 Mar 2025 17:40:30 GMT  
		Size: 81.0 MB (80993283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d5cc0f5d17d9780286fb5a937b6e6ea40269059856fb2014595901d94e0c11`  
		Last Modified: Mon, 10 Mar 2025 17:40:27 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37cd341e575f1d8a28d0881f38a337ec54a7d6db71ff5413b24fba9727c9b09f`  
		Last Modified: Mon, 10 Mar 2025 17:40:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4d206d07643b030eba9f275b07c3ad81fa5ed1e8d48e7ddb15a34a372b7e2225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7186917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fddb6bff8137f44ad882d62fade5e03c95be9c55a7872b1149e3dcd30d6fce3`

```dockerfile
```

-	Layers:
	-	`sha256:2af50c215d1cac386c8fddd7a148b0893e41daeabb5691fed7325c400f5ed6e1`  
		Last Modified: Mon, 10 Mar 2025 17:40:28 GMT  
		Size: 7.2 MB (7171096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cb3f357e420d96b666fd4a950bdb164858a367e197ea917878eee1e08094a47`  
		Last Modified: Mon, 10 Mar 2025 17:40:27 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8595a4d018824048c788f96b6a96fd500db45a2f566f51c13b62786a6130ed1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272605901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb3fc38bd07fd5133c5c6fa5e5b7a8d04dd41fcc91b350963c41f28294446cf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0024ab4e8de7a50cf5cb5d9ffb53640a0acc93c9a541b18218c4fe612e383214`  
		Last Modified: Mon, 10 Mar 2025 17:59:00 GMT  
		Size: 143.5 MB (143454700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b4caf35d2529b3b2fdedb5d49d4627b638799a8838bc96159da0ec7b4ff541`  
		Last Modified: Mon, 10 Mar 2025 17:58:59 GMT  
		Size: 80.8 MB (80842145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c861f84e93e25f77e7db6269ea8e5c6453e7ebd1dbdd86346ea80c9741c8cbb`  
		Last Modified: Mon, 10 Mar 2025 17:58:56 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa6c126780f0dc69bf734f2eee00be7ef7e99cb1ade8b587494cd4f949aeb72`  
		Last Modified: Mon, 10 Mar 2025 17:58:56 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:bff6238c8ff6806ee91445a6a9db1fb02f5592621d158b482deb70adcb5bb007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7192798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047262deecb6e5d03390c1e3b108e222ebf55345d62247c4408f7e209b7eb485`

```dockerfile
```

-	Layers:
	-	`sha256:21ad53b3193476ee29ac6c06689007f96e7cd337d52aa065aa3c4b46475c10c4`  
		Last Modified: Mon, 10 Mar 2025 17:58:57 GMT  
		Size: 7.2 MB (7176859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98c3542791c605b0a4b94768e4a3700fa72ce84ee577d997700784e96d016409`  
		Last Modified: Mon, 10 Mar 2025 17:58:56 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
