## `clojure:temurin-8-tools-deps-1.12.4.1602-trixie-slim`

```console
$ docker pull clojure@sha256:0394ba31d318ddcf28de3c418e10d7a55e5503ed3bf20e1fb5750cdee05b2eba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.4.1602-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:efc59db4b29ce084a70ce60f9a14d59a725ae8413c0e0f24831d2a458503437f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156944955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93ea19d0d0503aae995916345013e17027e331d214420a3adfb92379da1f6a1d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:01:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:01:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:01:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:01:34 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:01:34 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:01:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:01:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:01:50 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd0ecd915c6467940228f67cdf1d9cbda8291afe8004f27a5161306c7fcac93`  
		Last Modified: Thu, 05 Feb 2026 23:02:10 GMT  
		Size: 55.2 MB (55170164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3cd9dcd51e2d0afe0dc907dc86bdc6d05534c9e75204324a286a02d41bd271`  
		Last Modified: Thu, 05 Feb 2026 23:02:10 GMT  
		Size: 72.0 MB (71995549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76a05a33e8d1f38eba44e365f7fdc7b34046ffa6e36752d2343f1b40297a5d3`  
		Last Modified: Thu, 05 Feb 2026 23:02:07 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f42220972752b7e3e0596bfaf7f3286282171f053a7b820be51765cfdf0f2fb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5392766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c618ef36077fa257ac108d9aa77f7b0b184dfee83d820aa7569c04e75885a2e`

```dockerfile
```

-	Layers:
	-	`sha256:41bd83ad682bdd496b95d41418f2d92c984c27b02064ad895625d5369202978f`  
		Last Modified: Thu, 05 Feb 2026 23:02:08 GMT  
		Size: 5.4 MB (5378538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3878ca7084af167c939207d0900100c5f902362245ee65fc2a0eeae5aed0424b`  
		Last Modified: Thu, 05 Feb 2026 23:02:07 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1602-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8fb7770042b3bcc13701eb415e82172dcc7af16745c639d2fdf7b1b2f466313f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156198973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df1117c052753058ce5d649030799c4dd38531a1feeb46b7393e9914c52d4a14`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:02:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:02:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:02:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:02:52 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:02:52 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:03:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:03:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:03:10 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7b160c5fbf7b6aeb134db9bfa5aa4440fb200b255018ab23ff2259ee2afcf2`  
		Last Modified: Thu, 05 Feb 2026 23:03:28 GMT  
		Size: 54.3 MB (54251638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01d6077a931f03cf5aa2a612ecef14b97e6387678628770b6cfa07b5f0db4937`  
		Last Modified: Thu, 05 Feb 2026 23:03:29 GMT  
		Size: 71.8 MB (71806624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2ec8eee40f7ea82bd3ebc209dcf5009c2d6f6d8ef071c9960c5967c21b824c`  
		Last Modified: Thu, 05 Feb 2026 23:03:26 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a001cf00c3509748f8bab212e3c11def953e51a943ee37c6b6fa32e071b6a088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5399353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9c31ba71e75d44c4214bb5829e285f015725c6fa98e315e3aa821cf90549926`

```dockerfile
```

-	Layers:
	-	`sha256:edde1beab10265e1320b7f2932758fa1d7eac7df2666c8e444548243bb3d0041`  
		Last Modified: Thu, 05 Feb 2026 23:03:26 GMT  
		Size: 5.4 MB (5385007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7109f80c6a29b4e6aee6af423333a69ce0b46f6444c87d3ec79c3a08d916b04`  
		Last Modified: Thu, 05 Feb 2026 23:03:26 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1602-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:91f0d0e149e4d16d54ebc074861c9c57dea17a0e30702ebc9746c34a09babc8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.6 MB (163641758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2664422fe25744d74aa4c7187c585f55d35bc9cd78de34b3e24b56811fc6c979`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Fri, 06 Feb 2026 00:00:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:00:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:00:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:00:11 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Fri, 06 Feb 2026 00:00:12 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:07:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:07:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:07:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e89dcc3b95f00f17f7b2d6872744c6220cb1fbbd573cd216d9413691c73b51c`  
		Last Modified: Fri, 06 Feb 2026 00:02:21 GMT  
		Size: 52.7 MB (52650394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ccfc408e8ff54ba791a45ce0440d8c1e26e720d22e4eaf8ee74a5fb7f0f675f`  
		Last Modified: Fri, 06 Feb 2026 00:08:51 GMT  
		Size: 77.4 MB (77390534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26c858ae7504b91d032e21c47b2803e68ab2e6aacb9b231c2363351a693b12c`  
		Last Modified: Fri, 06 Feb 2026 00:08:49 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7c525aa42f361a02faa7c3b1be9b71b337134687f26cb083d1208b94cd6d223d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565e9ead29647a58810ab4eb876d7a26f976f5e132fad779658aa4dab86a50ac`

```dockerfile
```

-	Layers:
	-	`sha256:8a242450eeeacba4751e9d00ed92234a66ad768fdc9729fe1ca5df82d5ff84d1`  
		Last Modified: Fri, 06 Feb 2026 00:08:49 GMT  
		Size: 5.4 MB (5383504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4f15d0eeaf67385556c42044b5b28bc49a25b85e81ac75ff1c21f9ae74ee5cb`  
		Last Modified: Fri, 06 Feb 2026 00:08:49 GMT  
		Size: 14.3 KB (14276 bytes)  
		MIME: application/vnd.in-toto+json
