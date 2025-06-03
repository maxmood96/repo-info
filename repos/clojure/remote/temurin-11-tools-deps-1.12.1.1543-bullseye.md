## `clojure:temurin-11-tools-deps-1.12.1.1543-bullseye`

```console
$ docker pull clojure@sha256:f00d328629fec34e7dbf391dfc348d7daf2ff13f01af0f4bdec0094b069a9e87
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.1.1543-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:5193d526cf5dbef6e85fd4876bce1fea957a8295b9623e38156ec1b00c3eb6bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268796509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec938a22a6f2c558ef48ee2dec9be62159e855bbe9eeb6f0e4c153f15ad54e1`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe83d876f4979558bc4d196db2bee4c10af2c08f79baff5a6210d5c1ac8c2c0`  
		Last Modified: Tue, 03 Jun 2025 18:24:12 GMT  
		Size: 145.6 MB (145635640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eac40915dde3e73c054f3f86b66b542df051c5516f9bfc490358c76a969c3c7`  
		Last Modified: Tue, 03 Jun 2025 18:24:10 GMT  
		Size: 69.4 MB (69410030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4001f4e8d2be50bbd64805ce85e4efbd299710a00f84a8bcf76e11e670ef53cf`  
		Last Modified: Tue, 03 Jun 2025 18:24:07 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1543-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:01ad9e7083040e8c3eef01f34c3743a20b9e26184e21e6c703c25972e5fe2ffb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7290579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3912c4721f3782e0de382117ef697fc8d952e6faa6ab1f6e2c30e615ae8d3502`

```dockerfile
```

-	Layers:
	-	`sha256:0ddd40b698b5cb164adf2f1ea796ebacd1fba3b95e157246ffee013f05f139b4`  
		Last Modified: Tue, 03 Jun 2025 21:35:15 GMT  
		Size: 7.3 MB (7276327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2176a7cfd3fe8fbeb0184cbedfdbe81322437cff93a6e55e207161de6b3c5c69`  
		Last Modified: Tue, 03 Jun 2025 21:35:16 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1543-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1456a81cedb5cc8eff59933f93b47b4a1617a451c667642cd95b813e8baf0bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.2 MB (264207036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e103be696ebfea041b289311d8742ca2311a183b8375c62c78b43fb25aca8a23`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdd289c7253c53f059da906341840e1077ab6a119d05f64b8c6dff33cf8bed3`  
		Last Modified: Tue, 03 Jun 2025 10:41:56 GMT  
		Size: 142.4 MB (142420650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33695234c2e6ab85b83f5e3006ef148188fc5db403693983140c0ec1d0935e6a`  
		Last Modified: Tue, 03 Jun 2025 18:34:25 GMT  
		Size: 69.5 MB (69537986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d6f0bc73ff82076c5dbff94995a3f0985cb1b36114ed5a015f440be471a9a8`  
		Last Modified: Tue, 03 Jun 2025 18:34:16 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1543-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1849198b65f29c92ec761e6e5dad5df44d30e72a2aa08c80d32d044fd9e26abb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7296414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:768388134fef1a45c8001951bfc612d79fd26242249736cb9116cb1a28eec8e6`

```dockerfile
```

-	Layers:
	-	`sha256:145a78c72ffde55e4df1d1417824427e03781d8771527379862ed0f4d39adb4e`  
		Last Modified: Tue, 03 Jun 2025 21:35:22 GMT  
		Size: 7.3 MB (7282044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a8986cb7f90eb29ae7ac8e2b8ab784a7f4ddcf9a19eb20eb4997c506b661232`  
		Last Modified: Tue, 03 Jun 2025 21:35:23 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
