## `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm-slim`

```console
$ docker pull clojure@sha256:ec35d22f87c5feb7bc5dd0a4ad8db15bcdc1b4faf66773264a1d4466cf50d3b3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5c58411be3349ad9e8f13d7ee527bfa255b52620a6bfa975591842eed132f0e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242300660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c6d9d2d6ff1c6fa23c986fa088a02bec80dd1b12c8d24a402bdda4d8488cd1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec5fd05d73d6d87e118ad528a4ca3ec6b5a157a74be0954bb9e4e0dc124f6e5`  
		Last Modified: Mon, 17 Mar 2025 23:21:04 GMT  
		Size: 144.6 MB (144566550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b5db7d0b54fefe261b456554a93ae877e0f751a0f2dd8c4858a5edac28b4cb`  
		Last Modified: Mon, 17 Mar 2025 23:21:03 GMT  
		Size: 69.5 MB (69528207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790d468165fb65efddf3f8be4440af1677252de7252030b9a65720e0588d7039`  
		Last Modified: Mon, 17 Mar 2025 23:21:02 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbcca446234764866db96cf59d1256048d799aaa7aa48fa8360425ecee5282f`  
		Last Modified: Mon, 17 Mar 2025 23:21:02 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:eae647e3e4b3bc90b612227cfa562251d080f4e9c33aea7ffd7d9d7771b2f43d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4928476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8335652d7c59ddf4cb9b849d78abee704e9ce8a7137117a7f4bde8b34ccf3389`

```dockerfile
```

-	Layers:
	-	`sha256:ce051c2ddfffd7019ca96711ddb0eb100c4350f351c778ebcebbbb1bb34d5846`  
		Last Modified: Mon, 17 Mar 2025 23:21:02 GMT  
		Size: 4.9 MB (4912597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13ebadbacd09b1f45e3daa780628d1c1d0156b407aab58074b072862d756e1e1`  
		Last Modified: Mon, 17 Mar 2025 23:21:02 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:71f92550181745b9e8e4aa1141a942ace64a98e7b36699360e913d8851769026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240877766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e204026261f801ce6a85d003d0d4211d6baa05e9e1f736a692dd85e222b429d7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11dfabd29c0f6eabe9090686cc1ad0a4bf8f02c0ce0ebacc1f8f57362aa176cc`  
		Last Modified: Tue, 18 Mar 2025 00:06:31 GMT  
		Size: 143.5 MB (143454716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e97676a0436dc28f0aead91cc45ac6e03ef1dd91c1a8101fee1b2073eeb5e2`  
		Last Modified: Tue, 18 Mar 2025 09:17:59 GMT  
		Size: 69.4 MB (69377974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ec8d7bb8ca33fca386ef2cb43798eabc1bbb4524fccd0aaf4d15624da63b6d`  
		Last Modified: Tue, 18 Mar 2025 09:17:57 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972147c34943f487a71013fbb21960855a55500fec7fda8633ae1ed09981a205`  
		Last Modified: Tue, 18 Mar 2025 09:17:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:33b5b9e4272c28bb794b2e5ad7a62167268f7eef82e3699a88bf32a1e0d56155
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4934355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b01765f412539cc9e936b575abce1becaee394605ebdb5b3dfaba4db09f00f`

```dockerfile
```

-	Layers:
	-	`sha256:ff0a59c6c8ef67713b3f87611e985426a3f608191d9dbd5e3844ebcbe5776e69`  
		Last Modified: Tue, 18 Mar 2025 09:17:57 GMT  
		Size: 4.9 MB (4918358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09eb347e928ee8e842c11642e55f26cfaa99dd53df7ac2115db4728f8ab59006`  
		Last Modified: Tue, 18 Mar 2025 09:17:57 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
