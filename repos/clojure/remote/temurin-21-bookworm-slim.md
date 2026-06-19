## `clojure:temurin-21-bookworm-slim`

```console
$ docker pull clojure@sha256:77eaa95eb36a2194bc265c7b676d180dc5259894f78971e571a6248bcd9e1a61
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

### `clojure:temurin-21-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:99dff225cf16c5a1384084baee7570e682512aafc9a70999ebf0705c3cd9ba52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (253048046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7e67fa6f6bcb60f8b4666236f9074d6d96b0ce34790d592ad7771fbe69253fd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:18:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:18:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:18:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:18:38 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:18:38 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:18:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:18:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:18:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:18:51 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:18:51 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb83578017e0914790039f15bd963f381fbd903bbd2aea91a0a431d1d14f72c`  
		Last Modified: Fri, 19 Jun 2026 02:19:13 GMT  
		Size: 158.2 MB (158166921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a44529c0040793383c33aa9b213e8f07b14af14e0e66cab10d438fa9e2cf037`  
		Last Modified: Fri, 19 Jun 2026 02:19:11 GMT  
		Size: 66.6 MB (66642458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a06a410c9e1e19da2185673ef2b0b3f4def2f8bb4445878f1e755b21351c913`  
		Last Modified: Fri, 19 Jun 2026 02:19:07 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b739eb39fcd3fdcf85e4710da5706e75918b8f386339fdf8e884b02b02297f26`  
		Last Modified: Fri, 19 Jun 2026 02:19:07 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:db73a57b8544fb9e8289ea5a9f24378a2f68b7ede8c3a0a54ae6fcf4954fc7f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5131841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46a77ce29e54d65bf2ab3b9ba26a7bdebd676df13a0d22468ac7539e35f23365`

```dockerfile
```

-	Layers:
	-	`sha256:440b3e1d388b9c7d8e600af5c36d0e4edff15fc00d6ce8580d05d1209d18093d`  
		Last Modified: Fri, 19 Jun 2026 02:19:07 GMT  
		Size: 5.1 MB (5115851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d341447c4efc1c88fa5d7f358eb3aa43fc905e702043deca852dee2c7102f46`  
		Last Modified: Fri, 19 Jun 2026 02:19:07 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ddf09e52a131fb775659c5b5e03d39ce6d9f779fd39ca9bafd4b720bafc23307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.2 MB (251227268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2f9c1db2d3a267a4a4f6c9d91f906baa409a5a80d51014f20c2ba9a0663262`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:19:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:19:06 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:19:06 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:19:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:19:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:19:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:19:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:19:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb63de71613b0ee95a71b2390ea662e991a4523125ce8fd3b7f353b29e010096`  
		Last Modified: Fri, 19 Jun 2026 02:19:44 GMT  
		Size: 156.5 MB (156461328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcf2e8ac21081ac44604f84aed55473ff67c24c28f07bc181e5c30c13fcb4d0`  
		Last Modified: Fri, 19 Jun 2026 02:19:42 GMT  
		Size: 66.6 MB (66642595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd7e36dd3ad3922d60167df681659ee2ddf250c29a824feb16befab5fa56e98`  
		Last Modified: Fri, 19 Jun 2026 02:19:39 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d66dc6adfcf173fde5997b5dc308d714f2809d4e1bc5e11e31f61cb2321780`  
		Last Modified: Fri, 19 Jun 2026 02:19:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:09e13f5f5a6fabe97fd1cba339807d916a7d8006e27fb8ce2d31a1734975b66b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7f85a6013b998729bbe5d63eb45c77ac701252eac15ea983d3a4a9d5dd6bb18`

```dockerfile
```

-	Layers:
	-	`sha256:657bf033e434a4b5e4f87531d7b4e7b4d7cbd544033d05cf56268307fba8a685`  
		Last Modified: Fri, 19 Jun 2026 02:19:40 GMT  
		Size: 5.1 MB (5121612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3d16896523cb56bd03e5ee0748b71e96b5228bc4abad52cd9d5f757c0edcd07`  
		Last Modified: Fri, 19 Jun 2026 02:19:39 GMT  
		Size: 16.1 KB (16108 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:f3d589adc3b50bdc0d58b9cb86e4ccfb4911c97d13122af437e22ed98474bdde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.9 MB (262902574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d19030bc6cf6250cee62cb0758c9fec2810da67c54ae82a2c66aa7d2fcae5ae6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:54:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:54:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:54:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:54:22 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Tue, 16 Jun 2026 23:54:22 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:51:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:51:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:51:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:51:05 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:51:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:23f7cdee3ef2598b081c2b848fee95730a7ab2b1cc5b726c72dcb8c2fe3632f7`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 32.1 MB (32081941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e41ba91bd198088eadb03a3c25545d904cf2490691f50cad346a585a8741f3`  
		Last Modified: Tue, 16 Jun 2026 23:57:21 GMT  
		Size: 158.3 MB (158343240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae475647756fdd153bd9f29c0b8fabad9bae8f5197003de852c2e27e784ce0ab`  
		Last Modified: Fri, 19 Jun 2026 02:51:43 GMT  
		Size: 72.5 MB (72476357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7437237bf82753108a524dc96421224eefb13579517ad60befe7f4d018c188a6`  
		Last Modified: Fri, 19 Jun 2026 02:51:41 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b24fb6e9645776f5efc2d1cc8924ab2688b027e5cb7462b8cb788c684c07a5`  
		Last Modified: Fri, 19 Jun 2026 02:51:41 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:db76ab1b21a5d191c112bd989057ea703dc73a367e66a6b668ed86d86bf019f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a314bc9a603e020025ba65368649a3b676013361d68578d6f3a068ca917c3e`

```dockerfile
```

-	Layers:
	-	`sha256:595fed261c96145907bd11eca1b9e2e6a6eca405db10b20e1dc57fa3d509693e`  
		Last Modified: Fri, 19 Jun 2026 02:51:41 GMT  
		Size: 5.1 MB (5121009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13e709df68e31a921de4870276af022d6fcf44aab7259d12cd4d9bd612ab286b`  
		Last Modified: Fri, 19 Jun 2026 02:51:41 GMT  
		Size: 16.0 KB (16037 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:e7ebe4bd6e0065c404dd8e2ba18247fc989088e150506efc490611973e488ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.7 MB (239735033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d15df63bf79db63aa65942fd9ef51911a62653bd8d36f2239224cb99da294b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:36:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:36:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:36:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:36:47 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Tue, 16 Jun 2026 23:36:47 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:20:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:20:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:20:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:20:19 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:20:19 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7c23db7ea29bb7aa16742bb5f7f37601f5b9a0301d0417f6608ab147d6a0ad`  
		Last Modified: Tue, 16 Jun 2026 23:38:27 GMT  
		Size: 147.4 MB (147388339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611671cc9fc8d153994aaf3d80afee434541de7f7d4c74d43060c5266022918c`  
		Last Modified: Fri, 19 Jun 2026 02:20:42 GMT  
		Size: 65.5 MB (65452145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3979b6d27880b7f6e518d21212e43e0de1087ddd5766601f99b56c68d17a245`  
		Last Modified: Fri, 19 Jun 2026 02:20:40 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dacee03a157af71a1a689766cc213a3947c43d53d2883ad6b69cf43b3553868`  
		Last Modified: Fri, 19 Jun 2026 02:20:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a2d35441ef8a8b84196b8db0b5f9cd2f9d3dde9211b9749710e04c2a457ff6e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5122207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7886aae06a4f8310a2ca3ed1ba2f21afbedf84d0c64875dff435d5cd9095bb51`

```dockerfile
```

-	Layers:
	-	`sha256:69a740d387a38e7121db15ee1d81c4bf53ca1347fcf2287170c02294b19c4f85`  
		Last Modified: Fri, 19 Jun 2026 02:20:40 GMT  
		Size: 5.1 MB (5107172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96fe41019e8b793f7faa67f36fd0a695e590bba97a1007d7f55b9d85035e2b2c`  
		Last Modified: Fri, 19 Jun 2026 02:20:40 GMT  
		Size: 15.0 KB (15035 bytes)  
		MIME: application/vnd.in-toto+json
