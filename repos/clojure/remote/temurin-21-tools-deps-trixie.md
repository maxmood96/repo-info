## `clojure:temurin-21-tools-deps-trixie`

```console
$ docker pull clojure@sha256:cfd210b5d42d3e8e34c0d51b768a3bc2c55d864c5ec4bd4a3cbffac589289503
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:170df37cee239df0a4fa1f5f6cf199bed36c3e907aa79e0d1486f8d44bce6ee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292633356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89882b2ae37bea48ed7b32b8eeb18080f6706b2375ee716fd3a757a0e132e028`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:31:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 04:31:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 04:31:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:31:24 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 04:31:24 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 04:31:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 04:31:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 04:31:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 04:31:41 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 04:31:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2f4cb1d25f72fb916a05a4f87374b214338c1916890d35cd4686e785f74a25`  
		Last Modified: Tue, 04 Nov 2025 10:57:21 GMT  
		Size: 157.8 MB (157804765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f7e108076b70c2718c16675d2f66dd509f42a3bb1f8cdcca8dcc43fb935632`  
		Last Modified: Tue, 04 Nov 2025 04:32:18 GMT  
		Size: 85.5 MB (85541926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e5c1eb038ab6511fab03daa945fdd8269677a6b9b0c57c9b5d5cde0b574bf9`  
		Last Modified: Tue, 04 Nov 2025 04:32:09 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5214ef93f0dcda5e93fde9bd50b94f62cb29332cea941bda6da8dad8dc7b6f58`  
		Last Modified: Tue, 04 Nov 2025 04:32:09 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:58a8870a99d55b25da8818e1e7b60c4efa086fd3543a389e3cd20fbc1d9c92c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7485754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfaf441261ab034bae0472bc1f0020a27b989023200f555c7022d612469fe624`

```dockerfile
```

-	Layers:
	-	`sha256:c20b4d2b83a21d26b6922d95a7b27f63413a7310c6e72b87c5d93609084192f3`  
		Last Modified: Tue, 04 Nov 2025 10:44:33 GMT  
		Size: 7.5 MB (7470001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee07f5aa67f6dbfc0047a660778f9e51bac9b7c5b39d92bd7485470d45556bcc`  
		Last Modified: Tue, 04 Nov 2025 10:44:33 GMT  
		Size: 15.8 KB (15753 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c7c38df61c1ea6b9cca0c8bff8b90a6f05067dfa50720613d824efd41d8a9144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 MB (291096153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2168aaf079798dead50caee9b34fa518495c0475cd75b843f2d785d8f40507`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:45:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 01:45:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 01:45:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:45:19 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 01:45:19 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 01:45:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 01:45:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 01:45:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 01:45:37 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 01:45:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fa134ee7f4812ba368741835d72896b409fc9f20146a933419b76b18d0e213`  
		Last Modified: Tue, 04 Nov 2025 21:26:17 GMT  
		Size: 156.1 MB (156081258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bce4b23f265deb67e2d6b0dc969fb1a344011f39f70ad54913e17f9d56a5a58`  
		Last Modified: Tue, 04 Nov 2025 01:46:15 GMT  
		Size: 85.4 MB (85363423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a8e4f4a9910382cde659e7be9e9742a7a9b220ac0672852fe9fdb5be7dc7d6`  
		Last Modified: Tue, 04 Nov 2025 01:46:05 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44012217264db98186b751ea3960851d3c1c3c17ad728b6253b455d512a0576`  
		Last Modified: Tue, 04 Nov 2025 01:46:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:775d4515ebac20e0eb6d4ca01c6367745058a3e60731960510951886949c3de8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b1c4c89eaa3771897d684d16c5019127995470356b370a05c5c5cfe54017564`

```dockerfile
```

-	Layers:
	-	`sha256:4bfd0e7f11f1bb80ed8824e06c0ee3863af1683b6195b50a573d4c28dd43c86a`  
		Last Modified: Tue, 04 Nov 2025 10:44:41 GMT  
		Size: 7.5 MB (7477031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6553fbf5b3c9520252e08d56766a9e47d202d101f7ec41fc2e523c8f49cc48fb`  
		Last Modified: Tue, 04 Nov 2025 10:44:41 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:9ac7d001eed07a9861984664e6d829444bf632a15aba319ece1ddb58826ec230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (302024380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd02ff1158a98f2cebd2322758d6964a0e85995c7ac23787307c0d19bb3fcd47`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 13:35:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 13:35:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 13:35:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 13:35:42 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 13:35:42 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 13:42:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 13:42:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 13:42:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 13:42:14 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 13:42:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3c335bb15935da0eae5ce30111cfa6a289c813162bada9fd389d8ae5510d5d66`  
		Last Modified: Tue, 04 Nov 2025 00:20:22 GMT  
		Size: 53.1 MB (53110127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8603f9efd678d7e42bb5392a1026619d0919c9539d7c56b601271dc48ce60b5`  
		Last Modified: Tue, 04 Nov 2025 13:37:00 GMT  
		Size: 158.0 MB (157963427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b7199156a396f0379a9e0e9ad6124937adfc2cac3cd4e7fa8712d80f30db35`  
		Last Modified: Tue, 04 Nov 2025 13:43:17 GMT  
		Size: 90.9 MB (90949782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11d47270178f318bb5d664f8e0ae53caea5f4c50927307430f3323d3f2ea29c`  
		Last Modified: Tue, 04 Nov 2025 13:43:06 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd69a874417af3c712ce8bce5f130eb31530c262b2135f3ae00e43d61754518`  
		Last Modified: Tue, 04 Nov 2025 13:43:12 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:111173eacfb51393a6e898f712e50aebe3a1b119f4a2ff4ef56e6103eea7becb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee026e985b894a57e039ad397fe75920023fba69b6e20879f91563078308d4a`

```dockerfile
```

-	Layers:
	-	`sha256:fc526cfbfe26dae829aef68c9038ebb99bb37e38714d33f89a9ccd804a3d80e4`  
		Last Modified: Tue, 04 Nov 2025 16:38:59 GMT  
		Size: 7.5 MB (7474420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c935fc6d50c37e7699d039e971aba27af0cb57057816135c6d3153cb1e903b0`  
		Last Modified: Tue, 04 Nov 2025 16:39:00 GMT  
		Size: 15.0 KB (15001 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:e0764df59ff5f4b682ede3915a6075dbe545ee77ffe90e5b0d2202e3b1ebed3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285792160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4090e291ce22eef833cd319b64ecdc5de25866640f4193cedcb7aeb7b42328`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Fri, 07 Nov 2025 06:33:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 07 Nov 2025 06:33:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 07 Nov 2025 06:33:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Nov 2025 06:33:03 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 07 Nov 2025 06:33:03 GMT
WORKDIR /tmp
# Fri, 07 Nov 2025 06:48:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 07 Nov 2025 06:48:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 07 Nov 2025 06:48:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 07 Nov 2025 06:48:41 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 07 Nov 2025 06:48:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:de6b66e2abcf55248485e438d6def9b92cf28773b7cd7896ee78f9409b6e7526`  
		Last Modified: Tue, 04 Nov 2025 00:27:48 GMT  
		Size: 47.8 MB (47770924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f02f73111e105921cc185c6c33251c2d50b1703e0a326d71d528fa31b308a9`  
		Last Modified: Fri, 07 Nov 2025 06:39:09 GMT  
		Size: 153.6 MB (153593539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7191924e2dd042f142e99450efa2052df9d3595617cf9b749da5ea9b31e7785`  
		Last Modified: Fri, 07 Nov 2025 06:53:51 GMT  
		Size: 84.4 MB (84426653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc317734523252362c3c2f97d12ca0ab646ee7398d56a95eb02fa33b7f72ecd`  
		Last Modified: Fri, 07 Nov 2025 06:53:38 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281345e848ffad065672d9621ff7809d52c4f5ad9731de7f76bb3a0ef1de5ac5`  
		Last Modified: Fri, 07 Nov 2025 06:53:39 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b4c8206c44b8c77280089e734d4b82af3bbab2db275157bf4f4265e347977671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7473716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081bde84061250f5ca44720e12bdeb34280cd12faa2aecefbc182be0af031b3d`

```dockerfile
```

-	Layers:
	-	`sha256:f6850d6cf84bf0261ccd268538b4d7c9fc5d54f2704a5f80b3311df37651dedf`  
		Last Modified: Fri, 07 Nov 2025 10:37:25 GMT  
		Size: 7.5 MB (7457914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55cb847077b7586d97b532f0a54cfa7a141a216ba176970df135f2db21c563e3`  
		Last Modified: Fri, 07 Nov 2025 10:37:25 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:252e3fe3438cac14df71d2cbcfe493f0d45c4cc321c38930869fefd513d34a00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282888910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8920ffca7b99706d26e47379c475404643c2ea5dc7d421c309eebfcf57556d3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 13:04:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 13:04:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 13:04:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 13:04:15 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 13:04:15 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 13:06:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 13:06:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 13:06:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 13:06:32 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 13:06:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:48bd359f940d437208e8579c571291503fa327e04a66a6c8d918cfe93cae2e1e`  
		Last Modified: Tue, 04 Nov 2025 00:19:45 GMT  
		Size: 49.4 MB (49352299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8cb87dbc56dd0ceec8ade80dbf4a583ffd88c64721f2008d818d3b7e00891ad`  
		Last Modified: Tue, 04 Nov 2025 22:42:08 GMT  
		Size: 147.0 MB (147026991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb80fc6e462775d805bb7d466a99726f29e02214186bdbba1148dc8c0a3b1fd`  
		Last Modified: Tue, 04 Nov 2025 13:06:58 GMT  
		Size: 86.5 MB (86508580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c67eaa3eb1f8e09e6ef5a4212a65f94320608dc77a9ca868fced2aaaec3a879`  
		Last Modified: Tue, 04 Nov 2025 13:07:03 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac30b33de786a5c1a240753b1ce2e81624227c27aed4b382b30af18ebad86e4b`  
		Last Modified: Tue, 04 Nov 2025 13:07:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2d8736051b29244f1d79d5d5b37107933e03f80f19bdca2ad1800f5dbc492a89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7480876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad76ce242eb55813edd1638be7d6b532e1a391d069a9d8265dae44deee51665`

```dockerfile
```

-	Layers:
	-	`sha256:c98e9cbc2a453bc27948b6d94e1a38cb09049a031e372e39675c7e96b78b37c3`  
		Last Modified: Tue, 04 Nov 2025 13:37:38 GMT  
		Size: 7.5 MB (7465923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ba7e5e75fc1a8a36e5a4f51a8487834418ef16ed0aadc4da51e5a03113d5adb`  
		Last Modified: Tue, 04 Nov 2025 13:37:51 GMT  
		Size: 15.0 KB (14953 bytes)  
		MIME: application/vnd.in-toto+json
