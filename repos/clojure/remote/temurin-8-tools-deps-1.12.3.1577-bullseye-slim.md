## `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye-slim`

```console
$ docker pull clojure@sha256:a9828be764c2804ca838e19e98432ece17ff4c60669e521bfcbaed1b51ed6268
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5434dd2185e6cedd72fa5031e8272d0ca3d0b6645930d00ec161a9e4c1767123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144144120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da41e581a4719a250f8b4bc1b3fe7640d74d89e83c771cc5b89b872d0cdd3653`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:50:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:50:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:50:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:50:02 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:50:02 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:50:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:50:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:50:16 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a88499d92e58a9f7d74dc939bd949d9c2d87abbbaaec03b5f87553e69d901a53`  
		Last Modified: Mon, 08 Dec 2025 22:17:50 GMT  
		Size: 30.3 MB (30258465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc64fb9e4c8904524c0e6a81dfdfc06c1bb180140216432296eea166c5df800`  
		Last Modified: Mon, 08 Dec 2025 23:50:42 GMT  
		Size: 54.7 MB (54733371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d99f98ea3c77d4edc5e95008a9773e67c439bdc1672b12e9979b1ac2e1476a0`  
		Last Modified: Mon, 08 Dec 2025 23:50:42 GMT  
		Size: 59.2 MB (59151642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c831e2d64b846512c26c9bd85a7937ac11d307c95f25a0aeeb4c6c77775379f5`  
		Last Modified: Mon, 08 Dec 2025 23:50:37 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c8e569620f9bf8c51df7291063e88509887600ce2b27af1a94b7cef24cf71b7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5443923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f5d1212dd644de9c230aa7f9620144c039ec775d9bf950c452141ff94ef23b7`

```dockerfile
```

-	Layers:
	-	`sha256:f8f33547c960988fa5d5e70978bba2c06b7264cb1acc3a627e3061aa99f58314`  
		Last Modified: Tue, 09 Dec 2025 04:48:08 GMT  
		Size: 5.4 MB (5429677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fe8f1639653043c3778b2e88de637207084bfe238bce01355a31b92ea54b02d`  
		Last Modified: Tue, 09 Dec 2025 04:48:09 GMT  
		Size: 14.2 KB (14246 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9745430bbb07701953578641f69016d4357ea28b8d4194443fed5990cc065f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141851799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:373a397515bd9094ac259370446178af21faf247e6ac7587187b256fcd732c32`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:58:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:58:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:58:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:58:40 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:58:40 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:58:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:58:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:58:55 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7d43510e20279c4831f5ca1d424a1d56c6c24251d7c93288a50a066dc7e72bda`  
		Last Modified: Mon, 08 Dec 2025 22:16:06 GMT  
		Size: 28.7 MB (28748482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a9fa0e0e2b9b154d8b401b22046c49a7fecf426010b8eadc8eafd64dd39c22`  
		Last Modified: Mon, 08 Dec 2025 23:59:22 GMT  
		Size: 53.8 MB (53814992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3df21ffbcd338ae1ddc70625b6fa73ec5caab372f512dfb691208fd8191b5f4`  
		Last Modified: Mon, 08 Dec 2025 23:59:22 GMT  
		Size: 59.3 MB (59287680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d568c6b1cbecb95e02ccb2f2170b56b7b6b131a7ff8863918f274aa8cefbad1`  
		Last Modified: Mon, 08 Dec 2025 23:59:16 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f9bf3746618c89819c52f51a239b5b928ea9819d6ee07eac8f3c7d7e479e2af8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5450473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c8b5e232a9a6327308ca8cd09fd9bf4b6413a10721118a0c4a37c2b39e4d9c1`

```dockerfile
```

-	Layers:
	-	`sha256:1b7ac4922dab3cdbc70a907edd96423ddbcb01bfe8f1cf83954e3ca9c58c4f3f`  
		Last Modified: Tue, 09 Dec 2025 04:48:14 GMT  
		Size: 5.4 MB (5436107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71b9e393cbb9d7c024d5089c26a6cba9b793b076587fc7730f7c21c6f49fa1d0`  
		Last Modified: Tue, 09 Dec 2025 04:48:29 GMT  
		Size: 14.4 KB (14366 bytes)  
		MIME: application/vnd.in-toto+json
