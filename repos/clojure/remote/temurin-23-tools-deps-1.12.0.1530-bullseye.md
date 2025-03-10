## `clojure:temurin-23-tools-deps-1.12.0.1530-bullseye`

```console
$ docker pull clojure@sha256:9ee60475c073fefaa6c8862731f1ef1f13d635c696f287ffd962e2eea91a0fbf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-1.12.0.1530-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:6d041b3e5c1bdba01a7dd7f92854ba6c4f4c6a326de944aaea779413320b9c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288242144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3bd4cd50032a357020e77142c63c3064ac524b3ea210d4153f81726bb9c55b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
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
	-	`sha256:4ff5a3a54264ee833e4a09583363bbe779e881f15449fe4f4a6a662885dd37fb`  
		Last Modified: Tue, 25 Feb 2025 01:29:47 GMT  
		Size: 53.7 MB (53741401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5b5ac0155384a97f60455cbf44b86f5e5d239ad69e4d543c98077ca21cad7b`  
		Last Modified: Mon, 10 Mar 2025 17:40:17 GMT  
		Size: 165.3 MB (165316229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db2faa04e9cdc737ea2ca3401062cc6ef3352cc88f2b0156a481665e3e5e15a`  
		Last Modified: Mon, 10 Mar 2025 17:40:15 GMT  
		Size: 69.2 MB (69183472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f872fb082a4be5cfa1cc268e1f2001b4bf50bdeb1d3a3c5bb3c1b394323868b4`  
		Last Modified: Mon, 10 Mar 2025 17:40:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de0081bd79ebc2c33b3d0cf46959892596ead2cedbfbc580f7619d341318816`  
		Last Modified: Mon, 10 Mar 2025 17:40:14 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:76534183522960111233d9759bff9a600bb3080565ea840f73a2b2dc8793c798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7225379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1ae25d3e9ed5aad0745188ffb79e9c4e3f1fd0fd833ac631f21e71bcce4c089`

```dockerfile
```

-	Layers:
	-	`sha256:bac7ecc65ac398343d5392bbdc65f1ddeb847da054ea3f1f718c290e04de4986`  
		Last Modified: Mon, 10 Mar 2025 17:40:14 GMT  
		Size: 7.2 MB (7209560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:583115bd2580906ed8143b340483b9127157afc7a16ea5fa511e19955755b781`  
		Last Modified: Mon, 10 Mar 2025 17:40:14 GMT  
		Size: 15.8 KB (15819 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-1.12.0.1530-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ae2728e60994f6ccf633498c4fd75b626c4a9e0c6c459cf9cd946bdce68a5289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.9 MB (284896466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce9068f27258a6a63c7590eda14eff0334255a2341288be0a0fcd70bc4e8b96`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
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
	-	`sha256:7e1cabb756c27ddad3e1de86c2aaf2bca04f012bff531cd99d37f98896026ca4`  
		Last Modified: Tue, 25 Feb 2025 01:31:16 GMT  
		Size: 52.2 MB (52248644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef10ee5ecae1d9e3226dc2e461bf86d8923328cd233ecc4161f5a7e669aa40f5`  
		Last Modified: Mon, 10 Mar 2025 17:57:55 GMT  
		Size: 163.3 MB (163341424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77794f1521b81956ac8999e8b701249d6ceda6c4c7e55af2de23b2b200d78767`  
		Last Modified: Mon, 10 Mar 2025 17:57:54 GMT  
		Size: 69.3 MB (69305353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7afd1c127530fc95bb173ed2b7ec7285552821ce42953399187d57fd446156`  
		Last Modified: Mon, 10 Mar 2025 17:57:52 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae8557d1962d1cb29e177583744c8dff3a8c1496527743c567a019849a21b27`  
		Last Modified: Mon, 10 Mar 2025 17:57:52 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:4b6e4228abd30004244d07859f9e438d2ea96ba8f9ef7d307a658766a7edef51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7229976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3120e8fecf9153987d85873585ee1d4ec71c0d3824699e640d7d759290e66a6f`

```dockerfile
```

-	Layers:
	-	`sha256:ab0363ecf6e2fdc0e6487526e9ad5bb3c7127a832eb6013080775e3270ad82ee`  
		Last Modified: Mon, 10 Mar 2025 17:57:53 GMT  
		Size: 7.2 MB (7214038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6be547cfb4ee903bdd6ab90ea2ae6d3776ef61ddd219acad25815ba2fbb3f9c7`  
		Last Modified: Mon, 10 Mar 2025 17:57:52 GMT  
		Size: 15.9 KB (15938 bytes)  
		MIME: application/vnd.in-toto+json
