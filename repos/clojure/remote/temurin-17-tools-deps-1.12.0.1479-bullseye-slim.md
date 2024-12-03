## `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye-slim`

```console
$ docker pull clojure@sha256:dfec9002184650587404083bd234e3ae2bdb0525e168287694aa5230de71b3b3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b13106f89a2ecc562465ccb086b2b218c0f30614c6b6c475305427804b50fbef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 MB (233546327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ab41745be9b8e5c4396e38680138b8b64993516bd9eacf76a55ee63e6626887`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07eac5597ec3fdbfea238665e67b098c3ef491d319515c4618266bbdd4b20f01`  
		Last Modified: Tue, 03 Dec 2024 03:21:08 GMT  
		Size: 144.5 MB (144536664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd997129bb8d023e0de589e16de12734377db247d70ed8dc14e6db97911e8f5a`  
		Last Modified: Tue, 03 Dec 2024 03:21:03 GMT  
		Size: 58.8 MB (58755977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5def3e71546fe26644cd8d3c68a606833246ad8d24d8e4fc4900534d1dad48e`  
		Last Modified: Tue, 03 Dec 2024 03:21:03 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3840cfaf0baa068a82369d86b0bd8fa67a16528d4c981579695d8523436931`  
		Last Modified: Tue, 03 Dec 2024 03:21:02 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ba5bc76265ee50a4ab7c4899901fc2622a0de17e11b360babc2bfff4c5cfb150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0dfbeb1571b6a4627f4c98dee1d7becad6fa950437c1438b1a9b3e062f47988`

```dockerfile
```

-	Layers:
	-	`sha256:4b4db0d5397df17bc387a5106bbfea6439a355ecfeedc38a2f9db81de142dd28`  
		Last Modified: Tue, 03 Dec 2024 03:21:02 GMT  
		Size: 5.1 MB (5123549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d17e6633563e301a14580fde7b797a27aebc70682a9a69aad9d48cee9443014`  
		Last Modified: Tue, 03 Dec 2024 03:21:02 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:505f845c6973e7007de55fd47569852cca2a65e5099831ab0a2e268e02fad34a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232329997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf9ada41565fb98705807c5b9eb7a68dfae01d94924a7c803bd948a031b6051`
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
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5830c7c9e801f687e228dec0127a0dea10891bfae67095b136fc293a616aec5`  
		Last Modified: Sat, 16 Nov 2024 04:33:12 GMT  
		Size: 143.4 MB (143360989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66bfa198c784203ac9b329742e733995322f0eb42edb78cd1503423a83724f68`  
		Last Modified: Sat, 16 Nov 2024 05:36:03 GMT  
		Size: 58.9 MB (58876367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7599905d4e5a7065ebc6fb242abf3c1fc8e323ee470b1b74ff33fee508013ab`  
		Last Modified: Sat, 16 Nov 2024 05:36:01 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b267e5b73d0126f1e4ea0d23d49a629e95a392e7ea953c7f6d13807ecd6ff93`  
		Last Modified: Sat, 16 Nov 2024 05:36:01 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7aeb8e52bba08a07429de95e2a8cb4d5f5c2fd257743ec4ab4150f7baf8f05f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5147086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6f9f6f2a2ac9dfaa20634da75ce6490dcd30c3006272b420c6a959647c2e34`

```dockerfile
```

-	Layers:
	-	`sha256:aa89e37ef816a418f69c77732fbf8e3ca516d5d66951b246c8ecb3269322d60b`  
		Last Modified: Sat, 16 Nov 2024 05:36:01 GMT  
		Size: 5.1 MB (5131089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fa34a7757ddaebeece0cdd6fa5050739317e9a3ca459ad86917bbdb813530d8`  
		Last Modified: Sat, 16 Nov 2024 05:36:01 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
