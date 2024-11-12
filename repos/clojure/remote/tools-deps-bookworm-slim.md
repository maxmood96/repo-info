## `clojure:tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:16187edeef461072b19cc16ff88bf1cda78ba1c5e506db6b1a4ff79af1ef916a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6b217981a3952f747cf12cadd0e573f89189108ca131e94d4c7481442e69c5ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.2 MB (256184609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46243c8757d776163e2c789dff47b2354ef951e8ca31e2e30e70f244e5c11903`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a508a80b47ab791a3c316a7995bf7dc31f191f6f299c11ce462146ce03030dde`  
		Last Modified: Tue, 12 Nov 2024 02:24:38 GMT  
		Size: 157.6 MB (157568686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be46ba7ac074ddf6808f22eafd620d9f3c32612eb3923634949bcf6be960e929`  
		Last Modified: Tue, 12 Nov 2024 02:24:37 GMT  
		Size: 69.5 MB (69486886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2289eef2e49388214da6548b776c3f7f89e942338c5e8a30c6c67a20cf2c5f`  
		Last Modified: Tue, 12 Nov 2024 02:24:36 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5cc06e8400971402d57e6d455c2adfcd4c66a3b31f19fb0d2a2c9f4250bdcc`  
		Last Modified: Tue, 12 Nov 2024 02:24:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6d6235ea9701f5fe0244ee28cf6a7b9d93574e6f50d40dc1691da2765af7d9d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4941005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2425ed98d92d634f396068b4bd58d99077ec5722c16ee27254d5c9e985965de5`

```dockerfile
```

-	Layers:
	-	`sha256:41fa074b5a93529697fbb30ad3bc2f3ac202f68dfdcdb06831fc1e986fa62f52`  
		Last Modified: Tue, 12 Nov 2024 02:24:36 GMT  
		Size: 4.9 MB (4924431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf3044ef91298b5ed25685b3fbdee496524870237d2d8252043c487b188e398d`  
		Last Modified: Tue, 12 Nov 2024 02:24:36 GMT  
		Size: 16.6 KB (16574 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f64b1ed7cb7e487b00db6b78b655333008caad54038f63786b870fe5f4a07688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254295554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af30f3490e1f552b268d529ddf722798dfa085aa0bf75c76a7923ce20f8b4fdc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
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
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31de618d5329242a89cabf67cd0c3841b6c256ef62dc7074f5494636b182a3b`  
		Last Modified: Thu, 24 Oct 2024 09:25:25 GMT  
		Size: 155.8 MB (155793069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182f699111b18617ca5e05ba1f2f853196600fd23649d82e1b1036ef9d80cd65`  
		Last Modified: Thu, 24 Oct 2024 09:31:34 GMT  
		Size: 69.3 MB (69345105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b4aba3c403838e8175e5038580a8ca16ca5ade96ed0a384768c7ecea069af7`  
		Last Modified: Thu, 24 Oct 2024 09:31:32 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab7e8b2dbc3a7241a765ef2339304829cc758bfbb8692ecad6872a2e0b21cfc8`  
		Last Modified: Thu, 24 Oct 2024 09:31:32 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:467d4438ad736dc1fa7c3aedca343f9ccd07ffe5f91d1d6c349077eb6ba969b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4946736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec89aef540622c9b160942cfa98f8935dc09c694fc659b8de1b01c03cf1ba3d`

```dockerfile
```

-	Layers:
	-	`sha256:7a31a0370d6c990833fa8ed0b879a2740441c2c7a7857324ed1205d2b9026b07`  
		Last Modified: Thu, 24 Oct 2024 09:31:32 GMT  
		Size: 4.9 MB (4930185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbf8008722d358d1803b7a516afa4958ba082dc03cc9c98fe89f0c4c94d85b62`  
		Last Modified: Thu, 24 Oct 2024 09:31:32 GMT  
		Size: 16.6 KB (16551 bytes)  
		MIME: application/vnd.in-toto+json
