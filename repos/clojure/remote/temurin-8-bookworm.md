## `clojure:temurin-8-bookworm`

```console
$ docker pull clojure@sha256:f1a59776a1475b4d45275331d06225152a7b213b674a05d087a406b0e54566bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:1656686516aa8f6f77eb19b6727642796970b7994c78f9785334bfd7dde4089f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 MB (233475948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3201dff2da2cd86b294666ec873ed77e92f11aafa3c1ec049324efcb69e4ce5c`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f28176026b7610ed955787195c16f28a97a6e54b94da8ea7264f6d643d8806`  
		Last Modified: Wed, 05 Jun 2024 06:10:01 GMT  
		Size: 103.6 MB (103600229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ccb12b625db845f19d334b6e82045e6305f0f088068da7ef0176f2056c8f5b`  
		Last Modified: Wed, 05 Jun 2024 06:10:03 GMT  
		Size: 80.3 MB (80298681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a1d4b488c65ecb0af4424366bdd521fda04d0ef1b57f898e4f8afcc05cee98`  
		Last Modified: Wed, 05 Jun 2024 06:10:01 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ce5e7594bb3187ca595e5edaacaec8453570d69b47fb8d8b5de4251e5f98ea0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6996956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103ec60b33019f4669a67a45b329c22c6e0d231d6c376f123e50752c0ccf7184`

```dockerfile
```

-	Layers:
	-	`sha256:491dd50f52d001717f20225146fe67bc17495d176e126afc3ed3173bcd43db04`  
		Last Modified: Wed, 05 Jun 2024 06:10:02 GMT  
		Size: 7.0 MB (6983154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:927010bd102c7c7cb8b769d2623ba708a14fdbf41c24f428043357ca1a4ea399`  
		Last Modified: Wed, 05 Jun 2024 06:10:01 GMT  
		Size: 13.8 KB (13802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0e472da22e5f2a8a2c8908dc1a2544832ec0d173e0778045bd9b807a7d104687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232358197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b6b1fe4c43f57c00a39e0f94f3afb78d1c677bb5295b27ad91dc472fbd83d43`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 00:39:32 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Tue, 14 May 2024 00:39:33 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1bc72e2cf79426c46f7a4c1a51ed600705fe1718585f2c93199289349ffabcb`  
		Last Modified: Wed, 05 Jun 2024 13:31:09 GMT  
		Size: 102.7 MB (102700399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb954973d9febd32ae922ff843234e595f7141043a30988d984a6b5fdc9a3a49`  
		Last Modified: Wed, 05 Jun 2024 13:36:32 GMT  
		Size: 80.0 MB (80043762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966e2db3c83fb05dcdddfb7d49d71d8c63ec5494430e09c6bc130fc01a0def72`  
		Last Modified: Wed, 05 Jun 2024 13:36:29 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0d3e0f0a3004dc02d6a96b4074387504e6c8c47bd8ed3c9905a0ac0b59d29a90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7003876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695b68ff4dcc0f9319f5450a382001c99ec3f0912e9f0782d5cf051023782aea`

```dockerfile
```

-	Layers:
	-	`sha256:87988e189f4d5ec508bc8e20c6f5f25de41faacfef18fbd19b19d2d4c74f4bcf`  
		Last Modified: Wed, 05 Jun 2024 13:36:31 GMT  
		Size: 7.0 MB (6989541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2801bc72dce6c9de179cd2729941d55e7a03aeac14579b2332ebf14cbf8895c`  
		Last Modified: Wed, 05 Jun 2024 13:36:29 GMT  
		Size: 14.3 KB (14335 bytes)  
		MIME: application/vnd.in-toto+json
