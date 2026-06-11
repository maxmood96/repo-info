## `clojure:temurin-21-bookworm-slim`

```console
$ docker pull clojure@sha256:c966ed8e85d60722bebfbed4b686940407ce62cc7ce409b5d0586eac9e134df7
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

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-21-bookworm-slim` - linux; arm64 variant v8

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

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-21-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:60840c730c093a9fab30de697ac9ddf80b1ecac28b04a659ab52a002482f822d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.9 MB (262896035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:270a27238e41d53672abaf580703518af115aa7f89893085edc9b3caba396dd0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:58:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:58:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:58:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:58:22 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:58:23 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:59:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:59:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:59:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:59:04 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:59:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:562cecbb5aa529d280e58ef1f95f14cdcd37a90c5ea9181798a78377e934e6e7`  
		Last Modified: Tue, 19 May 2026 22:35:14 GMT  
		Size: 32.1 MB (32075742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026b5eac1372c58bf17e99c04c649b61fc2e6adc57b3b9da967a8850df068955`  
		Last Modified: Thu, 04 Jun 2026 17:59:55 GMT  
		Size: 158.3 MB (158343224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a4920934f69428ad5a43a330eca4bd9648bc599970c677d452276e6407909c`  
		Last Modified: Thu, 04 Jun 2026 17:59:53 GMT  
		Size: 72.5 MB (72476025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6656ba49bee3ed3b52da83c445ca5a27598396025d3e473739a2bef99afd9dad`  
		Last Modified: Thu, 04 Jun 2026 17:59:49 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ea18a6c09f4ecd6408aa54a7fbe3cada6a924a69270aeff2de05b90023272b`  
		Last Modified: Thu, 04 Jun 2026 17:59:49 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d16985462be4ac7b897170bb75559ac2e7a9a6fcc9f0f2d097cc8dafb1aa849c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b08d61d7f4a7847abf63385e27dff3e56e79e81a2219e058a3b5109dfa1edba0`

```dockerfile
```

-	Layers:
	-	`sha256:63588ec93a920f90f03a7d2bfff6c913e43bc823f1b1fca3098910dc3cb0e610`  
		Last Modified: Thu, 04 Jun 2026 17:59:50 GMT  
		Size: 5.1 MB (5120991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcb28b631b50cc4fe2f69cf47052ab0bd878aff6b67a9caf64fd28c2db1c9ea6`  
		Last Modified: Thu, 04 Jun 2026 17:59:49 GMT  
		Size: 16.0 KB (16036 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; s390x

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

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

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
