## `clojure:temurin-8-tools-deps-1.12.3.1577-trixie`

```console
$ docker pull clojure@sha256:0a61aa965e70a6b44cac022e87cd11c010f07c538f0503a1574766081a2dc0de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.3.1577-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:3b5ce12e9070dafbedfe9eea98685deff5d1eceb89e5f239408d10b2a48e9d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192515447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ffbead9c00e836d7b9ecf71b53e9ac6df100403b99d84087a2f2c28b7f5bff`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d0a2aa8a8e9647a643c4f6b3264bc6422a6b3ab7ec00074da78d9055e12b2b`  
		Last Modified: Thu, 02 Oct 2025 08:56:14 GMT  
		Size: 54.7 MB (54731291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfeb101092453df9b9240a5da1b136f82bd21f00460c23ef18682447017f4e0`  
		Last Modified: Thu, 02 Oct 2025 08:56:18 GMT  
		Size: 88.5 MB (88498883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3afe560e37070851df905d9875996cebf058c6d86cda77115e543c7fb54e663`  
		Last Modified: Thu, 02 Oct 2025 08:56:08 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ad673e44171a5397042c3fd45d4d0d0ac516900bea13b25e9a1b3b9f839dece4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7602721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676d9ccab2aa1fe53b43927f57441f08e90c987d5bf173cf4da231b78fce0548`

```dockerfile
```

-	Layers:
	-	`sha256:6b0de98e53cd8c7704da34fdf4e3d0cc2cab4fb7062ce8c092d21a72d013e21f`  
		Last Modified: Thu, 02 Oct 2025 12:47:55 GMT  
		Size: 7.6 MB (7588509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d79a4b27c3b6edc587217aa261f5e19b5f61c4171d1c6cead288fb55da1711c9`  
		Last Modified: Thu, 02 Oct 2025 12:47:57 GMT  
		Size: 14.2 KB (14212 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.3.1577-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e3ca314e9c3d414838736c7e68e6734a63e9fae2009405640ab99ea8e25165e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192175489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56d8ff8bdebcc014b1e9bf9b386a348bb6562593f6c09c46a0e684c650fdf212`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:28aec8b14b3eeacbf47ef38af72fab694b109fdcdf31581722750599baf1a932`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.6 MB (49648695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294d58c593997f72fdc61dbb01c6ed0a89e970af1c77b6e76d18b00bef5a4c84`  
		Last Modified: Thu, 02 Oct 2025 03:31:09 GMT  
		Size: 53.8 MB (53835607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29342fc5f8b1471a2ba4b812fe6662c0628ac411b1216646c2db58413fb0f834`  
		Last Modified: Thu, 02 Oct 2025 02:41:16 GMT  
		Size: 88.7 MB (88690544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53981a01908addfe566dbb7febfb7e810cdd44b28ec4a2a2e671dab218acd833`  
		Last Modified: Thu, 02 Oct 2025 02:41:07 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:eab78aee19cf740affbc5934ce811b89d293f73b0d144fa70d40ab96f51db016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7610568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12cbcade19a69daefcdbad92ce893143c85cfa43b412ce13159c7d24e5f4001d`

```dockerfile
```

-	Layers:
	-	`sha256:65d271e8bc0dc86268fcff44afd0a6e0aed645e5c8e06ef71cac46e00d607ef3`  
		Last Modified: Thu, 02 Oct 2025 03:37:46 GMT  
		Size: 7.6 MB (7596237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:108d4fce546e2b5b477f922a8982b99ec8b0decd7f6f8b8800fe4a9f64acc8c9`  
		Last Modified: Thu, 02 Oct 2025 03:37:47 GMT  
		Size: 14.3 KB (14331 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.3.1577-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:32b7f9e0801fea7f720ea132aa0237d56fe78425e7cc6612e55b4a628742ade0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.4 MB (199426922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20dc89fa90c553152ea02c5d32954465043d55aa51d386b6fa86c7dec74809ee`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:71fbf24a239310917388930bb043e64907cb532b9ac8f265e44e032dc3bf4409`  
		Last Modified: Mon, 29 Sep 2025 23:41:05 GMT  
		Size: 53.1 MB (53109217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b106d493cd6e406e3ad2015474e420aa8c22ce4a24af63afffe7efa48b35f7d8`  
		Last Modified: Thu, 02 Oct 2025 08:04:15 GMT  
		Size: 52.2 MB (52165400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e88a7176cdb3322a91da3f0f834684762140e286134e904bc008fea9e85416`  
		Last Modified: Thu, 02 Oct 2025 08:15:13 GMT  
		Size: 94.2 MB (94151662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85223edc4d7440ef8cbcd0057ef66040f76427164009dad9cd7af388f07a78e9`  
		Last Modified: Thu, 02 Oct 2025 08:15:01 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e5e9599839bc9273200389ee5024cf6223b736d0e3567a0ec4becce1a3a4b883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7607782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce563eb42756d2f9d42aaaf8816a0f1cde72f47fb47998eb0d7972dfcdb23999`

```dockerfile
```

-	Layers:
	-	`sha256:f779f1827f98888d63ef89e45948258c8c52141a82c2f421675c158eef746f94`  
		Last Modified: Thu, 02 Oct 2025 09:42:29 GMT  
		Size: 7.6 MB (7593521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1ea50c09c64ec841bb6c1fb8bdfc673811dbaee9b94b7abf684890039bcafcc`  
		Last Modified: Thu, 02 Oct 2025 09:42:29 GMT  
		Size: 14.3 KB (14261 bytes)  
		MIME: application/vnd.in-toto+json
