## `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye-slim`

```console
$ docker pull clojure@sha256:2eca905275ee0cc833203923be4e5875362dd36b57261a176817cff4f7e3adee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6e549e2b182726ffa80dcd539bc50fc253b30adb2d64eba2af336afacbf291ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.7 MB (234729533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbac70e6090929806e690a584c365d00c0d1526fad060f5ea66742883a40b5fb`
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
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16e12802980eb25fd6c3e7b5d0e43b591222ca7eb0fd1eba8c2fc1e7d3b0e20`  
		Last Modified: Sat, 16 Nov 2024 04:50:21 GMT  
		Size: 144.5 MB (144536721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48f205b269b0a9106f3c1713532c30b301f03374a7746835a29f17556604f44`  
		Last Modified: Sat, 16 Nov 2024 04:50:19 GMT  
		Size: 58.7 MB (58740209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4dbab5b5c4bafcc1506e187f34ffd711f7d904fab7acda73302f9f61005cb2`  
		Last Modified: Sat, 16 Nov 2024 04:50:17 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1c38a73d82076fdf531ea37cb79c631e753065110c440ac9231ae48edc9bfc`  
		Last Modified: Sat, 16 Nov 2024 04:50:17 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c40042263058acf98115d9bcf81c6cee24cffb44f039c9d3d7ab937763fd517b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5141231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeae0486f1cb87e6e527d9a7bc7d1666d155c59169b9c6e7b5a0a429a8ae9260`

```dockerfile
```

-	Layers:
	-	`sha256:50580dfed0fc359aa522d2f345b946aa2552b3402a66ce032152c033fde1baed`  
		Last Modified: Sat, 16 Nov 2024 04:50:17 GMT  
		Size: 5.1 MB (5125352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2daa27ef154738fc7493b90e3fc90d0422c1fbcf01e8d2b4aa47ca5525a4689e`  
		Last Modified: Sat, 16 Nov 2024 04:50:16 GMT  
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
