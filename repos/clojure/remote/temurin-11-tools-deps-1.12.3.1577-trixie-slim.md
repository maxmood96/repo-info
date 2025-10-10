## `clojure:temurin-11-tools-deps-1.12.3.1577-trixie-slim`

```console
$ docker pull clojure@sha256:dda671fcde68e83457b03c6de9a6c0e2e86d806e53c0b29790cf06a6819f0785
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

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:99fcd00ae715644745066d832700e976ec2f219b676f3c8dcd94f7feae09e7ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 MB (250374889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76293da450965584a7d8b80f78f7fe02878fec6ef294f8c7b8a6862f3a540acd`
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
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52ebca87d00ad513511f98a44d8a7b243ca05daf15aa37aa83d2bd3b7fd2104`  
		Last Modified: Thu, 02 Oct 2025 09:29:11 GMT  
		Size: 145.7 MB (145658171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b12b09585ee927b1e975f5f988b80c586d91786cbb8eb73c39c919f1df9fdc`  
		Last Modified: Thu, 02 Oct 2025 08:58:11 GMT  
		Size: 74.9 MB (74938308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b2f18c647d07b6c0bc823429989d25aec05680b298f0ec61a1f4515f9feab5`  
		Last Modified: Thu, 02 Oct 2025 08:58:05 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b0dbb30c2abe76ce6559d612bc0db51c0e63d1c69fe45af403d560ec47740bde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5290594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4f8cf62ffb88fb869248a52d10e6fe6a0daca782ac22e06b478412542418a14`

```dockerfile
```

-	Layers:
	-	`sha256:5d9072f6bd14b3ac478ed518a94c3d98f4f9b7aad6008470721d3a37f97f8a75`  
		Last Modified: Thu, 02 Oct 2025 12:37:29 GMT  
		Size: 5.3 MB (5276308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f55185b2492603f83dd3d2b891706c74ca39082e8532ba9376b80370971fda6`  
		Last Modified: Thu, 02 Oct 2025 12:37:30 GMT  
		Size: 14.3 KB (14286 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a15c3cde13197866de758bfc7d80c47eed1961d4e31d08455df724c698d88d9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 MB (247724951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d08eb8405cc0c17bdc60790297d38a27e846b05a49965340690d4d5dec1397e2`
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
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1879f9e67d5360893a34b59e5d6cda10ef9daa0401f6dcd448fbb9837370ce95`  
		Last Modified: Fri, 03 Oct 2025 08:58:35 GMT  
		Size: 142.5 MB (142458700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7449b8c57b556c4b2b7770347d2d995a766bdb6659ba6009f9449da56484151c`  
		Last Modified: Thu, 02 Oct 2025 02:42:59 GMT  
		Size: 75.1 MB (75124763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad53adbd0768eadb1d248d30ebec76bc50fcb6bca6ea29ccd2b5bbf93d9ab614`  
		Last Modified: Thu, 02 Oct 2025 02:42:54 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:62a9451cb00f6de6f34a15dab41c75ed16923335489e1030bf8eb92deb97e152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299636163f18f72ec09fd05536b2e6ebb8b3bd60826b48aadb4de3d7d51de502`

```dockerfile
```

-	Layers:
	-	`sha256:f013d5ef4a306b87bbec5ce70eb17c150788fe0da7a79f92a6b21b89a936646c`  
		Last Modified: Thu, 02 Oct 2025 06:38:22 GMT  
		Size: 5.3 MB (5282695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:781928f3e2611a8b7165e962d7e6af4e3ad8358c107b835c705d02c9ab3474ab`  
		Last Modified: Thu, 02 Oct 2025 06:38:22 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:92abd4fbff326dac24b41de23f179f0a777eb62a07d66a2efc5488f07558eae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.0 MB (247040634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f573950dfe4e88b001d53ab152cbf7cc5276202beac06646bc5b4c4577793cf8`
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
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38963c60f58211f48adb1985b3e1972224f5ee978afbbc88f9d6a9e57994f84`  
		Last Modified: Sun, 05 Oct 2025 11:51:11 GMT  
		Size: 132.9 MB (132853300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e765a73acbb3348daf7f3804a154d52328ad786f05929d8f55c540a6fb08fc9`  
		Last Modified: Thu, 02 Oct 2025 08:41:29 GMT  
		Size: 80.6 MB (80588236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7558696ef75f20f9ea1b4ac59a442c2338c229c9c10925b23bf50fbd09981f77`  
		Last Modified: Thu, 02 Oct 2025 08:41:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bed4d4debece011e8435a37ebcd55cbb00e6703ba438db98d7548f29d8230077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5294398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ef350bf3616c3d51b1054f4576b8a4ad8afe56f34723a7effb9be59c74f528`

```dockerfile
```

-	Layers:
	-	`sha256:2ecefce08227f64136687347adde87abfcdb5084b5a6a88cc49e02838ca2199f`  
		Last Modified: Thu, 02 Oct 2025 09:36:38 GMT  
		Size: 5.3 MB (5280064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:313990a48bf9cb23d4c3928ea02d92dbbeb1075101aa442eaeab7a8f8069b381`  
		Last Modified: Thu, 02 Oct 2025 09:36:39 GMT  
		Size: 14.3 KB (14334 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:4dcce88ed2952a5c50f91b0ff0d4e2897d27f6a44114a48df17da82da9ce1cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231022562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:388886c630afb8aca49ce0c1059f4a6cc9b7041696191c42b1f55af8b24baecb`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
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
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e79b5900b5effeda4776d69d4a251c63021d33a0ee35fa09174f72fb2c2348d`  
		Last Modified: Thu, 09 Oct 2025 23:01:47 GMT  
		Size: 125.6 MB (125622160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e28ad475e5850d31559ad5a4a4fd8a122056358bbbcbb146901f63fc424b46`  
		Last Modified: Thu, 09 Oct 2025 23:07:31 GMT  
		Size: 75.6 MB (75562527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341fb9185caaf29f861e138acceb05af227fe4253b0af3fa7442eb60493a3132`  
		Last Modified: Thu, 09 Oct 2025 23:07:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ec7c30648c2b7946cfbdd52b9fabd7f67f873da8995c3d970b7daf693b5a2454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5286521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad25d428ba507bacee76b7cbef4221054c7f2eb97a3fec9a7f712eaa7a7d8ec4`

```dockerfile
```

-	Layers:
	-	`sha256:42e553ca624159931c3989469da2f188896ec5318d323b25eb4b32ea28f7fd8b`  
		Last Modified: Fri, 10 Oct 2025 00:36:45 GMT  
		Size: 5.3 MB (5272236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b500d9ed0593c91fdc203b5ab1f6e68d564230fde0674c83800ee3c73814cf9`  
		Last Modified: Fri, 10 Oct 2025 00:36:46 GMT  
		Size: 14.3 KB (14285 bytes)  
		MIME: application/vnd.in-toto+json
