## `clojure:temurin-8-tools-deps-1.12.4.1602-bookworm-slim`

```console
$ docker pull clojure@sha256:152d88ff9511beb405a34ffa4d451a6b0bf7e6b5a9996b5856a61ec3bc6d2ef0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.4.1602-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5aee653647a5a046d59a76a08fd2ffc31bf2e8a308c6e0ff4c2c1f01fac6f674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153085182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d920a37c49c3b0f22d4c7a455db7de2152cb5657cb49dd5254768fa401288c2f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:52:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:52:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:52:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:52:56 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:52:56 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:53:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:53:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:53:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d78fce1206ac2fda2e1842a35a7b1064c5515f38ee0d94eb553d3ca345a7a42`  
		Last Modified: Tue, 24 Feb 2026 19:53:28 GMT  
		Size: 55.2 MB (55170068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c693aa26e2c870ebf896baf6746d4de93e711c279a71a2aa06d849880bcbe90`  
		Last Modified: Tue, 24 Feb 2026 19:53:28 GMT  
		Size: 69.7 MB (69678191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa74829ed0368a0571d329b3f8a17a82fa0fa88dc5578e2f3d927a46508ec1a`  
		Last Modified: Tue, 24 Feb 2026 19:53:25 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:035f5e457f0adface6dcf8ccbc4dadaf6310f14bdd08b4b956ccd132147505ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6660c0140a97165b5d353abb2748816cf16e2a978b3b4c5a56eb218892584945`

```dockerfile
```

-	Layers:
	-	`sha256:f23e539434ad5b5d9607ea3b174b7031ad4d1573a8d8c15c051b109087fca73e`  
		Last Modified: Tue, 24 Feb 2026 19:53:25 GMT  
		Size: 5.2 MB (5235641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cefd32fab7887b194b638f1325987ee62d00312ed708c4f0596d8c0ece8869b6`  
		Last Modified: Tue, 24 Feb 2026 19:53:25 GMT  
		Size: 14.2 KB (14246 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1602-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6bf8943d008c5338b4bc6e1134b5553303c690225e2bcad1856d86542db38478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (152041072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd90904883fdef2a55b087bf9cbe3a06721f22c7a89cd116d50f2536ae018a6a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:03:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:03:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:03:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:03:16 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:03:17 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:03:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:03:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:03:31 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5efebc0063ab903aa1b94c2759f150e779c405e898766b5d7b6e979d09a1236`  
		Last Modified: Tue, 24 Feb 2026 20:03:48 GMT  
		Size: 54.3 MB (54251619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbae7c37dc254edce5f0e679ce13c4312542f11bb3ce3642e09e2ef3290ef54`  
		Last Modified: Tue, 24 Feb 2026 20:03:48 GMT  
		Size: 69.7 MB (69672729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429cb800c75186edb5560f39e05adf7c943bd26cf2d59724708b6d63864a642c`  
		Last Modified: Tue, 24 Feb 2026 20:03:46 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:80323ed705dd702ad4ddf9639d935a3b5ecb4543064d27ad3dc3ab20a014d533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5256467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d7c39db9bb916be5650727ac0484cd08c7c68a105ef66ee3d3a53612394a07`

```dockerfile
```

-	Layers:
	-	`sha256:57523d2fd4f613e4fdba0ac8f7c385a15cfaec0770b332e5f804215da89effb2`  
		Last Modified: Tue, 24 Feb 2026 20:03:46 GMT  
		Size: 5.2 MB (5242102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a02ff498b1dd77dfe4d55c68e1f04c91c3d2fb3c95048adc730972f85d0fda0`  
		Last Modified: Tue, 24 Feb 2026 20:03:45 GMT  
		Size: 14.4 KB (14365 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1602-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:2331d3346f1ff2a16a32a92d3f6d98e44ab4e110dd270434766bdc6733d52a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160243485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c669a8d93af827599ca91b2e74fd2ea3742cd29e51418367998f3c8b980da6ac`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Wed, 25 Feb 2026 01:42:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 01:42:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 01:42:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 01:42:23 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 25 Feb 2026 01:42:23 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 01:46:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 25 Feb 2026 01:46:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 25 Feb 2026 01:46:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3def25e912c223ee8b3899e5ca048b2439f856f438ac690293817fbc0291fb36`  
		Last Modified: Tue, 24 Feb 2026 18:41:49 GMT  
		Size: 32.1 MB (32078334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea2f1da9d19213630e76b4b1f91db09749f3dbcc124c3818bfc80ad54656799`  
		Last Modified: Wed, 25 Feb 2026 01:43:48 GMT  
		Size: 52.7 MB (52650395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b28ae15c27265bd4c1ab9ed4ced82295d3686e3e48c098d53aab2eb659ee834`  
		Last Modified: Wed, 25 Feb 2026 01:47:05 GMT  
		Size: 75.5 MB (75514113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae01b5a0c0f53131f8565b7c0f0c06764dc2fce21f93e1fac1c424a1ff12b62`  
		Last Modified: Wed, 25 Feb 2026 01:47:03 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d5631354daaa4c7486e924654e9c131089b1d56f5d876c79dd1705e2a4715080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227073b5935e51be3907c43e9a35ae6a72ffb33e10c818deb17302650df89023`

```dockerfile
```

-	Layers:
	-	`sha256:3bc09bcbb5fffbbd060d38d5f3984350e73136033375251d7d0ee5897828312e`  
		Last Modified: Wed, 25 Feb 2026 01:47:03 GMT  
		Size: 5.2 MB (5241394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870d20ee3563ba9659c8b9d5c1e12c80a6788a9d344ef84381dad5535669a221`  
		Last Modified: Wed, 25 Feb 2026 01:47:03 GMT  
		Size: 14.3 KB (14296 bytes)  
		MIME: application/vnd.in-toto+json
