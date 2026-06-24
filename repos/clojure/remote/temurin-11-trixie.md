## `clojure:temurin-11-trixie`

```console
$ docker pull clojure@sha256:d53ef9b2d3a4b570fe13a5590ba1553b02b4918e8b85b97e312a242ef395ae29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-11-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:e4f98f655620357dc33f20646dfdd298d43b1030890be15a94aec6d44ddcebcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277722032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e77872131e9302c04a2f0a65ae5ced2a6da9c35523d7582a4594fd64b919960`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:17:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:17:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:17:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:17:08 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:17:08 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:17:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:17:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:17:23 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:aa3e9ef32f73c30e8b065800ee66429992d3bfea6a1fb8224afdd878ab5b994f`  
		Last Modified: Wed, 24 Jun 2026 00:28:33 GMT  
		Size: 49.3 MB (49317255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01fa782e862ea408fcd07caf3c748c77bfdef043fffd5c1464a1c297280e8cb7`  
		Last Modified: Wed, 24 Jun 2026 02:17:47 GMT  
		Size: 145.9 MB (145886165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c20540051388ab892bceb84b8cb3065fbcfb9ca738071da665e038747c70b6`  
		Last Modified: Wed, 24 Jun 2026 02:17:46 GMT  
		Size: 82.5 MB (82517967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09d56dca245494cb3719589040ffebdea43594bf3d6f3c30aab5d66ab0a65ee`  
		Last Modified: Wed, 24 Jun 2026 02:17:42 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ac78ec27d7a49dc1f8a2b20abf6009fabf94f382299dcd15c9f20ddf1851751a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7502626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ed9065bd8e966867caf169a4d9ef129d66ba26073e2a1e788e41e412f5fc2fd`

```dockerfile
```

-	Layers:
	-	`sha256:92b6868e5145a50f05e1a3c3b3427ae8bb6279c3e82f7fcb8da5e8cb7c9f1789`  
		Last Modified: Wed, 24 Jun 2026 02:17:43 GMT  
		Size: 7.5 MB (7488287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f85b9238c52ba430a52bbef15a821446de82c3116257b804a56cebc093122d49`  
		Last Modified: Wed, 24 Jun 2026 02:17:42 GMT  
		Size: 14.3 KB (14339 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a11a222eadcdbfbd1e12d9e8f37d8bf3bdeed3541ca5549dcf0af0a6bbccd826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274599672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf425558acc9f4926e1d2aed6510fa7093da07d9c369d8f8b41d4eee22507f30`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:23:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:23:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:23:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:23:17 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:23:17 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:23:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:23:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:23:35 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c8a311258fd162f6aa0db134045a19154c81a2244ff9ed7620256c95ae5d6b69`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 49.7 MB (49678395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057a7e51871d1aaecc2d344b7742f8c7a03d65bf3009f96c6f687eedc96453f3`  
		Last Modified: Wed, 24 Jun 2026 02:24:02 GMT  
		Size: 142.6 MB (142582142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb9f468ab6bc679bb1f4fab6dc3fc5335e0c8e8576a5ebe9f94ea3a13b6b646`  
		Last Modified: Wed, 24 Jun 2026 02:24:00 GMT  
		Size: 82.3 MB (82338489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450cb7d507c1f34290036fc09da06d81bef74ec958e8de2159f627ed5fc44011`  
		Last Modified: Wed, 24 Jun 2026 02:23:55 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:04e4acaa5bb7669f61fcf574fbb9431b55d725bbef6318471804de527ef00f0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7509755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b1d4c26937a2c055fd05fabf16c29360c4a0134932838d79c71bf612edbf957`

```dockerfile
```

-	Layers:
	-	`sha256:76651b9ca84d045367aec4fdaa81fce397f3af28b3e58b9574f3b853e1216b00`  
		Last Modified: Wed, 24 Jun 2026 02:23:55 GMT  
		Size: 7.5 MB (7495298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:243ab3edb723f99caf0452c0bd365c24932fd54cd53a56a7de954742c672a709`  
		Last Modified: Wed, 24 Jun 2026 02:23:54 GMT  
		Size: 14.5 KB (14457 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:9251da36908ec95e913a28b393a3906c7416467de374d93d5128acd34cdb9a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274188545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ffd9856572a87ccaf85f2ef2e1d7269ce8c4346ed6992fd286b1b3792b5d58f`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 07:54:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 07:54:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 07:54:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:54:39 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 07:54:40 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 08:00:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 08:00:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 08:00:35 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:99b7058514c1f9221ac3b0625d731341802c32d464fd604a099ae71d3765bbfd`  
		Last Modified: Wed, 24 Jun 2026 00:30:31 GMT  
		Size: 53.1 MB (53138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f879e6c1229219e4a1953047919d9134485f69fd32ad7cb6f48d66146dd828`  
		Last Modified: Wed, 24 Jun 2026 07:58:04 GMT  
		Size: 133.1 MB (133110616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f878a131340d68543781d52a14713d9f0f3e89c973e123a344a359b70f858a23`  
		Last Modified: Wed, 24 Jun 2026 08:01:12 GMT  
		Size: 87.9 MB (87939215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e5810e74163a8a9caa02134345bb5e8543eca0726cd1d12e029741acba8622`  
		Last Modified: Wed, 24 Jun 2026 08:01:10 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3912dcb4914dfcd5b4b21594355042543d212706cb9305ef93c92f4d9b1ac672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7506480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c156f3696e3d3ded4cc28d01be0ba2602d69ea9a25aad5f304f0eb6adf8510c2`

```dockerfile
```

-	Layers:
	-	`sha256:22f7b8f675817358850cd46bd2ab92bd50d265aaa30b4f7d13c99d8b6e4fb4ea`  
		Last Modified: Wed, 24 Jun 2026 08:01:10 GMT  
		Size: 7.5 MB (7492093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8d2b258c759e102af8c5e2c400205d834a18a9d991d1236a84d76efab32147e`  
		Last Modified: Wed, 24 Jun 2026 08:01:10 GMT  
		Size: 14.4 KB (14387 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:3ea2cd8a090f8defb12633503aa6821fa498020d27c3ab81c578efaf19a2128b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.5 MB (259541198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc08e142c73699103a07a26404e9e7bf32083f6941e8cd4c72891af43798792d`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 04:10:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:10:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:10:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:10:49 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 04:10:49 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 04:11:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 04:11:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 04:11:06 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4acbf08d84aa74ba1f41a222ae6a061c228f6ba4fc5d1d428650c7427ca1fbd3`  
		Last Modified: Wed, 24 Jun 2026 00:28:42 GMT  
		Size: 49.4 MB (49386060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d13c196f0dfb7ae4f939a9af8cd21a77f243351205411c96ae39f6583fdfad`  
		Last Modified: Wed, 24 Jun 2026 04:11:37 GMT  
		Size: 126.7 MB (126652585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21aaa85833558323d2acf637a1a0ad4cff107800526ce5a9b43e1d54df8022f0`  
		Last Modified: Wed, 24 Jun 2026 04:11:36 GMT  
		Size: 83.5 MB (83501908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87033d67e2f3149b3fd59e52202b20e75731d407e18bf17d6f4e07fa482fc657`  
		Last Modified: Wed, 24 Jun 2026 04:11:34 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a93f041f26bdb1b7d3e5c4dcb2f819b5c891f78d12b7d7552cc3b4ce65d6370e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7498551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f818120593f7283c56653366fd081223542e669b9976fb3f981db5b33af5b5dd`

```dockerfile
```

-	Layers:
	-	`sha256:dec4594e3103385efed19b71d02be17b8a885e624d40d6f5a9baa6ed77fbbf11`  
		Last Modified: Wed, 24 Jun 2026 04:11:34 GMT  
		Size: 7.5 MB (7484213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db84fc2047b6aed4324f4b05eedf65237ac5c96eb6c3909e3d33a8f917cf675e`  
		Last Modified: Wed, 24 Jun 2026 04:11:34 GMT  
		Size: 14.3 KB (14338 bytes)  
		MIME: application/vnd.in-toto+json
