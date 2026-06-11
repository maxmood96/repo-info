## `clojure:temurin-21-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:f7e33b7ec0b817dbea02c9246942496f33a3d86877048bb504876bed6ad56574
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

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:13954373eddd7a5eef98d9d7323cb57d2016f3be5e445e72caf01e01ae2feaaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (253048278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8c87834aaedadede3485de864ee2457e3b3b5d309c7bb3143b7741da7dae03`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:19:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:19:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:19:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:19:59 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:19:59 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:20:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:20:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:20:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:20:13 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:20:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d9d3f8415db9cefd6920d25ac4841b76ccbdde939a8113eaaf86d5b75e93f9`  
		Last Modified: Thu, 11 Jun 2026 01:20:37 GMT  
		Size: 158.2 MB (158166906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fced615daf5da062b879ceb1e93bd6b9ee3a4e6d66674f7f7f1c8a6cfc4afcca`  
		Last Modified: Thu, 11 Jun 2026 01:20:36 GMT  
		Size: 66.6 MB (66642706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434ca7b1ea8f77f9e743184c68b57e534bfd8a71cee2d5b156880f8f1255d3a7`  
		Last Modified: Thu, 11 Jun 2026 01:20:32 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb99499bd7442f22ae3f6774ed4ad966ec73534fe3b3ae74a6c041f7e86de89`  
		Last Modified: Thu, 11 Jun 2026 01:20:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6521aa1b218e9351279a03eef7f0e6cfcbc8df39231e952f0a832b24f22e88e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5131840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ed50bec9e818a03b259183094db085d8d570031ca249da348178152479de334`

```dockerfile
```

-	Layers:
	-	`sha256:d9755caa7340dd324b388ec7d5770e86888c714081d44301dd1eb5ab76c251d7`  
		Last Modified: Thu, 11 Jun 2026 01:20:33 GMT  
		Size: 5.1 MB (5115851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:269674ab69736a563548658c1810fb3354a9b566aac37c647e08a02b6e9bf9dd`  
		Last Modified: Thu, 11 Jun 2026 01:20:32 GMT  
		Size: 16.0 KB (15989 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:69242a2603b9294e580f2decd569ed88cd8c765f14ec35866f16fb87eea6811e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.2 MB (251227858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb1ec75410a011dcf0f6868d3d2588d2550d8c2d9ef2db83dda9c03e3fced4b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:24:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:24:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:24:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:24:00 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:24:00 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:24:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:24:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:24:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:24:14 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:24:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f229ea76cb5551ea185e36b37df4e5e6485c0684a3829a27a10fb428cacc251`  
		Last Modified: Thu, 11 Jun 2026 01:24:36 GMT  
		Size: 156.5 MB (156461285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bc94b52b2b397972150f0f944ebcb96d1a3c90d35ba9add42da55c1d7638fc`  
		Last Modified: Thu, 11 Jun 2026 01:24:36 GMT  
		Size: 66.6 MB (66643227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780914cfd2be7c9db08f004f0176a1636bee851b178f954310be76942ef73110`  
		Last Modified: Thu, 11 Jun 2026 01:24:32 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a5c29acaad97abffff1ef20d96218a5b7c0a7ffbb669e1310618e6eb8ad817`  
		Last Modified: Thu, 11 Jun 2026 01:24:32 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b07e076f0c70f3b6ffe1745a97e9d9d3d0b8160cc24ac6a237c04cd7f1456d28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c8dd390bda93e32da5bf08c1cb32106d2c0ea0f105e2cf303f64ad49ed1597`

```dockerfile
```

-	Layers:
	-	`sha256:e55273a548296de77533b5b8184d5e4eb8f9155d0d88d1561013ae0a5e85b28f`  
		Last Modified: Thu, 11 Jun 2026 01:24:33 GMT  
		Size: 5.1 MB (5121612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fad166f3493778370add3c7eda6581eddcc54edbe7d9e11dbaf72a53d1ea5e8`  
		Last Modified: Thu, 11 Jun 2026 01:24:32 GMT  
		Size: 16.1 KB (16108 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:bae30d340c6d598630ac37424d54205fd5774925a79efd14928b6ef740e74ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.9 MB (262902313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bc8530d5d15dd1dcd283cce96554b03c685151f1860df9077a124ea4b8e5bb1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 09:36:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 09:36:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 09:36:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 09:36:58 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 09:36:59 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 09:40:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 09:40:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 09:40:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 09:40:56 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 09:40:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:23f7cdee3ef2598b081c2b848fee95730a7ab2b1cc5b726c72dcb8c2fe3632f7`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 32.1 MB (32081941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce7fc17844961c443ec6ff9fc6852d7315d0c5de57330a5cd0dd3369a5a4e22`  
		Last Modified: Thu, 11 Jun 2026 09:38:13 GMT  
		Size: 158.3 MB (158343198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3c118b9f7d05886df50211fa5ca5a5a4944fea2436355a07cf5990fc3f4050`  
		Last Modified: Thu, 11 Jun 2026 09:41:30 GMT  
		Size: 72.5 MB (72476139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de26702f265ec61b5b340c8e112e88c7e907ce086ba644669904d5e7cd3c0e3`  
		Last Modified: Thu, 11 Jun 2026 09:41:28 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681205b8f53e6b29dba3fe75db85e8f63da8106c1ef9cb5ae7c244a03e489d02`  
		Last Modified: Thu, 11 Jun 2026 09:41:28 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:528b08bf2923cf9abd34589b170d646f64e6874935249dad14f5d3a91d2f3a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5136092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a362e2c6731ee95bf83e86cf56896cf03a46f9dc3ffe6f3fcad162adc569767`

```dockerfile
```

-	Layers:
	-	`sha256:5d1dbfc598eab94be88eac202573cdd5db54965f2284498b236303fb6bb901d2`  
		Last Modified: Thu, 11 Jun 2026 09:41:28 GMT  
		Size: 5.1 MB (5121009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:135491b3784d0ccd2a04c5c655def3c588e44fdb00ae6011218e413c1fd90722`  
		Last Modified: Thu, 11 Jun 2026 09:41:28 GMT  
		Size: 15.1 KB (15083 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:f2af2b986573e813058c17abb04559ee833254d2a4c054badffcfdb211163df8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.7 MB (239735126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed0487258c4a9f69d182691297137b1d09d222860b57c4ccf77a3dc99005ba7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 03:11:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 03:11:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 03:11:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:11:05 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 03:11:05 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 03:12:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 03:12:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 03:12:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 03:12:28 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 03:12:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315e35399e5d4547db2084583fbe80262cce5f385bc84081f625e7edec4d8b6b`  
		Last Modified: Thu, 11 Jun 2026 03:11:50 GMT  
		Size: 147.4 MB (147388354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2433bb9e19d43b9d0d2bb8468768ca318365cd3777d75dd84c7a7502643322`  
		Last Modified: Thu, 11 Jun 2026 03:12:52 GMT  
		Size: 65.5 MB (65452226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83f64e0df30172e41778d10cfccfa6e5b89de0063331c27e84faf1b9878bf95`  
		Last Modified: Thu, 11 Jun 2026 03:12:51 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47080ce1fe4864e6b3085f82c8145683bd9f1053def52593773e73bb254a6a8b`  
		Last Modified: Thu, 11 Jun 2026 03:12:51 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f4ed1939465607af5c3fd8eb6a7ed320425efc7989c0567edbf1a4201e7a618a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5122206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44950e9a7094b07000ae4e34db952cda9275a860ff6658ff4260476a0877e9b0`

```dockerfile
```

-	Layers:
	-	`sha256:3641dba4be0443db1e0235f9ea568b01a8839b5afa62edbf6b43ab3185bcabc3`  
		Last Modified: Thu, 11 Jun 2026 03:12:51 GMT  
		Size: 5.1 MB (5107172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a19c931c5eddc342ca6a79509a732ad84d5c68607c08e367c4f1c66912edb319`  
		Last Modified: Thu, 11 Jun 2026 03:12:51 GMT  
		Size: 15.0 KB (15034 bytes)  
		MIME: application/vnd.in-toto+json
