## `clojure:temurin-11-tools-deps-1.12.4.1602-trixie`

```console
$ docker pull clojure@sha256:e3fcbb6629128c1a9972f60f09ac02ccc4f693c520627a457d21219e7978ef62
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

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:879e3c6839da869220c8aaf73881edbb1fe7ff5c7651f14fcc2ebbabb9848282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 MB (280642616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33941e40fdc1801e42adb421672f169de99cdbd7effb6186381cf361e6839bbb`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:03:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:03:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:03:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:03:28 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:03:28 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:03:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:03:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:03:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168eb8a483a0e241dad1aecfa07135e2d8dd688192036684aed560a738ec3177`  
		Last Modified: Thu, 05 Feb 2026 23:04:09 GMT  
		Size: 145.8 MB (145806917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fd9c1073d3512d0c98133b91e92ad613004f33e8b96ce67eeffd4c21d36eeb`  
		Last Modified: Thu, 05 Feb 2026 23:04:08 GMT  
		Size: 85.5 MB (85542100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ed679856687e33a73fa2f50318f9ffe9084e9f91d0f75691b740af3c99e755`  
		Last Modified: Thu, 05 Feb 2026 23:04:05 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:10f49613c9dbb5950f431e9a18dff7315e692dfea3f825fc66f43497c2c37b97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7503406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee87db87e203a33f8c2a268b3086260588121c37ef1e0343b0bbaf40f0a609d`

```dockerfile
```

-	Layers:
	-	`sha256:dee3e8b9959e319d968450e846dabef156db98c38d7a2f4b1ac8643093b27a3d`  
		Last Modified: Thu, 05 Feb 2026 23:04:05 GMT  
		Size: 7.5 MB (7489221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ae2f42ece3ecf0653bd91e8b31a7b1ebc9b47ae5c99c39615612975e33d06ce`  
		Last Modified: Thu, 05 Feb 2026 23:04:05 GMT  
		Size: 14.2 KB (14185 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9a1fd0d5e9d73b707218a425ada42b833a85048431f1e057eec4a9b663c483cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277514825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3a0ab37704b7c1e83cbb9b341b87c90a6acfc8922cebee7928c13e043ba318d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:04:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:04:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:04:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:04:36 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:04:36 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:04:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:04:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:04:55 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cfa245cbd971e07e39d7912952d78ee5acc9f08587cd0c1eaac6a2e2e8bf45`  
		Last Modified: Thu, 05 Feb 2026 23:05:19 GMT  
		Size: 142.5 MB (142500849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642268b849bdbc20f113c3e02064be01b70ccabb5f37d01d2055ca1946f1ce50`  
		Last Modified: Thu, 05 Feb 2026 23:05:18 GMT  
		Size: 85.4 MB (85361311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd5e0ad99b5c56085d8468a67c5bea8221f0b32882b63ae9e815baa15269335`  
		Last Modified: Thu, 05 Feb 2026 23:05:15 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e25605dae7b87a397f08da6a11b37040868744fda9f9ac09638e5662d68c7890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7511172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09296700bb8f90d9b4dc29aee5d199089909a00e56aa7dcbc3e55d3ef3b9a2a7`

```dockerfile
```

-	Layers:
	-	`sha256:bbc0c141ac982d99024ac516e71c88daf8e16e9f8ae2927f98432041aca81743`  
		Last Modified: Thu, 05 Feb 2026 23:05:15 GMT  
		Size: 7.5 MB (7496869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3092ac75fb1057f0876e1d36de1ed93dca93b2aea67d8deb56c5d836d490c8f`  
		Last Modified: Thu, 05 Feb 2026 23:05:15 GMT  
		Size: 14.3 KB (14303 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:70c870d4271c77a3f8921befd17141271e61e6c499d0360ee00dbb3e58eaee44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.1 MB (277057564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9a10a2d99b401123c253a03db26222ebee48a1ba7b4e87f346ec21b098c4c0`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Fri, 06 Feb 2026 00:12:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:12:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:12:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:12:45 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Fri, 06 Feb 2026 00:12:45 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:20:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:20:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:20:42 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6397fc946e64e7714633f42a4de42b00c617e66212cd1a0b61df76767b81f868`  
		Last Modified: Tue, 03 Feb 2026 01:16:36 GMT  
		Size: 53.1 MB (53112115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee9196ca82c2237253cd105f74ebc47ce2f1292126825ec1d20ea1c7d414806`  
		Last Modified: Fri, 06 Feb 2026 00:14:35 GMT  
		Size: 133.0 MB (132996872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e024e82bf0bc590f479da75c58204f68a472492986758f364e5a5aaad89edb9f`  
		Last Modified: Fri, 06 Feb 2026 00:21:38 GMT  
		Size: 90.9 MB (90947931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a00461762e732dd9a7c785d70131169dea21afd790eae11a6eabc7f42638eb2`  
		Last Modified: Fri, 06 Feb 2026 00:21:35 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8408599e9b14012c4085df54c8323dccce464da1b451c145d199ecb6d736d362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7507260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f3c6864aa9569d16498ffb52e3cbdf3235f857dea6f0cf0af8e4a233f3d193`

```dockerfile
```

-	Layers:
	-	`sha256:a9150e2107caa1d553de9bd32ac1c6dd60c2806dd7177cebdf16735ec42bebbd`  
		Last Modified: Fri, 06 Feb 2026 00:21:35 GMT  
		Size: 7.5 MB (7493027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49c46609e82fcfb4ea465a0a726963e8d4ea1a278c5495acf5d7334bf6af9ee5`  
		Last Modified: Fri, 06 Feb 2026 00:21:35 GMT  
		Size: 14.2 KB (14233 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:e3f736994f451fc9556e7d0a1db2b2563895641f4e0fc3d92421ffe7a0ecc16e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.4 MB (262428882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeff5c2fb242559d7d0a76b3c1faf2d6aa3814997239bf72e90d62259af339af`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 22:59:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 22:59:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 22:59:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 22:59:27 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 22:59:27 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:01:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:01:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:01:17 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5578086c4ad67b3331d31c74c0b8aa3d13821b75ffa03070b0c1c80fdba7ceaa`  
		Last Modified: Tue, 03 Feb 2026 01:14:13 GMT  
		Size: 49.4 MB (49354378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23b198bbce5234d6c6418a67ec8420254720961b6a7485c3877bdf6aa827e27`  
		Last Modified: Thu, 05 Feb 2026 23:00:19 GMT  
		Size: 126.6 MB (126562163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb901e006e0651108703dec363c455e66ba91003c195885d0eab4b8b0a3bc323`  
		Last Modified: Thu, 05 Feb 2026 23:01:46 GMT  
		Size: 86.5 MB (86511696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edef4f528420060ad7e8bcafe5dcc7451548e430329f51795225d3c7b4967b2b`  
		Last Modified: Thu, 05 Feb 2026 23:01:43 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d58a1e7fa544edd8d7ebd52278cbaac4added2872b66c63490cd376c187dcd06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7499332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e1b4b1137af842bb49de55931d0612354a3e12bb88bbbd9ae789cf8c1dad080`

```dockerfile
```

-	Layers:
	-	`sha256:1278649031f88a2a042804ac8eec567c3411fc52fb8349891c6dbf330c78e449`  
		Last Modified: Thu, 05 Feb 2026 23:01:43 GMT  
		Size: 7.5 MB (7485147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d4242bae066870d8fc727932cea2a1bee2e2297fd68422326359083c5a7a8ac`  
		Last Modified: Thu, 05 Feb 2026 23:01:43 GMT  
		Size: 14.2 KB (14185 bytes)  
		MIME: application/vnd.in-toto+json
