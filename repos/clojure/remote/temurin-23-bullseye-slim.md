## `clojure:temurin-23-bullseye-slim`

```console
$ docker pull clojure@sha256:f98c305e4850030b787dff722d02efddb5140323c966367f2426b97c993aefa5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:fe7315329457c5685d008553afbfc45c402cc1925bf8c39e8a069d21104bb665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254329825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a1807429c2406f954dffd53ac55120e328a11121208d0385c708fd8070dad3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6c87eefc1f428634061bcdc9ec95ccceecd7c7475d35a777479af83f64ee6915`  
		Last Modified: Wed, 08 Jan 2025 02:30:32 GMT  
		Size: 30.3 MB (30252643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638a2b60981ecf3612b8fbf0a1e34e4be0efd56b143d6ee94ab7472cf96e1fed`  
		Last Modified: Tue, 07 Jan 2025 02:29:34 GMT  
		Size: 165.3 MB (165295113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776f08b5ee5cbed69dd6b0e6d4e5735ee9f755aaa76fc7f2a5958832deada7ab`  
		Last Modified: Tue, 07 Jan 2025 02:29:33 GMT  
		Size: 58.8 MB (58781031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9200d0c05032f201c97bfe1bd8e6a2b9272db22200b097dbe05de53e89152112`  
		Last Modified: Tue, 07 Jan 2025 02:29:32 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05067377ea4c099391cd6e8414e71f4e2ae7c919a62213ceb5ac216485a45879`  
		Last Modified: Tue, 07 Jan 2025 02:29:32 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cc10c72594240293760e0a79c77f0fee84f2b6a2ecbc73013f985322831c7bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:757532fd71da36f69d70272aa1c93d845a3f94b3db25df129f5c5c89898ad05c`

```dockerfile
```

-	Layers:
	-	`sha256:ab06b550d55b6646228d63b686c7b87c3930a38cb4a9dccb631be9fcd48501fd`  
		Last Modified: Tue, 07 Jan 2025 02:29:32 GMT  
		Size: 5.1 MB (5122074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3e077ef256897799f09917defada048f03ebed80c162df930f9bf1c20af3261`  
		Last Modified: Tue, 07 Jan 2025 02:29:32 GMT  
		Size: 15.9 KB (15877 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fdfd694d95329fbda2a328b82e0a33e392bb85499608bda68e0a780d19ace9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.9 MB (250932894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630891409a092f01300c1a67a36e4a917ee4d7aefe42ea218e96cc1ff44f611d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:879a6187682fc52c69294a2f450abdb54e257a50e8133ec6e89cb140345be6ce`  
		Last Modified: Tue, 24 Dec 2024 21:34:50 GMT  
		Size: 28.7 MB (28744853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5b4fb805b80b71c3e0694a62a0807be3fbcc30b4f67cf6fa8370c3421f0982`  
		Last Modified: Wed, 25 Dec 2024 07:39:53 GMT  
		Size: 163.3 MB (163281786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bec54235a6d96df2358ef1c9a16d1f84c34c259f63f2936191fa95e34af72b`  
		Last Modified: Tue, 07 Jan 2025 03:38:33 GMT  
		Size: 58.9 MB (58905215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955b90af7a64212921f379114d683f1ad259102ca5b7713828b8ad8c729d50bb`  
		Last Modified: Tue, 07 Jan 2025 03:38:31 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27eeca1ffe02466f09c266336743183f5805b7f68d7bb4d4624e3a3686861aca`  
		Last Modified: Tue, 07 Jan 2025 03:38:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:130c70acec62d3c1e499f5fbc0c74f098ae4102aa6b18a4baa0a9b99580fd4b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5143181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65101f77953f205e27958b96a902abd2b8aa29080968addd73586fcf9ca2bbf3`

```dockerfile
```

-	Layers:
	-	`sha256:891b41d18847162d60fdaf17abf304265d16aa8c0a314db4b2620b26d2c2ad41`  
		Last Modified: Tue, 07 Jan 2025 03:38:32 GMT  
		Size: 5.1 MB (5127185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9445ef179c4453497e3cdf506592678db7852657b5bacce7c3c011dab3e73ed2`  
		Last Modified: Tue, 07 Jan 2025 03:38:31 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
