## `clojure:temurin-11-tools-deps-1.12.0.1517-bookworm`

```console
$ docker pull clojure@sha256:44fb7cf719f33fe093c29d46da9e6de5e485a52f02fe7b6e18628cf1fa36a9b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1517-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:904957793c962da992efa20b9c82028f78d39817011a15946b0419f868e81ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.1 MB (275069766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe2244ab5e65a177d815cf5776b0207f264529a9e72433200e23e7a490e4ea0`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fe8f811fe2c8e2b3cc67365a66d537a49fde4eba7c511fd3db0ccd655c142a`  
		Last Modified: Tue, 25 Feb 2025 02:16:03 GMT  
		Size: 145.6 MB (145598934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ee2c44c2a6de65b311513924869f7d199a36408eccb0ee888eecd380f77f13`  
		Last Modified: Tue, 25 Feb 2025 02:16:00 GMT  
		Size: 81.0 MB (80994085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623ee11783fc8e11ba68c41fa1a9fb6f5a44ce0fdf8ed7174b1c6a9ec88fc81a`  
		Last Modified: Tue, 25 Feb 2025 02:15:59 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1517-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:af011e435634e5365143dd96f7f3cea570587220d2843691bbc42e9a5510bb7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7205489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65c8c20c677f1a6e7c8105f23ecf6e3040101032b23edea5cc02d40c5ccb2825`

```dockerfile
```

-	Layers:
	-	`sha256:a079a89d3ebc0f5a01a5a6ff20299dff539c2b5bbb17852e00b1532439ffaa58`  
		Last Modified: Tue, 25 Feb 2025 02:15:59 GMT  
		Size: 7.2 MB (7191237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45d1a90f21cc517f897feec74547477a13cc7df4912a8f782c14126141213685`  
		Last Modified: Tue, 25 Feb 2025 02:15:59 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1517-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3b67d901b917ac33a3e057f0e98b885f54729849e5e7f79e828fdd3641a891c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.5 MB (271537001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5573bbf79b8d1470285be5c9a72df0531974e47db1c521f67304cfc4ba0ea47d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb2f9b39fd107c3a1429362c7af01d5399568b883e7f731d9c0e63c44448f26`  
		Last Modified: Tue, 04 Feb 2025 23:33:31 GMT  
		Size: 142.4 MB (142385472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52186036e25f7ee63bcbd75ba1b5f07c1242f84cc983f8bbe931565b3a19098f`  
		Last Modified: Thu, 20 Feb 2025 03:45:16 GMT  
		Size: 80.8 MB (80844332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533f39faceac488ca6c76b0e8243bb06fe36f1141e080932135263917deea619`  
		Last Modified: Thu, 20 Feb 2025 03:45:14 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1517-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7edf6742195ccc91561ab6452c11be4f709f04cd9ec68c58fa8164fbfd16fc9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7211969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93cfbdded3a6903b924d02c386220984f4e5b131235bc5713f6b8d896a2b786d`

```dockerfile
```

-	Layers:
	-	`sha256:20a8775f2d1d26a85e1d50c5c80424850d0337ceb2b39779dbe3840f51742fa2`  
		Last Modified: Thu, 20 Feb 2025 03:45:14 GMT  
		Size: 7.2 MB (7197600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0160e88901926d2127b183b181259e758d6ac153ffa4c468a909848944d8785`  
		Last Modified: Thu, 20 Feb 2025 03:45:14 GMT  
		Size: 14.4 KB (14369 bytes)  
		MIME: application/vnd.in-toto+json
