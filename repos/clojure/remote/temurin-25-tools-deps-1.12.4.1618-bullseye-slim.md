## `clojure:temurin-25-tools-deps-1.12.4.1618-bullseye-slim`

```console
$ docker pull clojure@sha256:3255c484255fb4666350b0fd91ee1726174d73c7facc9a84114e2b0edc7e68ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-1.12.4.1618-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:026e81f4575416fab5212412fd373b78fd15fe5c34eefe7617712e1ae143b771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.0 MB (182019897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a2b56c0be93c27a5f32b5553d71dfcf401046456bcbd5619c7f79adcbd60908`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Fri, 08 May 2026 00:28:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:28:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:28:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:28:37 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:28:37 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:28:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:28:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:28:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:28:50 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:28:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7263c37a27b96bd5e0c0de77a44122fc986156c49e3c82b0ba12448611753e10`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 30.3 MB (30257934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3020ea788122d53a1bad9f4f7c148b5ab02a2c73a2df700d2336f4a1bd7450ae`  
		Last Modified: Fri, 08 May 2026 00:29:12 GMT  
		Size: 92.6 MB (92574587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13641df6cc9f0d2267d1efd32f7a95cf9c9f4fdb6357d9a626c8b7f8950ea93b`  
		Last Modified: Fri, 08 May 2026 00:29:11 GMT  
		Size: 59.2 MB (59186335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569cc7154e064613c017ac7386263f4d5a8dc3bd23d5307f8dd9ec3f24d723a2`  
		Last Modified: Fri, 08 May 2026 00:29:08 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a6f1db76b142cb1e1c9cc5dd74d0aa4e8a0ad56bb4c292fb2c8312a1f43ab8`  
		Last Modified: Fri, 08 May 2026 00:29:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a7c7c64474403861db3f15c7f9fc0de4209910d312dcf1c5db8bcefa44ec33ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5305449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b46d4d9d66866dc38a9e7507f43eff66952f5dead350e5af083c31b610c8e468`

```dockerfile
```

-	Layers:
	-	`sha256:9c042bff4946d81c5c3132116e4f542f20bbbe51400c1ccaacc499807634271c`  
		Last Modified: Fri, 08 May 2026 00:29:08 GMT  
		Size: 5.3 MB (5288770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8ca6b02104ff1436daddfa106276ad83ebb16b9a1a56597f93d372ae4b838c8`  
		Last Modified: Fri, 08 May 2026 00:29:08 GMT  
		Size: 16.7 KB (16679 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:54b83ab1c0d7bff4522d81613ab476641ff4e3e0a5ff5257993514fefb6757a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179616941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff9073945ebb382d72ee76104f89e817d8a79286cb5389a2989aae187cff744b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Fri, 08 May 2026 00:27:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:27:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:27:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:27:46 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:27:46 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:27:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:27:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:27:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:27:59 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:27:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ab304f220d8a8ccbd47569f385750aa3f87cafd221f915b82f8e566f1abe130b`  
		Last Modified: Wed, 22 Apr 2026 00:16:28 GMT  
		Size: 28.7 MB (28742512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2798e573252c7ddc8331f3ebfe4553695099baf57dc4d88dd4cd4918155942ad`  
		Last Modified: Fri, 08 May 2026 00:28:29 GMT  
		Size: 91.5 MB (91542278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c409f586bf1ceb5bef31040c3d81cf27cb2be3c80bdec82e63baee4baa78bf`  
		Last Modified: Fri, 08 May 2026 00:28:20 GMT  
		Size: 59.3 MB (59331106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96c120021c95eeb24c6a90e7a7aedafd0b691b8f6036bc27eef6811e3595d4d`  
		Last Modified: Fri, 08 May 2026 00:28:15 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba29dadd62da7afe9120e72d35d4c095da2814505dae45f81d7c2a1bdf2b6909`  
		Last Modified: Fri, 08 May 2026 00:28:16 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2781fc0c960c5d2cd152c3fbd0bacd03640a458db6226fde5353ca1fd1b82d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5311344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59628d864da3e23c6dde9c59d96a9875917c0b7d19f6ded6bdcbee8427a7a7fb`

```dockerfile
```

-	Layers:
	-	`sha256:50e1d6cbbf672b60d68fff9c131898acd843b6f133b5433fd1922e6a13319f38`  
		Last Modified: Fri, 08 May 2026 00:28:16 GMT  
		Size: 5.3 MB (5294523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92df48e4f75d5656fd857b8b8c59628df11796fa2195ff1e539d8ba312ac41b9`  
		Last Modified: Fri, 08 May 2026 00:28:15 GMT  
		Size: 16.8 KB (16821 bytes)  
		MIME: application/vnd.in-toto+json
