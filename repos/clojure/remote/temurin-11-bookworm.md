## `clojure:temurin-11-bookworm`

```console
$ docker pull clojure@sha256:7e743618d15b28125833f19fbf97fda9aec5aa95984b320ab4685f65a4a55376
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:2145189e726efc130184d6358f94a3b5bef34e5524da5239355e83f8f44de08b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.1 MB (275084060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640dd357db0a307efdedf93bec9ada86a24751c3abedf66fe623538cdd3eab54`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568d067a21b9c292bad949c83f55952167326fc9ed41790587fcf70d541fda54`  
		Last Modified: Tue, 08 Apr 2025 01:35:41 GMT  
		Size: 145.6 MB (145598936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabc176b8a2755ff5a42da0b39299809c11ebdf1628e428f309a134fca882901`  
		Last Modified: Tue, 08 Apr 2025 01:35:40 GMT  
		Size: 81.0 MB (80993938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5b3e6a6fa3c9580f375cbef40ee6dfcec19e503b4dd18356bb20cbde8aa1fe`  
		Last Modified: Tue, 08 Apr 2025 01:35:39 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:df7882dbedf062d94ac3e5adc0a8c770a4969c8cbc08f440d045aaae9719095a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7206868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f738171f2e2b5f8333709a712931a94e0d49eed88acba3379b3562a5b44bbe`

```dockerfile
```

-	Layers:
	-	`sha256:55fb4ae3571e328ec37f1bd1d021ab4518b7a0e0e3a98e3842a46a29d87c8f41`  
		Last Modified: Tue, 08 Apr 2025 01:35:39 GMT  
		Size: 7.2 MB (7192617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dc1ee471e16b2aa625392427d3df73877b713063d755205934c29d613f8d961`  
		Last Modified: Tue, 08 Apr 2025 01:35:39 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b38f46d242ed1d14cd96ccc51f35d2aa0bb76f88f57e8b00690836674ce93125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.5 MB (271533420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f7d153fa23f8e3c11eb32af13ed53fb672d614ae1080624b98e7d06edb953c6`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80416af1d3bf4ace7aa0e10ee519635ec3d15c0d12597a41d027eae7da592c3`  
		Last Modified: Tue, 18 Mar 2025 00:12:41 GMT  
		Size: 142.4 MB (142385459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d190f20538667c16df22cf1a15e2a15ca0f4edb204f331a726c276e6f8079e`  
		Last Modified: Tue, 18 Mar 2025 00:12:40 GMT  
		Size: 80.8 MB (80842460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f220c0a8b144efba18e222c53a5bbffdfde27fe53802600d4d6b6bf6abe57e3`  
		Last Modified: Tue, 18 Mar 2025 00:12:37 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:fb60ccd51a3a99552a59a94d4f4144ba6f65514032d7cf4389c325133f7a5f77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7211998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccfb03beb11cfbd7331a0a2bbbc5b1386d6e5ff386668f68c9ce84f804c05684`

```dockerfile
```

-	Layers:
	-	`sha256:1686dc0da175281623b6eddd0a7b4f46ad64270931984006ff284e2c1e6c4f18`  
		Last Modified: Tue, 18 Mar 2025 00:12:38 GMT  
		Size: 7.2 MB (7197630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55f69461567512742dae394fbdc0b31456795094f9a5bb81212b3e2c6901ec4e`  
		Last Modified: Tue, 18 Mar 2025 00:12:37 GMT  
		Size: 14.4 KB (14368 bytes)  
		MIME: application/vnd.in-toto+json
