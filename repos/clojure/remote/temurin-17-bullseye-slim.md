## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:4715d4099ac885703c309a820bcf2df21cc95416633f27d7655c00117322dfe0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:53df20395f8e00802285542c1d43564fb46ee6b3d9e16237e5d0bad554a7874f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234244103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71f957410e00ae74c5c7630c6c084b248595e712c44be823f48a9e13a34f9fdf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Wed, 28 Jan 2026 18:04:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:04:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:04:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:04:42 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:04:42 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:04:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:04:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:04:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:04:55 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:04:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bd1b97a95a10ded4767bfcdbb3d042b961d107d141121fdbb255239f0ca115f4`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 30.3 MB (30258497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4289994a77e828f49eb75ad121be08260b3fb931587461ff1ff32315abfd2b5c`  
		Last Modified: Wed, 28 Jan 2026 18:05:16 GMT  
		Size: 144.8 MB (144847973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe37ed0fe6b13ad9af10ecf19df86d66989c87ce46cb2dac18697b1a3c08a59`  
		Last Modified: Wed, 28 Jan 2026 18:05:14 GMT  
		Size: 59.1 MB (59136589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd5189f23ad8f5b801729e9ac60e0a6ca0431e992e6ff77dc9367b9b1f8fa83`  
		Last Modified: Wed, 28 Jan 2026 18:05:12 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119177714d8831b6ffa48b3bffafcdeb09d7b802cd39de07e7481f404023d2e9`  
		Last Modified: Wed, 28 Jan 2026 18:05:12 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:554cbdd141d91a81a1b30a76a522b833de3748a7bafa4704f46de11daa06ac4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5324702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a7f034d34e7c004ed3dcb9e84e91dc25007043e5adbb38fff6498c4a0f15888`

```dockerfile
```

-	Layers:
	-	`sha256:d0d8897aad1a8663090de6f333f541fc3784ffb5ff51d15bef98759f90a5282b`  
		Last Modified: Wed, 28 Jan 2026 18:05:12 GMT  
		Size: 5.3 MB (5308868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4af2231703046b34d6498731433902937b443f1a298383a31f9e79b34787cd6`  
		Last Modified: Wed, 28 Jan 2026 18:05:11 GMT  
		Size: 15.8 KB (15834 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:329790500d2926d06a6f9774e63300b1d35d7eb63dd09ae8aaab9fe881dff0ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231717683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec2922f48e9f89e1dd734bf40aa3488cf6cb6e86b03962108821fc8309b5d1b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Wed, 28 Jan 2026 18:04:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:04:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:04:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:04:14 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:04:14 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:04:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:04:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:04:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:04:29 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:04:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:51 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bd383b92dc3a5ad6e303f259e027f5de3c5d2399df069006d0fc711d466a4f`  
		Last Modified: Wed, 28 Jan 2026 18:04:51 GMT  
		Size: 143.7 MB (143679942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8194add1c0ef0c097b112bec4bd98d8e831004343a1aa93b599370b39521998`  
		Last Modified: Wed, 28 Jan 2026 18:04:49 GMT  
		Size: 59.3 MB (59288183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaabd8676fa1a28d095b7e0c6891aaf0bea72c31174276aeb3a7ed27c2b4804e`  
		Last Modified: Wed, 28 Jan 2026 18:04:47 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3168a7c4cda350cb421c96dda39e4c3d256eefb975c03c0c79850a7de75efec`  
		Last Modified: Wed, 28 Jan 2026 18:04:47 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7ef84a9e476dacb4c823bc483d4f22997ab431fac45e3c35d5753b2aa5bb7dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5330554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:facdc24fa5678b333a2638e33f22fdbd04736b3d7aa78a6cb75198a19217c5cc`

```dockerfile
```

-	Layers:
	-	`sha256:73ec04b1d1f810423bdd1858cef68cade0fe13b52b65713ca92db9d35695ce13`  
		Last Modified: Wed, 28 Jan 2026 18:04:47 GMT  
		Size: 5.3 MB (5314600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1df6c00654c9062fd582b59c05532e60cae86763bf42a1752b8a146bd2282ba`  
		Last Modified: Wed, 28 Jan 2026 18:04:47 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json
