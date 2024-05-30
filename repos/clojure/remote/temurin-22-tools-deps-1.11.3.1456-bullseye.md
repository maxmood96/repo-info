## `clojure:temurin-22-tools-deps-1.11.3.1456-bullseye`

```console
$ docker pull clojure@sha256:088b6500de1d8ca8cbed684d5426a60a6a8b2b6a2aa6e122ae70dbd6617446e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-1.11.3.1456-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:33d2a19b8a0fb4c4d9386b0011b8fd283ece48671fbcfc52821d1a9fa2e948f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 MB (280632290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1569b914e5e60b8b1e904b84314dc58a61a549a2a9d68d20e6f840132e50f62`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:28:14 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 14 May 2024 01:28:14 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5450f27dbd9b9fd0347d787cba74d81bbe13a56d3c0c2e0db084d707ce48bc8`  
		Last Modified: Wed, 29 May 2024 19:59:26 GMT  
		Size: 156.7 MB (156715502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2b5c5117b36d04d55b23fdaade95e5868db5055c9027b4f7080bbd04583b5c`  
		Last Modified: Wed, 29 May 2024 19:59:25 GMT  
		Size: 68.8 MB (68816340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6613035c1716e5c150436bd7c1830987e128c778dd33599f7aa4d8582faaf60`  
		Last Modified: Wed, 29 May 2024 19:59:24 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9005e1dba41c1becbd93e1be93463c779e523b36c6e97bc6895112af5e8f25`  
		Last Modified: Wed, 29 May 2024 19:59:24 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.11.3.1456-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:463f787937d4e641a8f8a2889bedc8d6e5a799e069bfc743b5d9dc16330284fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7015136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19258c638f77a30de9aee3e39d00ac20d0ac419832c8712a116235bcd5a2e80b`

```dockerfile
```

-	Layers:
	-	`sha256:7d2c940fe696fc31c9fa062d9fcd053bae74b79de54890de3a67f34c6315746c`  
		Last Modified: Wed, 29 May 2024 19:59:24 GMT  
		Size: 7.0 MB (6999746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0829d39d7dd611f6369ac920013817a72343a32c508053c7f6aaf34ef4a93a29`  
		Last Modified: Wed, 29 May 2024 19:59:24 GMT  
		Size: 15.4 KB (15390 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps-1.11.3.1456-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6cae71f07f9ab62871834092f120ebdae5da0bee441428fd7813c794b5ef1e8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.4 MB (277407344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6243246a85dc8ddd3d6855c2ac34e75b926053526b0dfe08dd395e73efe20798`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:47 GMT
ADD file:43721c605da3f74f0c3f71384780fc0e57e2478b88197672caaf4baa3eddab23 in / 
# Tue, 14 May 2024 00:39:48 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:078d9526cc72763b2db16388f6b511c18a73e3e7f9d229364b3b85a6b5277bc8`  
		Last Modified: Tue, 14 May 2024 00:43:13 GMT  
		Size: 53.7 MB (53738990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5d071f94f0c3964a4deaafd6866af2b5c74f604a4aec7ef317e1b404399677`  
		Last Modified: Thu, 30 May 2024 01:52:52 GMT  
		Size: 154.7 MB (154737940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54510924510574b590e30445fd82e1dce924027f6b79d9cf014cc048b74a36b4`  
		Last Modified: Thu, 30 May 2024 02:08:01 GMT  
		Size: 68.9 MB (68929369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d8f713b487a3ac85cb7ad3b19a3c4005354919f665778bf8ced6758aa3d9ed`  
		Last Modified: Thu, 30 May 2024 02:07:59 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c980cb961c06bea984705e8f5c91326e482e49cac9ec5199952c39fcebfd95`  
		Last Modified: Thu, 30 May 2024 02:07:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.11.3.1456-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:9ab15708c90f8bcd50979164a636b182c24bc1301babe642755c21c2555c159d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7021394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:012d6c9ec85e3e31bcd6e22afa283a6495f1e0b7d051b9b328aa4f5b9299cf04`

```dockerfile
```

-	Layers:
	-	`sha256:0ff7c11cab969400a30f9674f28bbf73b0f7dc0c9e538a40a7bcc0c6833d469f`  
		Last Modified: Thu, 30 May 2024 02:07:59 GMT  
		Size: 7.0 MB (7005468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3443e07107290fe4081adc6838c7669bf71176c134a35edfb6877496c7897bc8`  
		Last Modified: Thu, 30 May 2024 02:07:59 GMT  
		Size: 15.9 KB (15926 bytes)  
		MIME: application/vnd.in-toto+json
