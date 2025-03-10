## `clojure:temurin-11-bookworm`

```console
$ docker pull clojure@sha256:7cd9686bc21b002dd1c51bef670eb0d75957dda9453cf3be5cb95e254732210b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:0eed677b9d39d66e412fb418cd51d3b9fb06361e1a144e1ba0423563311e6c75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.1 MB (275068597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8e339d2ba5217babf62b32f53ba8cd4cae29a4f3e73b3a71b1a94377686935`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5704120e767113ba68fd0f0d0dd7b9c0423e9f7ffac125da9d736fd6ccd2804d`  
		Last Modified: Mon, 10 Mar 2025 17:40:15 GMT  
		Size: 145.6 MB (145598936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b991010d5efc835cdb063269522eaaff6c44d7aec869c9544593f69d4cc9fd60`  
		Last Modified: Mon, 10 Mar 2025 17:40:14 GMT  
		Size: 81.0 MB (80992916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ea11eb86df1bef34f8e61fe2e6c7e4bd373871dd7a758e0f92ca92d60f87b5`  
		Last Modified: Mon, 10 Mar 2025 17:40:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:34755fcee4b460b647c9b2cf6398c03c6f79030c99485315e2f2275e67f3bd3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7205489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b89f00627e716353dcad16a8e01f4819b1311099369fdc123a76cd69f7e340`

```dockerfile
```

-	Layers:
	-	`sha256:ecab0d65c3b34dbf2af4a222cb8589ec84100f4c6d6e6093cde77f0f11a81229`  
		Last Modified: Mon, 10 Mar 2025 17:40:13 GMT  
		Size: 7.2 MB (7191237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:531161e0bb4f4869cf8ae83c6b08af7ff9542d14c84120c08c1af9205939b6f4`  
		Last Modified: Mon, 10 Mar 2025 17:40:13 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ac7d283ec4e116553a3667a6bf51fba57a898f1da21ad416accb80a4033b548a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.5 MB (271536833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14d2025506ba5807d985b934816f5e0f0d34d6329e0ba6108b4c685713900550`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303b40c1583f8acc6e9f8c60814390e2911071d4d448b7b11902e6e80aecbf3e`  
		Last Modified: Mon, 10 Mar 2025 17:50:14 GMT  
		Size: 142.4 MB (142385396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad930e0d9d35251c41a01848aa220fa03a59ddbdd62ce2d9f00fdc5ff1616d6`  
		Last Modified: Mon, 10 Mar 2025 17:50:13 GMT  
		Size: 80.8 MB (80842783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd1da300a5e5cedcd829999f5a11f8ba4c5b2d0744ed5410965012fe2cb03b1`  
		Last Modified: Mon, 10 Mar 2025 17:50:10 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:66ea81c5080158ef93b23515f29b24a32553fc4997f66cb5d5661b0192d17b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7211988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d555c97a81b69d75ed651ff620eb7508a441cc878cbfe899ec9fdd86a2ff1c4c`

```dockerfile
```

-	Layers:
	-	`sha256:d797ad171b33419d8b964748dc7e08dcbb149bf51474c342db918c894441ed7a`  
		Last Modified: Mon, 10 Mar 2025 17:50:11 GMT  
		Size: 7.2 MB (7197618 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d27eb29e908510c476dfbf7d0e1b3a432df4afafcaf82abe6d884d29746adb00`  
		Last Modified: Mon, 10 Mar 2025 17:50:10 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
