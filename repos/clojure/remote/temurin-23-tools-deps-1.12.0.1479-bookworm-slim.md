## `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm-slim`

```console
$ docker pull clojure@sha256:f6369d177fb97ce1c11a39be5906c38f045ce773597f9d9657d4439fc95b53c0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:45c583ff7f0ea9e77497e020f2030a46aa2a6ca3d16872236cbf70f2b9afef8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.9 MB (263877683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c3ce9de6f314b6df32046103beec5573e0a451fdb71cdb7c7f2f311198f32d4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
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
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da8b417e94ffe90cc045694624c53796b632c1af2ac457a9af33455dd7731b6`  
		Last Modified: Thu, 03 Oct 2024 19:00:40 GMT  
		Size: 165.3 MB (165267610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83e2d85220e06ab2c4f462dfae3cc82c21172ea2b931e7510c70d55d506cd3b`  
		Last Modified: Thu, 03 Oct 2024 19:00:39 GMT  
		Size: 69.5 MB (69482758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc9c33df973c66d4f6f7071feaa1aa6c373d519e21c791a29f2823657c7f9c9`  
		Last Modified: Thu, 03 Oct 2024 19:00:38 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d234164a520e5bfc06aa41e420e9f2de9d57d611dfa69a3a6e506b718cfd037d`  
		Last Modified: Thu, 03 Oct 2024 19:00:38 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:92eb0c35dc10755d70cbb0f1ea09254143dffed85209b3f74ecfe0ddc2d48b4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4915326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98a46fd8af3eab1e48ff819c6019c5f67e10153013d2e706e67e7e6a658e728e`

```dockerfile
```

-	Layers:
	-	`sha256:90e83032ea7a8bb5df836664dc3bae312d7bd8d5a4053a83249f7047d13ed8a5`  
		Last Modified: Thu, 03 Oct 2024 19:00:38 GMT  
		Size: 4.9 MB (4899844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:374dcd3729d583d38f9474d26838e43e7a9e52822b3f34e08c335090df957db6`  
		Last Modified: Thu, 03 Oct 2024 19:00:38 GMT  
		Size: 15.5 KB (15482 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fb5fb22e7b85cdde29e88239f6ae1dcbf7764eecd4322f94ce048e6b8a616b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.8 MB (261755635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7fa2a5e894d09bfa3f514e85d0a4b95fef5198b596b9a4238a9b4bc5e76a756`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
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
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f2181aea0e19380ae77b609dc8da808603701a8fecc4831f1adbd3eef11053`  
		Last Modified: Thu, 03 Oct 2024 19:01:58 GMT  
		Size: 163.3 MB (163252821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c01715e17693b4ecf2dfc4f187c93e513e5f057b6735787d34127e729344a45`  
		Last Modified: Thu, 03 Oct 2024 19:07:41 GMT  
		Size: 69.3 MB (69345408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9676374a7b14252ab1df72e783993c033a7902138cbe2daac132efa3e33ed95`  
		Last Modified: Thu, 03 Oct 2024 19:07:38 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc713dda8979d9152724562aa1e175a9ddedf57d41699987f3d715b5a5c2a2f`  
		Last Modified: Thu, 03 Oct 2024 19:07:38 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:553f05445b56f217ded4ef922d4e30ef29e8586e8aca54e2e89c3f90d504f86b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4920612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c077344a5bd9afd109f013f4df80f722c445c6215377821beddefc8272e62af`

```dockerfile
```

-	Layers:
	-	`sha256:bc10b62ca3ad296041fa680445ee00b6f1b5409886d964199662a25511cc4420`  
		Last Modified: Thu, 03 Oct 2024 19:07:39 GMT  
		Size: 4.9 MB (4904988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b48f5b73a71c8db0d629080c6cac38183b195ceab455cbb394bde5b642bbf26`  
		Last Modified: Thu, 03 Oct 2024 19:07:38 GMT  
		Size: 15.6 KB (15624 bytes)  
		MIME: application/vnd.in-toto+json
