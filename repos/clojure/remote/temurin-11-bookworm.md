## `clojure:temurin-11-bookworm`

```console
$ docker pull clojure@sha256:981f84460b7534ba5719118ebdb0c417dd2f66cc3c3ba5c3b6f39ffb06e7da45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:02afb265e8b4c249b37f522e9f43723d7ac700a87900773ba8e076b4a295d94c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.1 MB (275059883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:035d1a79a3bf7bc5b1dddc9331aed741c5e074a440f13d0f7552488c778257be`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c9473a0733c4ff12727c983146546f26461261c6c2e36fb2a46a3b69cfd7d4`  
		Last Modified: Wed, 22 Jan 2025 19:42:33 GMT  
		Size: 145.6 MB (145601464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d0093a647e7a973aa2e122c0973d52f523538e1a6a4017cb623cdf363c3293`  
		Last Modified: Wed, 22 Jan 2025 19:42:32 GMT  
		Size: 81.0 MB (80977812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29c9aaaa6f9534308600f2e4c3b0449fe12f75956dca3cb8a0fabe59291f1ea`  
		Last Modified: Wed, 22 Jan 2025 19:42:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b4f5dd08960ac0c0c33770bb5f4db169d5fa7af481882aefdc8895cb24951c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7205471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36598708ba234ecdd29e7ee06eeb37950785c213df67fcf48bffca7b1f127c00`

```dockerfile
```

-	Layers:
	-	`sha256:d1a6996f4562f562fd478e5b87c011a72b8a87d67d1e01ca2e9b99f567451881`  
		Last Modified: Wed, 22 Jan 2025 19:42:30 GMT  
		Size: 7.2 MB (7191219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7e7c6f5658ce20ebfd0cabca9b6a154ae5ad9d7a1a07d7659fe509f18697004`  
		Last Modified: Wed, 22 Jan 2025 19:42:29 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3141b7563ca9f11baedf0e3198cbd599bf6164fa7147e0021c0de950eaa77d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.5 MB (271522678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8653563fa07356f98bba47f09819f0d6d3f0728ee4fd8ae9dbe22988d43d6a56`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e26ee9a41b1f3ed7214ca9a70f8e4f943b0205b19d4b46842fffeca87f50c45`  
		Last Modified: Tue, 14 Jan 2025 12:20:13 GMT  
		Size: 142.4 MB (142389012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f3c014d7157555335e8c509e92758c14660e25f81a007e9437ed79c324aa06`  
		Last Modified: Tue, 14 Jan 2025 12:23:46 GMT  
		Size: 80.8 MB (80826127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daca4338f8af026177e8c41986e79e86ad5cdd029c04dae9cec4fb741b0ef69e`  
		Last Modified: Tue, 14 Jan 2025 12:23:44 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:671ae66a405da65736ce35744a43207da64d3dae216ded11f60c798ecdda9d74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7211970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1606991c724d1d42bdf4fdc3652c3370428cba5b761ab1cc38e8b3bcb753a0`

```dockerfile
```

-	Layers:
	-	`sha256:ac8a6b32371e57ae2288641aad83877356ec26b6720d0c8917decaf9358095bb`  
		Last Modified: Tue, 14 Jan 2025 12:23:45 GMT  
		Size: 7.2 MB (7197600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c67f49e2994b05dc17439cc925909c118cb9d7af468020902dea69018a767dc`  
		Last Modified: Tue, 14 Jan 2025 12:23:44 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
