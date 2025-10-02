## `clojure:temurin-21-tools-deps-1.12.3.1577-trixie-slim`

```console
$ docker pull clojure@sha256:7e5bf81cc50c2a903bb0920b3cadaa3c368c2a6784972b591264c590984662e4
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

### `clojure:temurin-21-tools-deps-1.12.3.1577-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:dd0de22baf7dea393da598b6962621d9d102c22b0ff4f9f6baa10731b35504bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.5 MB (262522441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:570e8320948f33f67e2239abc45eea812d57a27eefef28dc937bca3714290524`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7735751dd61f687069bf32d41727e3e2197c427d3e9a7670f08eb09e6e4383`  
		Last Modified: Thu, 02 Oct 2025 09:00:48 GMT  
		Size: 157.8 MB (157804830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0662fd7bf5c43ebdd6b54c6c0ff779c9ffcf73480dc1a71607525c790d227c3a`  
		Last Modified: Thu, 02 Oct 2025 09:01:09 GMT  
		Size: 74.9 MB (74938805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcea209291a2e75d3994c3cc6490cb555f12c318a6c084f00abad64d07907964`  
		Last Modified: Thu, 02 Oct 2025 09:00:59 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbdba96018fdb3f6ac7c55d04d821f48aa1130f2647dfc990fe3a90369c0cb2`  
		Last Modified: Thu, 02 Oct 2025 09:00:59 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9ced929d1731e349be36010d605f182db63b25ceac14273c5292bd2b9ced3d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9126659e7e324fbb80c86409f3dbe16bdf8ae17464ea4d06d6066e1ede862937`

```dockerfile
```

-	Layers:
	-	`sha256:b0aa6fa133e48f82641fae6919f69ed8110f168d911d03f618d43f5254e01b6f`  
		Last Modified: Thu, 02 Oct 2025 12:43:20 GMT  
		Size: 5.3 MB (5259269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2f6ccf1ec6364ad9af86ad48cebf978c9fe0ae5190198da087f09ade67d2dbe`  
		Last Modified: Thu, 02 Oct 2025 12:43:21 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.3.1577-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f3ab4f453ee60dabc0f4ad4076c02bd981b7adaf10edc544f41205bde9c987e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.3 MB (261348283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:175adf385ccd34a70f9c569f204e2959db0c98bcb4e9f99f9fa418ab30c90d4f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c71fc27b3b52869ec8eed570f304367f7de8f596bf195cad368294135a0b18`  
		Last Modified: Thu, 02 Oct 2025 19:16:51 GMT  
		Size: 156.1 MB (156081248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbe18c72f192a64b42864de8edd05e98ce526960b8a3e4321ff649dc5a8db7e`  
		Last Modified: Thu, 02 Oct 2025 02:46:26 GMT  
		Size: 75.1 MB (75125155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff618cc437e4b93895c9388abb694627d34bcd0a5f70c901cc75e19933d0d64c`  
		Last Modified: Thu, 02 Oct 2025 02:46:23 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9fd8ad33be6010d3e4b868b19cb3a2e8a47e73b0ac8c3efb7a609fff3a3aa3`  
		Last Modified: Thu, 02 Oct 2025 02:46:23 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:24064e27bc269bfe6ace230592171e50b38ebb5f8ac0098ee0ffe297bef2593e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5280209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e28b606d38074938a969dea0c0ee7430c283b5c3f6df24e3daa5ab856884ecfc`

```dockerfile
```

-	Layers:
	-	`sha256:56e2e5cf2d51561391f06038a89e55a514f71d77e3ed9e24e5ca8067bd7b1310`  
		Last Modified: Thu, 02 Oct 2025 06:45:21 GMT  
		Size: 5.3 MB (5265038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0df1d797ec5c3c76514cab10a1299050fd5c7e3ec4d61a2c03b470bd8d6b91ed`  
		Last Modified: Thu, 02 Oct 2025 06:45:21 GMT  
		Size: 15.2 KB (15171 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.3.1577-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:2db5674f7d635b4a925555c48d77efd865647d07f7c7680c8f50429ec7bfc7aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272151093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:064e183d56889b86e31deaa70789277a10a8ccb409c1bbd04da0566c8e3c5d3c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a57ffbfccebb44fefcd7b1c31f53e3f4e6047cdb4893843ade55ff60b7c712`  
		Last Modified: Thu, 02 Oct 2025 20:37:44 GMT  
		Size: 158.0 MB (157963428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60c6205eaed18b5905234b19c866225df9c6cf48600b0c3c172439543d79bf7`  
		Last Modified: Thu, 02 Oct 2025 09:29:45 GMT  
		Size: 80.6 MB (80588169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da363b5a418dd6a765d8f6c92a06e10acc6e9444c5a2db947cc79f16f6e4f494`  
		Last Modified: Thu, 02 Oct 2025 09:29:59 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b321506559621645b95822947cb474400e3cc06c1af46c3425402948520bfb4`  
		Last Modified: Thu, 02 Oct 2025 09:29:59 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b5935f18e8622fa707b90d6ab050ed887eb4d701e2ab8c1603defd9a7b6f3e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13e27ef11518eb7f2929d5b57ddd0e2fb292e2ca766ac9c907c53b473ac64caa`

```dockerfile
```

-	Layers:
	-	`sha256:c7fc6e494e5f78ade74d00465e48fbb96bcf8a10d583270f239afbc6601a323c`  
		Last Modified: Thu, 02 Oct 2025 12:43:28 GMT  
		Size: 5.3 MB (5263640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba499e1bd4202e643826696e962308d3098b9730df909df656934e623406eb89`  
		Last Modified: Thu, 02 Oct 2025 12:43:29 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.3.1577-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:8f0638980a34346987ccc3e6c0e9bc28457cde0666f8511b95427fd935455a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.7 MB (252746926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7010361391da66739ba133336048d7531923a371f18396f81045a8a610a1a8d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:dd4e3fb8766f676c414c0c55be0f5d9f6e6359dc2628caa804016b0f2ba461f2`  
		Last Modified: Tue, 09 Sep 2025 01:07:45 GMT  
		Size: 28.3 MB (28271372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25be0a32c196b5e86daa223045b0e32e55940405ffb33be6fe5f6bd48aeeeee`  
		Last Modified: Sun, 14 Sep 2025 19:26:07 GMT  
		Size: 153.6 MB (153593492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad65798ac3af68bb3d796da257a0138854ff669ee25377b5c0c648e9bbef733`  
		Last Modified: Sat, 27 Sep 2025 00:47:33 GMT  
		Size: 70.9 MB (70881018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dadd4cea2a07fe4570727784cb847ea0f0a240bf0462cd20c2d11eae1490fb2a`  
		Last Modified: Sat, 27 Sep 2025 00:47:26 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7d9cf1957104da57f9801eefa7be4852302482f90cd81afbdfb2432c4de08e`  
		Last Modified: Sat, 27 Sep 2025 00:47:26 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:803bbce4b2ad2abcf02e3dbf846df2d44ce596183694890ff5f8153dbec97b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5264582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aae94893d2a1785c3cf25f358558d14df2123aa906839d01168fec7da164042`

```dockerfile
```

-	Layers:
	-	`sha256:9c0244d422b3ecbb16c67ab330781b0db89388dbf320e2c40fe5a73007a80e60`  
		Last Modified: Sat, 27 Sep 2025 03:36:50 GMT  
		Size: 5.2 MB (5248679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b6f2325cf600513400ff9d10485f9e3bb7fb94e5a95ecfc1267b97f3cfe466a`  
		Last Modified: Sat, 27 Sep 2025 03:36:51 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.3.1577-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:16cd8b987f23c4973d123d5848b4060f0597f61c8fdcbc6ca13498ff0b9b45b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.4 MB (252428410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3142712bb02a52fb82e2eba1a646412aa161870b8650607559beddf96c3e9440`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5ba71f67252a0f4d16e2d9e3d46396c7535298113149842edaa2e394beebe8`  
		Last Modified: Thu, 02 Oct 2025 04:46:49 GMT  
		Size: 147.0 MB (147027015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52ed45eaa092067199dca5f21c132a443fece6e6a5eade703859068453de6bb`  
		Last Modified: Thu, 02 Oct 2025 04:53:18 GMT  
		Size: 75.6 MB (75563125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0797147a241e6b80559055118f61d129beaf709a426bc9eb74f9b3cf1ef9005a`  
		Last Modified: Thu, 02 Oct 2025 04:52:57 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5827ec4e13772349f93c3556b9c5b1ff743c00166eb8e918fe72903cbefbdaa`  
		Last Modified: Thu, 02 Oct 2025 04:52:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a95957e7bdf229ba7f28811be0646c0f0648e29ea20462e002e4d0c3abe1bf90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5271048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b6b458486d114959d12cd91a44c54e90d8bca8acae4040bcd7f2a188b545346`

```dockerfile
```

-	Layers:
	-	`sha256:860cf32395438ed2e453e05875c41fa339b55fc03926b75f6981f17b9fcfada2`  
		Last Modified: Thu, 02 Oct 2025 06:45:32 GMT  
		Size: 5.3 MB (5255193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c943e090e13de10a7124695e92d502147011358d2c7e48c7d0eab4d87a41027`  
		Last Modified: Thu, 02 Oct 2025 06:45:33 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json
