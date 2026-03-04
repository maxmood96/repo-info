## `clojure:temurin-17-tools-deps-1.12.4.1612-bookworm-slim`

```console
$ docker pull clojure@sha256:a0d96c08a16571919585c1f9073b4b76835a6c1dab93c353dc4757d569bc9b20
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

### `clojure:temurin-17-tools-deps-1.12.4.1612-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:551f8cf9ff1fa611b3f1efe08df02af870cefdade49a67ea28d1d9fdb5b93e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243567312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be2d331fea754597e4ed7691d7fe235cd2bf83e764a70c2bbe8352631b497220`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Wed, 04 Mar 2026 17:50:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:50:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:50:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:50:01 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:50:01 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:50:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:50:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:50:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:50:15 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:50:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de409a93e9b0fd0588648d84387fae123b96abcb6814ec6ba76eeddeba139fc1`  
		Last Modified: Wed, 04 Mar 2026 17:50:37 GMT  
		Size: 145.6 MB (145628711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e51e2bbf82a26bfeb874b48427e9d1b9beda188f4c53c5ee6c0d8357508b9c7`  
		Last Modified: Wed, 04 Mar 2026 17:50:35 GMT  
		Size: 69.7 MB (69701283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ed4aac31a6e2f219d51f610bb379d3bfca9ad258c5506d698f35c836993552`  
		Last Modified: Wed, 04 Mar 2026 17:50:32 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825e7d1e8bd2144f78d1e2820e377d2bde6ad93cfc9c5d6bfd5e77fa9aedd199`  
		Last Modified: Wed, 04 Mar 2026 17:50:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1612-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9a5bac52a4d493d04dc2ee32583692ca7d0ab6231777deea31631f55b8533485
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ce3f12458a13bcf9b1f1904609c96dab71b27787b2e12734c3c0c9266e0ecc`

```dockerfile
```

-	Layers:
	-	`sha256:e2db1a25d168a2e5d528702470976b914ce936892dad3ae3b6f5c64ac3ec5288`  
		Last Modified: Wed, 04 Mar 2026 17:50:33 GMT  
		Size: 5.1 MB (5116167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2054d2bdc277421023631e7da5a6843b301717947132bbc1070e554aa5151747`  
		Last Modified: Wed, 04 Mar 2026 17:50:32 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1612-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:718e34a1b74f61091c18119c7198b2538a0ac458b649f3df1fc9520da350d6a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.2 MB (242242074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b578e044cf9cb6c087389ed9887a17e1c5cf74c67254536d260329f96f222f7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Wed, 04 Mar 2026 17:49:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:49:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:49:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:49:43 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:49:43 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:49:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:49:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:49:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:49:59 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:49:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8716e022554d023082455135b32da849affb97e66bfd05edc85c08648d673297`  
		Last Modified: Wed, 04 Mar 2026 17:50:21 GMT  
		Size: 144.4 MB (144436243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae967f5dd5a51c00fc7077b584b2489d6d7e2706f272ef1ee8e6fa0789bb1e95`  
		Last Modified: Wed, 04 Mar 2026 17:50:20 GMT  
		Size: 69.7 MB (69688707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10e47bb825b457a4e81732cb3a46a0f25708deaddc79d13e6d6339c2f312c92`  
		Last Modified: Wed, 04 Mar 2026 17:50:17 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40c27db285493c4f09f789864f440b7420e0f3be40b7d0ab4c518f67579b39c`  
		Last Modified: Wed, 04 Mar 2026 17:50:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1612-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e593f3c2e6a08fd19c26cd2ef86bba669948104de2e62066e01164790e60e8db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1070caa82f175300a62e70256f90d32340d320e9d247cfeea9efcb93ca328bcf`

```dockerfile
```

-	Layers:
	-	`sha256:76661fe317ee561cfdc8474a4248d528401bb54aafd7d2c806f64d88bb16b417`  
		Last Modified: Wed, 04 Mar 2026 17:50:17 GMT  
		Size: 5.1 MB (5121928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:641a454cdf582c09322dadfe2860df03cde8301d464da79173af0db0c9b265ad`  
		Last Modified: Wed, 04 Mar 2026 17:50:17 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1612-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:99e9d9daad0fe0b0811b71f9032aa186546fb5e22cf692062e987becb369e7e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.1 MB (253050983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637e1f0deeaeb8fa466ddaa06d3d88e84233f5b49579680fa03aa8a86e118669`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Wed, 04 Mar 2026 17:57:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:57:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:57:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:57:16 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:57:17 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:58:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:58:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:58:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:58:23 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:58:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3def25e912c223ee8b3899e5ca048b2439f856f438ac690293817fbc0291fb36`  
		Last Modified: Tue, 24 Feb 2026 18:41:49 GMT  
		Size: 32.1 MB (32078334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c36420ec7af61268c4b524afcf7adfb9959462e77cf94d8569576f66caac0b7`  
		Last Modified: Wed, 04 Mar 2026 17:59:09 GMT  
		Size: 145.4 MB (145438252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65335e3b84175708cb4132ed9aef16b5f0c3b153feb1cf2e37490d990bf4da0d`  
		Last Modified: Wed, 04 Mar 2026 17:59:06 GMT  
		Size: 75.5 MB (75533354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a82251de46511519592982f7062de6e45e3d3b3521ff1e5cd39bd4b2690127`  
		Last Modified: Wed, 04 Mar 2026 17:59:03 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0842d1a0c46986191e006a73839c1503ad18cd9869c9dd5020f796842adffa`  
		Last Modified: Wed, 04 Mar 2026 17:59:03 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1612-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dc243be3ebc051768dfe95c78586603e98c75715fdbaded3aea558fda7521bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0fff56fb2177ee052affecd0264a47b122225b3794e572c79c6df49c6e45eeb`

```dockerfile
```

-	Layers:
	-	`sha256:93dc0012ee1453d5cf22af58b949a1394411f8597f7a76a4d74998fb16566f03`  
		Last Modified: Wed, 04 Mar 2026 17:59:03 GMT  
		Size: 5.1 MB (5121325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:247d7e13566e9b60684b28913c8f41568e0990965d0850d93066719faacff8ec`  
		Last Modified: Wed, 04 Mar 2026 17:59:03 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1612-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:501f15cf3af8548c49685378679446a3206857ca110f1d840c4c5b5cba2ea9ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231033051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f5afa045f3b89f709b0dcb767b20b8fc848e4764d20712a803d35a7e0ab371a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Wed, 04 Mar 2026 17:49:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:49:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:49:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:49:06 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:49:06 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:49:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:49:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:49:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:49:19 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:49:19 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2958aa0249852b5d012866780f27028b7b7939636684f9d883c62168e418a7`  
		Last Modified: Wed, 04 Mar 2026 17:49:48 GMT  
		Size: 135.6 MB (135627087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59eb75aa68d206dff4557fd8cf6bf94389982c578eb09702d8fda3e2e638b59`  
		Last Modified: Wed, 04 Mar 2026 17:49:47 GMT  
		Size: 68.5 MB (68513398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56c0531388f7ca4a3feac5e724084f6ccee3349d38926da126b44b13c34efbb`  
		Last Modified: Wed, 04 Mar 2026 17:49:45 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41416317ebeb317d8435982c03b49f6b341a0f80c4361bcb8c6ff9950b645cb`  
		Last Modified: Wed, 04 Mar 2026 17:49:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1612-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4ccc7bff63f5a18b20791bf3ad0e18e39f9ee3d4d431e07fa79c87aaa457a365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5123324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fde516ecc87c2d61d9e79981bfce9935407ac6d94af2672396c859b43a0300e`

```dockerfile
```

-	Layers:
	-	`sha256:0a12d2b55fd28c39048e232dc524c2bd70bda377126ad6155170af4111c90483`  
		Last Modified: Wed, 04 Mar 2026 17:49:45 GMT  
		Size: 5.1 MB (5107488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06c85a6f2956e68828640c1979c7aa98a6a29f255421b2ee06a963526328acd4`  
		Last Modified: Wed, 04 Mar 2026 17:49:45 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json
