## `clojure:temurin-8-tools-deps-1.12.4.1612-bookworm`

```console
$ docker pull clojure@sha256:fe8959e444671ec6f431ecc1412e07e7f1df6289fabe23417caa513f0b9685ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.4.1612-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:5b51e2439100273c6e7e49eee85831964fbe7be30ded69e034beffad5792cf0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.8 MB (184836375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dff267caedfa6a9f25e1fdb66ff11482a27fbc4a9a315c07b994e95e3f83280`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Wed, 04 Mar 2026 17:48:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:48:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:48:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:48:39 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:48:39 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:48:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:48:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:48:55 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a4789b6607bb64f31399bd1cb159a67b022139e962c425d85e8ade037018ef`  
		Last Modified: Wed, 04 Mar 2026 17:49:15 GMT  
		Size: 55.2 MB (55170068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d83fdbd81dc4d64198bec7de4e21776459aa403a08f6850e949483a6271710`  
		Last Modified: Wed, 04 Mar 2026 17:49:16 GMT  
		Size: 81.2 MB (81176886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84926d755589f056ac8fbfa47c0ec040658fc5892d6bd9257a82c4bd0a52c25`  
		Last Modified: Wed, 04 Mar 2026 17:49:12 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1612-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ed868b227c52770a0f6f4bfb9be05ffd5e323d199c308e940e1e683f8c381c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346e3cb0de92aa177309e6c202b2d41150420367239b5e1cb7fd333983ae723c`

```dockerfile
```

-	Layers:
	-	`sha256:261aecfb3dba16e876e3cd0a082e7b3e6f59d458c1390c9285d09d70214d41ef`  
		Last Modified: Wed, 04 Mar 2026 17:49:13 GMT  
		Size: 7.5 MB (7499289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e22deacf035d987226fb0d1bdfe50144659c9682d5336ba659844d77c524a86`  
		Last Modified: Wed, 04 Mar 2026 17:49:12 GMT  
		Size: 14.2 KB (14194 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1612-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:34d36b6cfcc3f9bab31b91bd4236474af942265ccb365bff3e23f95e01d99f57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.8 MB (183783420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f05cea3c48f7f70fa4a015ba8852836a24de794ae95fc5a9ed0dd3f388a3eb5`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Wed, 04 Mar 2026 17:48:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:48:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:48:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:48:12 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:48:12 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:48:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:48:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:48:28 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013d4cfde79c12f10fb7eb43087aee5e00f6e6179c228a7a7e55c48118de06fc`  
		Last Modified: Wed, 04 Mar 2026 17:48:47 GMT  
		Size: 54.3 MB (54251620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ad0740e7e4df560b36035f153786fc8ee936d39ac033262e1aa66ac2c6cf16`  
		Last Modified: Wed, 04 Mar 2026 17:48:47 GMT  
		Size: 81.2 MB (81157947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d71b83a1bb3b878cbfcc1f0b7a489b5c88291fb882e3067309a337bf39040b`  
		Last Modified: Wed, 04 Mar 2026 17:48:44 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1612-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:185d6b53317d9282694d85d04bbb7ff1fc22f8485e46d15739322950ead5c753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7520063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927a53673e5eb03a8864fcf9465d14af56efc43f8db5ef51cf5498ba0b9810d9`

```dockerfile
```

-	Layers:
	-	`sha256:6e8faf2e1e5da7ac01d478c1255150eb462ec34ec9e678a6fa375f2f28da9ae6`  
		Last Modified: Wed, 04 Mar 2026 17:48:45 GMT  
		Size: 7.5 MB (7505752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b95a565078842f85551220daa079c9d258e972075bf9d9c5776e1427e9640dcb`  
		Last Modified: Wed, 04 Mar 2026 17:48:44 GMT  
		Size: 14.3 KB (14311 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1612-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:8625cd9370766eac8baea549a283c7cbb13b8eb2bc9fe1fb0a4b520490678150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (191987671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac7a049797b279488d770448a11c752aa046194f4f78c60f90e8be2fe3810efd`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Wed, 04 Mar 2026 17:46:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:46:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:46:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:46:29 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:46:29 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:47:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:47:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:47:23 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c87483c04549ca1f8af23b64a504890762706ca023e75ae627b0893b8723d8`  
		Last Modified: Wed, 04 Mar 2026 17:47:59 GMT  
		Size: 52.7 MB (52650380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daff325f1ea86d38adcd708a5ff5f06b3706d202d59bb1da27d1af8da994bba`  
		Last Modified: Wed, 04 Mar 2026 17:48:00 GMT  
		Size: 87.0 MB (86999846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357067375d1731ee5e820df0e72285bffa6855ed7ca68b5bb24e506e4cd898e9`  
		Last Modified: Wed, 04 Mar 2026 17:47:56 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1612-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0732ae8ae895d6b93a0693a531faf54280238200c636907a73edeb3c4a927a35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7519342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6109ba6ef5383780f6e53a690dd7f4a8110bda0543458179b885c65db1d04ecf`

```dockerfile
```

-	Layers:
	-	`sha256:3d65900d79c9d4d15698943bca1848398a3d7f33491b3ef7ad70d618f4f1bdab`  
		Last Modified: Wed, 04 Mar 2026 17:47:57 GMT  
		Size: 7.5 MB (7505100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aac98ea14a6352d2c97972ccfdc410469d0a609ec0a952103fb4613a558ab60c`  
		Last Modified: Wed, 04 Mar 2026 17:47:56 GMT  
		Size: 14.2 KB (14242 bytes)  
		MIME: application/vnd.in-toto+json
