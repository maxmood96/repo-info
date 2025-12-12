## `clojure:temurin-8-bullseye-slim`

```console
$ docker pull clojure@sha256:f027a1b2cc28bd326de6e7f869a6e4420d13a4e9089d3ae27ec0fde6b8c955a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d255ca99e8e910999c160c3a84dc7488b925b026b4a14330238170e79a931543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144142425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bab582241b35664884e4c287d91fba366d324806aef1efdff8160e258ca8b1c0`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Thu, 11 Dec 2025 22:36:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:36:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:36:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:36:15 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:36:15 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:36:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:36:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:36:28 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a88499d92e58a9f7d74dc939bd949d9c2d87abbbaaec03b5f87553e69d901a53`  
		Last Modified: Mon, 08 Dec 2025 22:17:50 GMT  
		Size: 30.3 MB (30258465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2a0759b132857473e9712094fa4a76568dc9cfaedb45e3c5c551b69133bc60`  
		Last Modified: Thu, 11 Dec 2025 22:36:57 GMT  
		Size: 54.7 MB (54733373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3590e403eb7ff793b996b2bf6602bbf045052121f5eb4a51ea4ca9717a7bc84e`  
		Last Modified: Thu, 11 Dec 2025 22:36:54 GMT  
		Size: 59.1 MB (59149941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bd9ec3b28d7a9f1793298501a6614048c7f6154bc3871db5ba88950b97e1c4`  
		Last Modified: Thu, 11 Dec 2025 22:36:48 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fdd0878c1cdc0de8a17ae1e26dcb2fc22a1dc427f63e21b8a7767340b6635ea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5443924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31bfddc588ae2b07f21f76153887fd7fc5ac40f9e27855a4fee7af92b805ab53`

```dockerfile
```

-	Layers:
	-	`sha256:9a35f181a9532a4f2fa370e90a460da8e1c98bf5d90067fe549b217e72d63f4d`  
		Last Modified: Fri, 12 Dec 2025 01:46:41 GMT  
		Size: 5.4 MB (5429677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77332a7ba0ecf9ab2c1760552eaf9fdd08528592d25fccf097cb553ec96f63a0`  
		Last Modified: Fri, 12 Dec 2025 01:46:42 GMT  
		Size: 14.2 KB (14247 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fc2648c1558434176c44f1f8ea84b86c0ccbb3cb1630cd60af12fb5b2f76b0f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141848690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35634be7bdda2e5d4b35ce6f8117fec784dbd0deb5fb5b613e9f90d265830c16`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Thu, 11 Dec 2025 22:35:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:35:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:35:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:35:25 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:35:25 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:35:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:35:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:35:39 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7d43510e20279c4831f5ca1d424a1d56c6c24251d7c93288a50a066dc7e72bda`  
		Last Modified: Mon, 08 Dec 2025 22:16:06 GMT  
		Size: 28.7 MB (28748482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4b75759e7c826a872d67e5ace7f30975641048fad91669fdf2c70c34059636`  
		Last Modified: Thu, 11 Dec 2025 22:36:08 GMT  
		Size: 53.8 MB (53814975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4970220c5c81f80f61b3321cbf20d0ece0f8aa992c38a69154b5aab61b7cf8ed`  
		Last Modified: Thu, 11 Dec 2025 22:36:07 GMT  
		Size: 59.3 MB (59284588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4a16f12ccd51b2283c291eac8448a44c221d292bc0db6deafe5462c3169c42`  
		Last Modified: Thu, 11 Dec 2025 22:36:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0d101e507f4584f3c477274d2bf35b1442814e78ee67cbed13ce2ce611f7e0f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5450472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6c2d44659f2542c1c10ac6d66be44451783110b920b7a290122b95026089bf`

```dockerfile
```

-	Layers:
	-	`sha256:1cb6f83fe91b098d0359fc02d181986b1b0cbc6c605eb6376c97be263c4c6579`  
		Last Modified: Fri, 12 Dec 2025 01:46:47 GMT  
		Size: 5.4 MB (5436107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a90bf3c040cbfe62fc261651935aa21b2bbdf817eb972395ecdac015775f1c66`  
		Last Modified: Fri, 12 Dec 2025 01:46:48 GMT  
		Size: 14.4 KB (14365 bytes)  
		MIME: application/vnd.in-toto+json
